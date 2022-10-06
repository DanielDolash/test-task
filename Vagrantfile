  Vagrant.configure("2") do |config|
    config.vm.box = "generic/ubuntu"
    config.vm.synced_folder "docker-cont/", "/opt/docker"
    config.vm.provider "virtualbox" do |v|
      v.name = "ubuntu2004"
      v.cpus = 2
      v.memory = 4096
      v.check_guest_additions = false
  end

  
  config.vm.network "private_network", ip: "192.168.60.25"
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.network "forwarded_port", guest: 9090, host: 9090




  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
