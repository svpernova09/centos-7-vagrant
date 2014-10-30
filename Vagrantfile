# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

path = "#{File.dirname(__FILE__)}"

require 'yaml'
require path + '/scripts/centos.rb'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  Centos.configure(config, YAML::load(File.read(path + '/Centos.yaml')))

  config.vm.provision "shell", path: "scripts/customize.sh"
end

