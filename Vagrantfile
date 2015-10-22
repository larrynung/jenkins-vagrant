Vagrant.configure(2) do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"

  config.vm.provision "shell", inline: $script
  config.vm.network "forwarded_port", guest: 8080, host: 8080
end

$script = <<SCRIPT
  sudo apt-get update
  sudo apt-get -y install jenkins
SCRIPT