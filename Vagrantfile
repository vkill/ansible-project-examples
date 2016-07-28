local_ubuntu_xenial64_box_url = File.expand_path("../xenial-server-cloudimg-amd64-vagrant.box", __FILE__)
if File.exists?(local_ubuntu_xenial64_box_url)
  ubuntu_xenial64_box_url = local_ubuntu_xenial64_box_url
else
  ubuntu_xenial64_box_url = "https://cloud-images.ubuntu.com/xenial/current/xenial-server-cloudimg-amd64-vagrant.box"
end

Vagrant.configure(2) do |config|

  config.vm.define "ubuntu_xenial64" do |os_config|
    os_config.vm.box = "ubuntu/xenial64"
    os_config.vm.box_url = ubuntu_xenial64_box_url

    os_config.vm.network "private_network", ip: "192.168.99.11"

    os_config.vm.provider "virtualbox" do |vb|
    	vb.name = "APE_ubuntu_xenial64"
      vb.gui = false
      vb.memory = "512"
    end

    config.ssh.forward_agent = true

  end
end
