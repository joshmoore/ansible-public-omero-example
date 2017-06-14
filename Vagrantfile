Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--memory", "2048"]
  end


  [
    "public-user",
    "all-in-one",
    "two-nodes-database",
    "two-nodes-omero",
    "firewalled",
  ].each do |server|
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "#{server}.yml"
      ansible.galaxy_role_file = "requirements.yml"
    end
  end
end
