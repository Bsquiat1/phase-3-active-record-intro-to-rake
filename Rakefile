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

namespace :db do
  desc 'migrate chenges to our database'
  task migrate: :environment do
    Student.create_table
  end
  desc 'seed the database with some dummy data'
  task seed: :environment do
    require_relative './db/seeds'
  end
  
  desc 'drop into the pry console'
  task console: :environment do
    Pry.start
  end
end
task :environment do
  require_relative './config/environment'
end
