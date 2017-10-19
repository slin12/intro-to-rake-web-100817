namespace :greeting do
  desc 'outputs hello to the terminal'
  task :hello do
    puts "hello from Rake!"
  end

  desc 'outsputs hola to the terminal'
  task :hola do
    puts "hola de Rake!"
  end
end

task :environment do
  require_relative './config/environment.rb'
end

namespace :db do
  desc 'migrates changes to your database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'seeds database with data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end

desc 'starts console'
task :console => :environment do
  Pry.start
end
