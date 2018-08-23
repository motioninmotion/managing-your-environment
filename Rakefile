# -*- coding: utf-8 -*-
$:.unshift("/Library/RubyMotion/lib")
$:.unshift("~/.rubymotion/rubymotion-templates")

require 'motion/project/template/ios'

begin
  require 'bundler'
  Bundler.require
rescue LoadError
end

Dotenv.load
Dotenv.overload(".env.local")

# puts ENV["API_HOST"]

Motion::Project::App.setup do |app|
  app.name = 'ManagingYourEnvironment'

  app.development do
    Dotenv.load(".env.development")
  end

  app.release do
    Dotenv.load(".env.release")
  end

  app.env['API_HOST'] =  ENV["API_HOST"]

  if ENV["RM_ENV"] == "development"
  elsif ENV["RM_ENV"] == "adhoc"
  elsif ENV["RM_ENV"] == "release"
  end
end
