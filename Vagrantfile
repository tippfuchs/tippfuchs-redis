# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.hostname = "tippfuchs-redis"
  config.vm.box = "ubuntu1204"
  # config.vm.box_url = "https://opscode-vm.s3.amazonaws.com/vagrant/opscode_ubuntu-12.04-i386_provisionerless.box"
  
  config.vm.boot_timeout   = 120
  config.berkshelf.enabled = true
  config.omnibus.chef_version   = :latest

  config.vm.provision :chef_solo do |chef|
    chef.run_list = [
      "recipe[tippfuchs-redis::default]"
    ]
  end
end