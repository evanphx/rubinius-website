dir = ENV['RBX']

task :sync do
  if !dir or !File.directory?(dir)
    puts "Please set the RBX variable"
    fail
  end

  Dir.mkdir "public" unless File.directory? "public"

  sh "rsync -r #{dir}/web/_site/ public/"
end
