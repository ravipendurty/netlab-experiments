VAGRANT_COMMAND = ARGV[0]

Vagrant.configure("2") do |config|
  config.vm.provider :libvirt do |libvirt|
    libvirt.management_network_address = "192.168.121.0/24"
    libvirt.default_prefix = "netlab_again_"
  end
  vm_name = "L1"
  config.vm.define vm_name do |L1|
    L1.vm.provider :libvirt do |domain|
      domain.management_network_mac = "08:4f:a9:00:00:01"
      domain.qemu_use_session = false
    end
    L1.vm.box = "arista/veos"
    L1.vm.synced_folder ".", "/vagrant", id: "vagrant-root", disabled: true
    L1.ssh.insert_key = false
    L1.ssh.shell = "bash"
    L1.vm.guest = :freebsd

    L1.vm.provider :libvirt do |domain|
      domain.disk_bus = 'ide'
      domain.cpus = 2
      domain.memory = 2048
      domain.driver = "kvm"
    end
    L1.vm.provider :libvirt do |domain|
    end

    L1.vm.network :private_network,
                  :libvirt__tunnel_type => "udp",
                  :libvirt__tunnel_local_ip => "127.1.1.1",
                  :libvirt__tunnel_local_port => "10001",
                  :libvirt__tunnel_ip => "127.1.1.4",
                  :libvirt__tunnel_port => "10001",
                  :libvirt__iface_name => "vgif_L1_1",
                  auto_config: false
    L1.vm.network :private_network,
                  :libvirt__tunnel_type => "udp",
                  :libvirt__tunnel_local_ip => "127.1.1.1",
                  :libvirt__tunnel_local_port => "10002",
                  :libvirt__tunnel_ip => "127.1.1.5",
                  :libvirt__tunnel_port => "10001",
                  :libvirt__iface_name => "vgif_L1_2",
                  auto_config: false

  
  end
  vm_name = "L2"
  config.vm.define vm_name do |L2|
    L2.vm.provider :libvirt do |domain|
      domain.management_network_mac = "08:4f:a9:00:00:02"
      domain.qemu_use_session = false
    end
    L2.vm.box = "arista/veos"
    L2.vm.synced_folder ".", "/vagrant", id: "vagrant-root", disabled: true
    L2.ssh.insert_key = false
    L2.ssh.shell = "bash"
    L2.vm.guest = :freebsd

    L2.vm.provider :libvirt do |domain|
      domain.disk_bus = 'ide'
      domain.cpus = 2
      domain.memory = 2048
      domain.driver = "kvm"
    end
    L2.vm.provider :libvirt do |domain|
    end

    L2.vm.network :private_network,
                  :libvirt__tunnel_type => "udp",
                  :libvirt__tunnel_local_ip => "127.1.1.2",
                  :libvirt__tunnel_local_port => "10001",
                  :libvirt__tunnel_ip => "127.1.1.4",
                  :libvirt__tunnel_port => "10002",
                  :libvirt__iface_name => "vgif_L2_1",
                  auto_config: false
    L2.vm.network :private_network,
                  :libvirt__tunnel_type => "udp",
                  :libvirt__tunnel_local_ip => "127.1.1.2",
                  :libvirt__tunnel_local_port => "10002",
                  :libvirt__tunnel_ip => "127.1.1.5",
                  :libvirt__tunnel_port => "10002",
                  :libvirt__iface_name => "vgif_L2_2",
                  auto_config: false

  
  end
  vm_name = "L3"
  config.vm.define vm_name do |L3|
    L3.vm.provider :libvirt do |domain|
      domain.management_network_mac = "08:4f:a9:00:00:03"
      domain.qemu_use_session = false
    end
    L3.vm.box = "arista/veos"
    L3.vm.synced_folder ".", "/vagrant", id: "vagrant-root", disabled: true
    L3.ssh.insert_key = false
    L3.ssh.shell = "bash"
    L3.vm.guest = :freebsd

    L3.vm.provider :libvirt do |domain|
      domain.disk_bus = 'ide'
      domain.cpus = 2
      domain.memory = 2048
      domain.driver = "kvm"
    end
    L3.vm.provider :libvirt do |domain|
    end

    L3.vm.network :private_network,
                  :libvirt__tunnel_type => "udp",
                  :libvirt__tunnel_local_ip => "127.1.1.3",
                  :libvirt__tunnel_local_port => "10001",
                  :libvirt__tunnel_ip => "127.1.1.4",
                  :libvirt__tunnel_port => "10003",
                  :libvirt__iface_name => "vgif_L3_1",
                  auto_config: false
    L3.vm.network :private_network,
                  :libvirt__tunnel_type => "udp",
                  :libvirt__tunnel_local_ip => "127.1.1.3",
                  :libvirt__tunnel_local_port => "10002",
                  :libvirt__tunnel_ip => "127.1.1.5",
                  :libvirt__tunnel_port => "10003",
                  :libvirt__iface_name => "vgif_L3_2",
                  auto_config: false

  
  end
  vm_name = "S1"
  config.vm.define vm_name do |S1|
    S1.vm.provider :libvirt do |domain|
      domain.management_network_mac = "08:4f:a9:00:00:04"
      domain.qemu_use_session = false
    end
    S1.vm.box = "arista/veos"
    S1.vm.synced_folder ".", "/vagrant", id: "vagrant-root", disabled: true
    S1.ssh.insert_key = false
    S1.ssh.shell = "bash"
    S1.vm.guest = :freebsd

    S1.vm.provider :libvirt do |domain|
      domain.disk_bus = 'ide'
      domain.cpus = 2
      domain.memory = 2048
      domain.driver = "kvm"
    end
    S1.vm.provider :libvirt do |domain|
    end

    S1.vm.network :private_network,
                  :libvirt__tunnel_type => "udp",
                  :libvirt__tunnel_local_ip => "127.1.1.4",
                  :libvirt__tunnel_local_port => "10001",
                  :libvirt__tunnel_ip => "127.1.1.1",
                  :libvirt__tunnel_port => "10001",
                  :libvirt__iface_name => "vgif_S1_1",
                  auto_config: false
    S1.vm.network :private_network,
                  :libvirt__tunnel_type => "udp",
                  :libvirt__tunnel_local_ip => "127.1.1.4",
                  :libvirt__tunnel_local_port => "10002",
                  :libvirt__tunnel_ip => "127.1.1.2",
                  :libvirt__tunnel_port => "10001",
                  :libvirt__iface_name => "vgif_S1_2",
                  auto_config: false
    S1.vm.network :private_network,
                  :libvirt__tunnel_type => "udp",
                  :libvirt__tunnel_local_ip => "127.1.1.4",
                  :libvirt__tunnel_local_port => "10003",
                  :libvirt__tunnel_ip => "127.1.1.3",
                  :libvirt__tunnel_port => "10001",
                  :libvirt__iface_name => "vgif_S1_3",
                  auto_config: false

  
  end
  vm_name = "S2"
  config.vm.define vm_name do |S2|
    S2.vm.provider :libvirt do |domain|
      domain.management_network_mac = "08:4f:a9:00:00:05"
      domain.qemu_use_session = false
    end
    S2.vm.box = "arista/veos"
    S2.vm.synced_folder ".", "/vagrant", id: "vagrant-root", disabled: true
    S2.ssh.insert_key = false
    S2.ssh.shell = "bash"
    S2.vm.guest = :freebsd

    S2.vm.provider :libvirt do |domain|
      domain.disk_bus = 'ide'
      domain.cpus = 2
      domain.memory = 2048
      domain.driver = "kvm"
    end
    S2.vm.provider :libvirt do |domain|
    end

    S2.vm.network :private_network,
                  :libvirt__tunnel_type => "udp",
                  :libvirt__tunnel_local_ip => "127.1.1.5",
                  :libvirt__tunnel_local_port => "10001",
                  :libvirt__tunnel_ip => "127.1.1.1",
                  :libvirt__tunnel_port => "10002",
                  :libvirt__iface_name => "vgif_S2_1",
                  auto_config: false
    S2.vm.network :private_network,
                  :libvirt__tunnel_type => "udp",
                  :libvirt__tunnel_local_ip => "127.1.1.5",
                  :libvirt__tunnel_local_port => "10002",
                  :libvirt__tunnel_ip => "127.1.1.2",
                  :libvirt__tunnel_port => "10002",
                  :libvirt__iface_name => "vgif_S2_2",
                  auto_config: false
    S2.vm.network :private_network,
                  :libvirt__tunnel_type => "udp",
                  :libvirt__tunnel_local_ip => "127.1.1.5",
                  :libvirt__tunnel_local_port => "10003",
                  :libvirt__tunnel_ip => "127.1.1.3",
                  :libvirt__tunnel_port => "10002",
                  :libvirt__iface_name => "vgif_S2_3",
                  auto_config: false

  
  end
  vm_name = "H1"
  config.vm.define vm_name do |H1|
    H1.vm.provider :libvirt do |domain|
      domain.management_network_mac = "08:4f:a9:00:00:06"
      domain.qemu_use_session = false
    end
    H1.vm.box = "generic/ubuntu2004"
    H1.vm.synced_folder ".", "/vagrant", id: "vagrant-root", disabled: true

    H1.vm.provider :libvirt do |domain|
      domain.cpus = 1
      domain.memory = 1024
    end
    H1.vm.provider :libvirt do |domain|
    end


  
  end
  vm_name = "H2"
  config.vm.define vm_name do |H2|
    H2.vm.provider :libvirt do |domain|
      domain.management_network_mac = "08:4f:a9:00:00:07"
      domain.qemu_use_session = false
    end
    H2.vm.box = "generic/ubuntu2004"
    H2.vm.synced_folder ".", "/vagrant", id: "vagrant-root", disabled: true

    H2.vm.provider :libvirt do |domain|
      domain.cpus = 1
      domain.memory = 1024
    end
    H2.vm.provider :libvirt do |domain|
    end


  
  end
end
