# Vagrant configuration version
Vagrant.configure("2") do |config|

  # Enable and configure hostmanager plugin
  config.hostmanager.enabled = true 
  config.hostmanager.manage_host = true

  # Define NexusServer VM
  config.vm.define "NexusServer" do |nexus|
      # Set the box for NexusServer VM
      nexus.vm.box = "bento/amazonlinux-2"
      # Set the hostname for NexusServer VM
      nexus.vm.hostname = "NexusServer"
      # Configure a private network for NexusServer VM with a static IP
      nexus.vm.network "private_network", ip: "192.168.56.21"
      # Configure VirtualBox provider settings for NexusServer VM
      nexus.vm.provider "virtualbox" do |vb|
          vb.memory = "3072" # Set memory to 3 GB
          vb.cpus = "3" # Set number of CPUs to 3
      end
      # Provision NexusServer VM with a shell script
      nexus.vm.provision "shell", path: "userdata/nexus.sh"
  end


#   # Define SonarServer VM
#   config.vm.define "SonarServer" do |sonar|
    #   # Set the box for SonarServer VM
    #   sonar.vm.box = "ubuntu/bionic64"
    #   # Set the hostname for SonarServer VM
    #   sonar.vm.hostname = "SonarServer"
    #   # Configure a private network for SonarServer VM with a static IP
    #   sonar.vm.network "private_network", ip: "192.168.56.31"
    #   # Configure VirtualBox provider settings for SonarServer VM
    #   sonar.vm.provider "virtualbox" do |vb|
        #   vb.memory = "3072" # Set memory to 3 GB
        #   vb.cpus = "3" # Set number of CPUs to 3
    #   end
    #   # Provision SonarServer VM with a shell script
    #   sonar.vm.provision "shell", path: "userdata/sonar.sh"
#   end

end
