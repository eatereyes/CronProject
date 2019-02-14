# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "forwarded_port", guest: 80, host: 5050
  config.vm.network "forwarded_port", guest: 3306, host: 4564
  config.vm.synced_folder ".", "/var/www/html/php", mount_options: ["dmode=775,fmode=777"]
  config.vm.provider "virtualbox" do |vb|
    vb.name = "Cron"
  end
  config.vm.provision "shell", path: "install/lampserver.sh"
end
