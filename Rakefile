desc 'run static http server on port 8888'
task :server do
  require 'webrick'
  WEBrick::HTTPServer.new(:DocumentRoot => "./", :Port => 8888).start
end
