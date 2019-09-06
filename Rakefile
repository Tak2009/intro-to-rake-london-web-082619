
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

desc 'outputs comments in console'
task :console do
  puts "Make sure you have a 'console' rake task"
end


namespace :db do

  desc 'need to give our task access to enviromnet.rb'
  task :environment do
    require_relative './config/environment'
  end

  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end
  
  desc 'seed the database with some dummy data'
    task :seed do
      require_relative './db/seeds.rb'
    end
  
    desc 'drop into the Pry console'
     task :console => :environment do
     Pry.start
  end

end

  

