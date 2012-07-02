require 'yaml'
require 'json'
require 'alpha_omega/deploy'

set :repository, "https://github.com/HeSYINUvSBZfxqA/getting-started.git"
set :application, "getting_started"
set :deploy_to, "/data/#{application}"

set :user, "XXX"
set :group, "XXX"

# ruby
set :ruby_loader, "/usr/local/bin/rvmrun default"

# branches
set :branch, AlphaOmega.what_branch(%w(master staging) + [%r(/)])

# pods, hosts, groups
AlphaOmega.setup_pods self, ENV['CHEF_PATH'] do |adm,n| 
  { :deploy => { }
  }
end

task :hello do
  run "uname -a"
end
