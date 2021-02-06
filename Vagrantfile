Vagrant.configure("3") do |config|

### master instance
  config.vm.define "master" do |master|
    master.vm.box = "bento/ubuntu-18.04"
    master.vm.network "public_network", bridge: "wlo1", ip: "192.168.1.202"
    master.vm.provision :shell do |shell|
      shell.args = "1"
      shell.path = "https://gist.githubusercontent.com/rizkyramadhanch/de2fc3a0978b34440d77b50d3c76281e/raw/bb95cf4465ecf3d3070bce5b811bf19561447dc0/kube_master.sh"
    end
  end

### worker1 instance
  config.vm.define "worker1" do |worker1|
    worker1.vm.box = "bento/ubuntu-18.04"
    worker1.vm.network "public_network", bridge: "wlo1", ip: "192.168.1.203"
    worker1.vm.provision :shell do |shell|
      shell.args = "2"
      shell.path = "https://gist.githubusercontent.com/rizkyramadhanch/99404d7bedab90cc666b04b3b11faf93/raw/b0ff6b87b4d96065a4edfa15a85ab1f3ee781b5e/worker1.sh"
    end
  end

### worker2 instance
  config.vm.define "worker" do |worker2|
    worker2.vm.box = "bento/ubuntu-18.04"
    worker2.vm.network "public_network", bridge: "wlo1", ip: "192.168.1.204"
    worker2.vm.provision :shell do |shell|
      shell.args = "3"
      shell.path = "https://gist.githubusercontent.com/rizkyramadhanch/3c112bc87f0be849209d8782cacf7856/raw/b94d344465bf8ba94d3b70678a227cfd5ec38795/worker2.sh"
    end
  end
end
