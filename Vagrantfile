
Vagrant.configure("2") do |config|
  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true


#Nginx VM
  config.vm.define "nginx" do |nginx|
    nginx.vm.box= "ubuntu/trusty64[[O"
    nginx.vm.hostname= "nginx"
    nginx.vm.network "private_network", ip: "192.168.56.5"
    nginx.vm.provision "shell",
      inline: "yum install net-tools vim -y"
  end

#tomcat VM
  config.vm.define "tomcat" do |tomcat|
    tomcat.vm.box= "centos/7"
    tomcat.vm.hostname= "tomcat"
    tomcat.vm.network "private_network", ip: "192.168.56.10"
    tomcat.vm.provider "virtualbox" do |vt|
      vt.memory= "1024"
    tomcat.vm.provision "shell",
      inline: "yum install net-tools vim -y"
    end
  end


#RabbitMQ VM
  config.vm.define "rabbit" do |rabbit|
    rabbit.vm.box= "centos/7"
    rabbit.vm.hostname= "rabbit"
    rabbit.vm.network "private_network", ip: "192.168.56.15"
    rabbit.vm.provision "shell",
      inline: "yum install net-tools vim -y"
  end


#Memcached VM
  config.vm.define "memcached" do |memcached|
    memcached.vm.box= "centos/7"
    memcached.vm.hostname= "memcached"
    memcached.vm.network "private_network", ip: "192.168.56.20"
    memcached.vm.provision "shell",
      inline: "yum install net-tools vim -y"
  end


#DB VM
  config.vm.define "db" do |db|
    db.vm.box= "centos/7"
    db.vm.hostname= "db"
    db.vm.network "private_network", ip: "192.168.56.25"
    db.vm.provision "shell",
      inline: "yum install net-tools  vim -y"
  end
end
