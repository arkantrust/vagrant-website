Vagrant.configure("2") do |config|

  # use ubuntu 24.04
  config.vm.box = "ubuntu/noble64-server"

  config.vm.network "private_network", type: "dhcp"

  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y apache2
  SHELL

  # config static files
  config.vm.synced_folder ".", "/var/www/html"

  # config vm
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "512"
  end

end