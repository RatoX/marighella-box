require_relative './key_authorization'

Vagrant.require_version ">= 1.8.5"

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.ssh.insert_key = true
  config.vm.network "private_network", ip: "192.168.50.4"
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.hostname = "dev.marighella.io"
  config.hostsupdater.aliases = ["dev.marighella.io"]


  authorize_key_for_root config, '~/.ssh/id_rsa.pub'
  config.vm.provision :shell, inline: "apt-get update"
end
