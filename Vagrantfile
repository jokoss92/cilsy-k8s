Vagrant.configure("2") do |config|

### master instance
  config.vm.define "master" do |master|
    master.vm.box = "bento/ubuntu-18.04"
    master.vm.network "public_network", ip: "192.168.1.202"
    master.vm.provision :shell do |shell|
      shell.args = "1"
      shell.path = "https://gist.githubusercontent.com/rizkyramadhanch/95f72fe6e4791a9da1bfdba765a0b60c/raw/f149874543a6813137533c16f77635058f9b2731/web_server_config.sh"
    end
  end

### worker instance
  config.vm.define "worker" do |worker|
    worker.vm.box = "bento/ubuntu-18.04"
    worker.vm.network "public_network", ip: "192.168.1.203"
    worker.vm.provision :shell do |shell|
      shell.args = "2"
      shell.path = "https://gist.githubusercontent.com/rizkyramadhanch/95f72fe6e4791a9da1bfdba765a0b60c/raw/f149874543a6813137533c16f77635058f9b2731/web_server_config.sh"
    end
  end
end
