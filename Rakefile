# ex. 
# rake  --trace install_all DESTDIR=${HOME}/.emacs.d/plugins/yasnippet/snippets/text-mode/html-mode/
task :default => [:install_all]

INSTALL_CMD = 'install -v'
namespace :install do 
  ['root-element'].each do |str|
    desc "#{str} snippets"
    task str  do 
      if ENV['DESTDIR']
        sh "#{INSTALL_CMD} #{str}/* #{ENV['DESTDIR']}"
      else
        puts "please specify 'DESTDIR=/path/to/html-mode'"
        exit 1
      end
    end
  end
end

desc "install all extra snippets"
task :install_all => ['install:root-element']  do; end

