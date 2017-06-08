$mach_quant = 3

Vagrant.configure("2") do |config|
 
  config.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.memory=256
      vb.cpus=1
      vb.check_guest_additions=false
  config.vm.box_check_update=false
  config.vm.box="ubuntu/trusty64"
 end

(1..$mach_quant).each do |i|
    config.vm.define "node#{i}" do |node|
        node.vm.network "public_network", ip: "192.168.1.#{25+i}"
        node.vm.hostname = "node#{i}"
    end
end
  
end 