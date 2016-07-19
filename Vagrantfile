# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true

  config.vm.define "webserver01" do |webserver01|
      webserver01.vm.box = "geerlingguy/centos7"
      webserver01.vm.hostname = "webserver01"
      webserver01.vm.network "private_network", ip: "192.168.10.10"
      webserver01.hostmanager.aliases = %w(webserver01.fisl17)
      webserver01.vm.synced_folder ".", "/vagrant", disabled: true
  end

  config.vm.define "webserver02" do |webserver02|
      webserver02.vm.box = "geerlingguy/centos7"
      webserver02.vm.hostname = "webserver02"
      webserver02.vm.network "private_network", ip: "192.168.10.11"
      webserver02.hostmanager.aliases = %w(webserver02.fisl17)
      webserver02.vm.synced_folder ".", "/vagrant", disabled: true
  end

  config.vm.define "webserver03" do |webserver03|
      webserver03.vm.box = "geerlingguy/centos7"
      webserver03.vm.hostname = "webserver03"
      webserver03.vm.network "private_network", ip: "192.168.10.12"
      webserver03.hostmanager.aliases = %w(webserver03.fisl17)
      webserver03.vm.synced_folder ".", "/vagrant", disabled: true
  end

  config.vm.define "load" do |load|
      load.vm.box = "geerlingguy/centos7"
      load.vm.hostname = "load"
      load.vm.network "private_network", ip: "192.168.10.100"
      load.hostmanager.aliases = %w(load.fisl17)
      load.vm.synced_folder ".", "/vagrant", disabled: true
  end

end
