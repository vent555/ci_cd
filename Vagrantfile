
Vagrant.configure("2") do |config|
    #One key to all hosts
      config.ssh.insert_key = false
    #Three vagrant hosts configuration
      config.vm.define "jenkins" do |jenkins|
        jenkins.vm.box = "ubuntu/focal64"
        jenkins.vm.network "forwarded_port", guest: 8080, host: 8080
      end
      config.vm.provider "virtualbox" do |v|
        v.name = "jenkins"
        v.memory = 3072
        v.cpus = 2
      end
    end