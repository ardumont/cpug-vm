# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.define :vm do |vm_config|
    vm_config.vm.box = "quantal"
    vm_config.vm.box_url = "https://github.com/downloads/roderik/VagrantQuantal64Box/quantal64.box"
    vm_config.vm.customize ["modifyvm", :id,  "--natdnshostresolver1", "on", "--memory", 1024]
    vm_config.vm.network :hostonly, "192.168.33.10"
    vm_config.vm.host_name = "clojure-vm"
#    vm_config.vm.share_folder "v-data-1", "/etc/puppet/", "./puppet/UNIX_ROOT/etc/puppet/"
    vm_config.vm.provision :shell, :path => "./bootstrap.sh"
  end
end
