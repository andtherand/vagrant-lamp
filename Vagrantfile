#!/usr/bin/env ruby
#^syntax detection

data_base_path = "data/vagrant/"

Vagrant.configure("2") do | config |
  config.vm.box = "precise32"
  #config.vm.box_url = "http://files.vagrantup.com/precise32.box"

  config.vm.network :private_network, ip: "33.33.33.10"

  # Dependencies on vagrant plugins
  config.omnibus.chef_version = :latest
  config.vbguest.auto_update = true
  config.librarian_chef.cheffile_dir = data_base_path

  # virtualbox specific settings
  config.vm.provider :virtualbox do | vb |
    vb.customize ["modifyvm", :id, "--memory", 1024]
  end

  config.vm.provision :chef_solo do | chef |
    chef.cookbooks_path = [data_base_path + "cookbooks"]
    chef.roles_path = data_base_path + "roles"

    chef.add_role "lamp"

  end
end
