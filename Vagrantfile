Vagrant.configure("2") do |config|
  config.vm.define :master do |master|
    master.vm.box = "ubuntu/focal64"
    master.vm.network :private_network, ip: "172.72.72.10"
    master.vm.hostname = "master"
    master.vm.provision :shell, inline: "sudo curl -fsSL https://get.docker.com | sh"
  end

  config.vm.define :worker1 do |worker1|
    worker1.vm.box = "ubuntu/focal64"
    worker1.vm.network :private_network, ip: "172.72.72.20"
    worker1.vm.hostname = "worker1"
    worker1.vm.provision "shell", inline: "sudo curl -fsSL https://get.docker.com | sh"
  end
  
  config.vm.define :worker2 do |worker2|
    worker2.vm.box = "ubuntu/focal64"
    worker2.vm.network :private_network, ip: "172.72.72.30"
    worker2.vm.hostname = "worker2"
    worker2.vm.provision "shell", inline: "sudo curl -fsSL https://get.docker.com | sh"
  end
end