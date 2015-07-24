# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"
BOX_URL_TRUSTY32 = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-i386-vagrant-disk1.box"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define "testserver" do |testserver|
    testserver.vm.box = "ubuntu/trusty32"
    testserver.vm.box_url = BOX_URL_TRUSTY32
    testserver.vm.network :private_network, ip: "192.168.245.101"
    testserver.vm.provision "ansible" do |ansible|
      ansible.limit = "testserver"
      ansible.playbook = "site.yml"
      ansible.inventory_path = "vagrant_hosts"
      ansible.verbose = "vvvv"
    end
  end
end
