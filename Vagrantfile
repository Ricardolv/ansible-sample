Vagrant.configure("2") do |config|

    config.vm.box = "ubuntu/trusty64"
     
    config.vm.define "wordpress" do |wordpress|

        wordpress.vm.synced_folder ".", "/vagrant", disabled: true

        wordpress.vm.provider "virtualbox" do |vb|
            vb.memory = 1024
            vb.cpus = 1
            vb.name = "wordpress"
        end

        wordpress.vm.network "private_network", ip: "172.17.177.40"
    end

    config.vm.define "mysql" do |mysql|

        mysql.vm.synced_folder ".", "/vagrant", disabled: true

        mysql.vm.provider "virtualbox" do |vb|
            vb.memory = 1024
            vb.cpus = 1
            vb.name = "mysql-server"
        end

        mysql.vm.network "private_network", ip: "172.17.177.41"
    end

end