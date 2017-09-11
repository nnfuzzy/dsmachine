# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Every Vagrant virtual environment requires a box to build off of.
  config.ssh.insert_key=false
  #config.vm.box = "ubuntu/trusty64"
  config.vm.box = "continuumio/anaconda3"
  # ubuntu/xenial64 has problems with ssh key login
  # alternative could be  see https://stackoverflow.com/questions/40384811/unable-to-ssh-to-vagrant-ubuntu-16-04
  # config.vm.box = "bento/ubuntu-16.04"

  config.vm.hostname = "default"
  config.vm.network "private_network", ip: "10.0.0.10"
  config.ssh.insert_key = false

  #config.vm.provision "ansible"  do |ansible|
  #    ansible.playbook = "data-science.yml"
  #end

  config.vm.provider "virtualbox" do |vb|
      # Don't boot with headless mode
      vb.gui = false

      # Use VBoxManage to customize the VM. For example to change memory:
      vb.customize ["modifyvm", :id, "--memory", "8192","--cpus", "2"]
  end
end
