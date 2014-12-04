# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.define :Xen do |xen_config|
    xen_config.vm.hostname = "Xen"
    xen_config.vm.network "private_network", ip: "192.168.35.33"
  end

  config.vm.define :Vlab_Gluster1 do |gluster_config1|
    gluster_config1.vm.hostname = "Vlab-gluster1"
    gluster_config1.vm.network "private_network", ip: "192.168.35.11"
  end

  config.vm.define :Vlab_Gluster2 do |gluster_config2|
    gluster_config2.vm.hostname = "Vlab-gluster2"
    gluster_config2.vm.network "private_network", ip: "192.168.35.22"
  end

  config.vm.define :Vital do |vital_config|
    vital_config.vm.hostname = "Vital"
    vital_config.vm.network "private_network", ip: "192.168.35.2"
    vital_config.vm.network "forwarded_port", guest: 80, host: 80
    vital_config.vm.network "forwarded_port", guest: 443, host: 443
  end

end
