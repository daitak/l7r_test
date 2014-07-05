# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos65"
  config.vm.box_url = "http://www.lyricalsoftware.com/downloads/centos65.box"
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--natdnsproxy1", "off"]
  end

  config.vm.define :web1 do |web1|
    web1.vm.host_name = "web1"
    web1.vm.network :private_network, ip: "192.168.56.10"
  end

  config.vm.define :redis1 do |redis1|
    redis1.vm.host_name = "redis1"
    redis1.vm.network :private_network, ip: "192.168.56.11"
  end
end
