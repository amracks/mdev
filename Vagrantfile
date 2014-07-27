# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box     = "CentOS-6.5-Desktop-05212014-x64.box"
  config.vm.box_url = "http://www.freebsd.org/releases/9.3R/schedule.html"

  config.vm.network "public_network"

  config.ssh.private_key_path = "modules/vagrantkey/files/id_rsa"

  config.vm.provider "virtualbox" do |v|
        v.gui  = false
        v.name = "MDev"
  end

  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = "manifests"
    puppet.manifest_file  = "init.pp"
    puppet.module_path    = "modules"
    puppet.hiera_config_path = "conf/hiera.yaml"
  end

end
