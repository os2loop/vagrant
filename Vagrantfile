VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "3072"]
    vb.customize ["modifyvm", :id, "--cpus", "2"]
  end

  # Box info
  config.vm.box = "chef/debian-7.6"
  config.vm.box_check_update = true

  # Hostname
  config.vm.hostname = "loop.vm"

  # IP
  config.vm.network "private_network", ip: "192.168.50.11"

  # Shared folder
  config.vm.synced_folder ".", "/vagrant", type: "nfs"

  # What to install
  config.vm.provision :shell, :path => "bootstrap.sh"

  # SSH
  config.ssh.forward_agent = true
end
