namespace :greeting do

  desc 'puts hello'
  task :hello do
    puts 'hello from Rake!'
  end

  desc 'puts hola'
  task :hola do
    puts 'hola de Rake!'
  end

end

desc 'starts an IRB with the environment loaded'
task :console => :environment do
  Pry.start
end

desc 'loads environment'
task :environment do
  require_relative './config/environment.rb'
end

namespace :db do

  desc 'migrates database'
  task :migrate => :environment do
    Student.create_table
  end

  desc 'plants seed data'
  task :seed do
    require_relative './db/seeds.rb'
  end
end