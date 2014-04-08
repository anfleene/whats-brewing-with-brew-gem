require 'bundler'
Bundler.setup

desc 'Default: run library specs.'
task :default => :release

desc "Push to github, github pages, and heroku"
task :release do |t|
  system "git push origin master"
  system "bundle exec showoff github"
  system "rm -r static"
  system "git push heroku master"
end
