require 'fileutils'

task :default do
  exec "rake -T"
end

desc "init"
task :init do 
  puts "--- init ---"
  FileUtils.mkdir_p("./plugins")
  if Dir.exist?("./plugins/tpm")
    sh "cd ./plugins/tpm && git pull"
  else
    sh "git clone https://github.com/tmux-plugins/tpm ./plugins/tpm"
  end
end
task :i => [:init]

desc "Clean everything"
task :clean do 
  FileUtils.rm_rf("./plugins")
end

