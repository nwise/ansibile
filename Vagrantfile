# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
VAGRANT_API_VERSION = "2"
Vagrant.configure(VAGRANT_API_VERSION) do |config|
  config.ssh.insert_key = false

  config.vm.define "vagrant1" do |vagrant|
    vagrant.vm.box = "ubuntu/trusty64"
    vagrant.vm.network "forwarded_port", guest: 80, host: 8080
    vagrant.vm.network "forwarded_port", guest: 443, host: 8443
  end
  config.vm.define "vagrant2" do |vagrant|
    vagrant.vm.box = "ubuntu/trusty64"
    vagrant.vm.network "forwarded_port", guest: 80, host: 8081
    vagrant.vm.network "forwarded_port", guest: 443, host: 8444
  end

  config.vm.define "vagrant3" do |vagrant|
    vagrant.vm.box = "ubuntu/trusty64"
    vagrant.vm.network "forwarded_port", guest: 80, host: 8082
    vagrant.vm.network "forwarded_port", guest: 443, host: 8445
  end

end
