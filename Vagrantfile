Vagrant.configure '2' do |config|
  config.vm.box = 'trusty-14_04'
  config.vm.box_url = 'https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-i386-vagrant-disk1.box'

  config.vm.hostname = 'localhost'

  config.vm.provider :virtualbox do |v|
    v.memory = 1024
    v.customize ['modifyvm', :id, '--natdnshostresolver1', 'on']
    v.customize ['modifyvm', :id, '--natdnsproxy1', 'on']
  end

  config.vm.provider :vmware_fusion do |v|
    v.vmx['memsize'] = '1024'
    v.vmx['numvcpus'] = '8'
  end

  config.vm.provider :parallels do |v, override|
    override.vm.box = 'parallels/ubuntu-14.04'
  end

  # Forward the port from the VM to the host machine for the app.
  config.vm.network :forwarded_port, guest: 3000, host: 3000

  config.vm.provision :ansible do |ansible|
    ansible.playbook = 'playbook.yml'
  end
end
