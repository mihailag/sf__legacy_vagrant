Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.box_check_update = false
  config.vm.network "public_network"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end
  
  config.vm.provision "shell", inline: <<-SHELL
    sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
    wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
    sudo apt-get update
    sudo DEBIAN_FRONTEND=noninteractive apt-get -y install postgresql-8.4
  SHELL
end
