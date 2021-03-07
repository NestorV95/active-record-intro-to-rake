task :environment do
  require_relative './config/environment'
end 
#enviorment gives our Rakefile access to the rest of our files via enviorment.

namespace :greeting do

  desc 'outputs hello to the terminal'
    task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hola to the terminal'
    task :hola do
    puts "hola de Rake!"
  end

end
# namespace :greeting is just a custom task that ot puts message when called.

namespace :db do

  desc 'migrate changes to your database'
    task :migrate => :environment do
    Student.create_table
  end
  
  desc 'seed the database with some dummy data'
  task :seed do
    require_relative './db/seeds.rb'
  end

end
#namespace :db depends on the eniorment to create student table in database.

desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end
#opens up a pry session for us.
