# -*- mode: ruby -*-
Vagrant.configure("2") do |config|
 config.vm.define "web", primary: true do |web|
  web.omnibus.chef_version = :latest
  web.vm.box ="ubuntu/trusty64"
  web.vm.network "forwarded_port", guest:80, host:8080
  web.vm.provision "chef_solo" do |chef|
    chef.add_recipe "testweb-0.1.0"
 end
 end
end
