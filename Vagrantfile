Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/bionic64"
  
  config.vm.network "forwarded_port", guest: 80, host: 4444

  # run Ansible from the Vagrant VM
  config.vm.provision "ansible_local" do |ansible|
    ansible.install = true
    # ansible.sudo = true
    ansible.playbook = "provisioning/deploy.yaml"
  end

  # add localhost to Ansible inventory
  config.vm.provision "shell", inline: "printf 'localhost\n' | sudo tee /etc/ansible/hosts > /dev/null"

end
