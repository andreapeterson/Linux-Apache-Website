Vagrant.configure("2") do |config|
  config.vm.box = "eurolinux-vagrant/centos-stream-9"

  config.vm.network "private_network", ip: "192.168.56.30"
  config.vm.network "public_network"

  config.vm.synced_folder "/Users/andrea/Desktop/vagrant-vms/website_IAC/my_website", "/var/www/html/", type: "rsync", rsync__auto: true

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end

  config.vm.provision "shell", inline: <<-SHELL
    sudo yum update -y
    sudo yum install httpd wget vim unzip zip rsync -y
    sudo systemctl start httpd
    sudo systemctl enable httpd
  SHELL
end
