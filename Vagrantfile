Vagrant.configure '2' do |config|
  config.vm.box = 'precise64-latest'
  config.vm.box_url = 'http://cloud-images.ubuntu.com/vagrant/precise/current/precise-server-cloudimg-amd64-vagrant-disk1.box'

  config.vm.network :forwarded_port, guest: 3000, host: 3000

  config.vm.provision :ansible do |ansible|
    ansible.playbook = 'playbook.yml'
  end
end
