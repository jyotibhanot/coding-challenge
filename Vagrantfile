Vagrant.configure(2) do |config|

# box to build virtual evironment to build off of.
  config.vm.box = "ubuntu/trusty64"

# Create a private network, which allows host-only access to the machine
# using a specific IP

  config.vm.network :private_network, ip: "10.10.10.20"

# configurating the vm

  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048", "--cpus", "2", "--cpuexecutioncap", "100"]
  end

# Use ansible playbook to "provision" the box. This playbook sets up and deploy the flask application.

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "flask-app.yml"
  end
end
