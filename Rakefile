namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outputs hello to the terminal in spanish'
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc 'migrate changes to your database'
  task :migrate => :environment do
    Student.create_table
  end
  
  desc 'seed your database'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'console'
task :console do
  Pry.start
end
