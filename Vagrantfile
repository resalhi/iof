Vagrant.configure("2") do |config|
  config.vm.define "ressalhiS" do |machine|
    machine.vm.box = "debian/bullseye64"
    machine.vm.network "private_network", ip: "192.168.56.110"
    machine.vm.hostname = "ressalhiS"
    machine.vm.provider "virtualbox" do |vb|
      vb.name = "ressalhiS"
      vb.cpus = "1"
      vb.memory = "1024"
    end

    machine.vm.provision "shell", inline: <<-SHELL
      sh /vagrant/scripts/setup.sh
    SHELL
  end
end