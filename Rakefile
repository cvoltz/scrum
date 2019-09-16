# Copyright (C) 2019 Christopher Voltz

require "rake/clean"

PRESENTATION = "scrum"

CLEAN.include("#{PRESENTATION}/*")

task :default => [:build]

desc "Create presentation"
task :build do
  cmd = "hovercraft -c #{PRESENTATION}.css #{PRESENTATION}.rst #{PRESENTATION}"
  if ENV["_system_name"] =~ /centos/i
    cmd = %Q[scl enable python37 "#{cmd}"]
  end
  sh cmd
end

desc "View presentation"
task :view do
  sh "gio open #{PRESENTATION}/index.html"
end

desc "Publish presentation"
task :sync do
  sh "rsync -avzP --delete Rakefile #{PRESENTATION}{.rst,/} voyager:/var/www/html/sths/#{PRESENTATION}/"
end

desc "Automatically rebuild presentation"
task :guard do
  sh "bin/guard start"
end

desc "Setup environment"
task :setup do
  sh "bundle install --binstubs"
end
