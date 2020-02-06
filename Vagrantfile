Vagrant.configure(2) do |config|
  config.vm.define "webserver1" do |webserver1|
    webserver1.vm.box = "ubuntu/bionic64"
    webserver1.vm.network :private_network, ip: "192.168.0.10"
    webserver1.vm.hostname = "webserver1"
    webserver1.vm.provision :shell, path: "webserver-bootstrap.sh"
  end
  
  config.vm.define "webserver2" do |webserver2|
    webserver2.vm.box = "ubuntu/bionic64"
    webserver2.vm.network :private_network, ip: "192.168.0.20"
    webserver2.vm.hostname = "webserver2"
    webserver2.vm.provision :shell, path: "webserver-bootstrap.sh"
  end

  config.vm.define "ansible" do |ansible|
    ansible.vm.box = "ubuntu/bionic64"
    ansible.vm.network :private_network, ip: "192.168.0.254"
    ansible.vm.hostname = "ansible"
    ansible.vm.provision :shell, path: "ansible-bootstrap.sh"
  end
end
