# Before using the vagrantfile, you need to add the relevant boxes or check if you have them on your system
# To see a list of boxes on your system, type " vagrant global-config "
# To add the Precise box: vagrant box add hashicorp/precise64
# To add the trusty box: vagrant box add ubuntu/trusty64
# To add the puphpet box: vragrant box add puphpet/ubuntu1404-x64
#
# Note: If you use the vagrantfil as it is, YOU WILL GET ERROR MESSAGES.
# HINTS: There are errors on line 12, 25 and 37.
# Good luck and waiting to hear your comments.

Vagrant.configure("2") do |config|

	config.vm.define "Precise64" do |Precise64|
		precise.vm.box = "hashicorp/precise64"
		config.vm.box_url="https://vagrantcloud.com/hashicorp/precise64"
		precise.vm.network :forwarded_port , guest: 22, host: 10222, id: "ssh"
		precise.vm.network :private_network , ip: "192.168.56.102"
		precise.vm.provider :virtualbox do |v|
		v.customize ["modifyvm", :id, "--memory", 512]
		end
	end
	
	config.vm.define "trusty" do |trusty|
		trusty.vm.box = "ubuntu/trusty64"
		config.vm.box_url="https://vagrantcloud.com/ubuntu/trusty64"
		trusty.vm.network :forwarded_port , guest: 22, host: 10222, id: "ssh"
		trusty.vm.network :private_network , ip: "192.168.56.103"
		trusty.vm.provider :virtualbox do |v|
		v.customize ["modifyvm", :id, "--memory", 512]
		end
	end
	
	config.vm.define "puphpet" do |puphpet|
		puphpet.vm.box = "puphpet/ubuntu1404-x64"
		config.vm.box_url="https://vagrantcloud.com/puphpet/ubuntu1404-x64"
		puphpet.vm.network :forwarded_port , guest: 22, host: 10226, id: "ssh"
		puphpet.vm.network :private_network , ip: "192.168.56.104"
		puphpet.vm.provider :virtualbox do |vb|
		v.customize ["modifyvm", :id, "--memory", 512]
		end
	end
	
end
