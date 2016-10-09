# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  # Foward port from host to guest
  config.vm.network "forwarded_port", guest: 80, host: 8080 #http

  # Private IP
  config.vm.network "private_network", ip: "192.168.33.44"

  # Folder synced from host to vagrant vm
  config.vm.synced_folder "projects/", "/var/www/html/", create:true, id: "vagrant-root",
    owner: "vagrant",
    group: "www-data",
    mount_options: ["dmode=775,fmode=664"]
  
  
  # Ansible provisioner
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"
  end

end
