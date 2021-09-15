Vagrant.configure("2") do |config|
  config.vm.box = "gusztavvargadr/windows-server"
  config.vm.box_version = "1809.0.2106"  
  config.vm.provision :shell, path: "provision.ps1"
  config.vm.network "forwarded_port", guest: 8081, host: 8081
  config.vm.network "forwarded_port", guest: 10000, host: 10000
  config.vm.network "forwarded_port", guest: 10001, host: 10001
  config.vm.network "forwarded_port", guest: 10002, host: 10002
  config.vm.network "forwarded_port", guest: 10255, host: 10255
  config.vm.provider "virtualbox" do |pmv|
    pmv.memory = 8192
    pmv.cpus = 2
    pmv.gui = false
  end
end