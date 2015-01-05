# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "searchsuite"
  config.vm.box_url = "https://github.com/2creatives/vagrant-centos/releases/download/v6.5.3/centos65-x86_64-20140116.box"
  config.vm.network "private_network", ip: "192.168.33.11"
  config.vm.synced_folder "../searchsuite/", "/vagrant_data",  owner: "vagrant", group: "apache", :mount_options => ['dmode=777','fmode=777']
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"
  end

end

