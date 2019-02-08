# Environment 
desc 'require the environment'
task :environment do
  require_relative './config/environment'
end

# Example nested tasks inside a namespace
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

# Essential support for using databases
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

# Console support
desc 'drop into the Pry console'
task :console => :environment do
  Pry.start
end