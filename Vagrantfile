Vagrant.configure("2") do |config|
    config.vm.box = "precise64"
    config.vm.box_url = "http://files.vagrantup.com/precise64.box"

    config.vm.synced_folder "~/webapp", "/opt/webapp"
    config.vm.network :private_network, ip: "192.168.130.10"

    ## Use all the defaults:
    config.vm.provision :ansible do |ansible|
        ansible.playbook = "site.yml"
        ansible.inventory_file = "hosts.yml"
        ansible.verbose = true
        #ansible.ask_sudo_pass = true
    end
end
