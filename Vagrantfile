# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|
  config.vm.box      = 'ubuntu/wily64'
  config.vm.hostname = 'rails-dev-box'

  config.vm.network :forwarded_port, guest: 3000, host: 3000, auto_correct: true

  config.vm.provision :shell, path: 'bootstrap.sh', keep_color: true

  config.vm.synced_folder '../project', '/vagrant/dev'
  config.proxy.https = 'https://10.100.12.253:3128'
  config.proxy.http = 'http://10.100.12.253:3128'
end

# export VAGRANT_HTTP_PROXY='https://10.100.12.253:3128'