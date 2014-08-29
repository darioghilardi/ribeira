Vagrant.configure '2' do |config|
  config.vm.box = 'trusty-14_04'
  config.vm.box_url = 'https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-i386-vagrant-disk1.box'

  config.vm.network :forwarded_port, guest: 3000, host: 3000

  config.vm.provision :ansible do |ansible|
    ansible.playbook = 'playbook.yml'
  end
end
