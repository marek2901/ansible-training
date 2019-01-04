# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|
  config.vm.box = "centos/7"
  config.vm.network 'forwarded_port',
                    guest: 80, host: 1234, host_ip: '127.0.0.1'

  config.vm.provider 'virtualbox' do |vb|
    vb.cpus = 4
    vb.memory = '8096'
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible-fun/root.yml"
  end
end
