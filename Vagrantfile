
Vagrant.configure("2") do |config|
    #One key to all hosts
      config.ssh.insert_key = false
    #Three vagrant hosts configuration
      config.vm.define "jenkins" do |jenkins|
        jenkins.vm.box = "ubuntu/focal64"
        jenkins.vm.hostname = "jenkins"
        jenkins.vm.network "private_network", ip: "192.168.50.100"
      end
      config.vm.provider "virtualbox" do |jenkins|
        jenkins.memory = 3072
        jenkins.cpus = 2
      end
      config.vm.define "k8s1" do |k8s1|
        k8s1.vm.box = "ubuntu/focal64"
        k8s1.vm.hostname = "k8s1"
        k8s1.vm.network "private_network", ip: "192.168.50.101"
      end
      config.vm.provider "virtualbox" do |k8s1|
        k8s1.memory = 2048
        k8s1.cpus = 2
      end
      config.vm.define "k8s2" do |k8s2|
        k8s2.vm.box = "ubuntu/focal64"
        k8s2.vm.hostname = "k8s2"
        k8s2.vm.network "private_network", ip: "192.168.50.102"
      end
      config.vm.provider "virtualbox" do |k8s2|
        k8s2.memory = 2048
        k8s2.cpus = 2
      end
    end