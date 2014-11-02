# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "precise64-server"
  config.vm.provision "shell", path: "myprov.sh"
  config.vbguest.auto_update = false

  config.vm.define "web" do |web|
    web.vm.provision "shell", inline: "apt-get install nginx -y"
    #web.vm.box = "apache"
  end

  config.vm.define "db" do |db|
    db.vm.provision "shell", inline: "apt-get install mysql-server -y"
    #db.vm.box = "mysql"
  end
end

