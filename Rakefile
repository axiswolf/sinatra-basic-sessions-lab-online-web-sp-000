ENV["SINATRA_ENV"] ||= "development"

require_relative './config/environment'

# Type `rake -T` on your command line to see the available rake tasks.
def reload!
	load_all "./config" if Dir.exists?("./config")
	load_all "./app" if Dir.exists?("./app")
	load_all "./lib" if Dir.exists?("./lib")
	load_all "./*.rb" if Dir.entries(".").include?(/\.rb/)
end

task :console do
  reload!
  Pry.start
end
