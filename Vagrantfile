Vagrant.configure('2') do |config|
  config.vm.box = 'phusion/ubuntu-14.04-amd64'
  config.vm.synced_folder '.', '/dockreduce'
  config.vm.network :forwarded_port, guest: 5000, host: 5000
  config.ssh.forward_agent = true
  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'ansible/development.yml'
    ansible.verbose = 'v'
  end
end
