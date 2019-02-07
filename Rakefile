namespace :greeting do
  desc "Outputs hello to the terminal"
  task :hello do
    puts "hello from Rake!"
  end

  desc "Outputs hola to the terminal"
  task :hola do
    puts "hola de Rake!"
  end
end

namespace :db do
  desc "Migrate changes to your database"
  task :migrate => :environment do
    Student.create_table
  end

  desc "Seed the database with some dummy data"
  task :seed do
    require_relative './db/seeds.rb'
  end
end

task :environment do
  require_relative './config/environment'
end

desc "Drop into the Pry console"
task :console => :environment do
  Pry.start
end