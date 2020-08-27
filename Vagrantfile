Vagrant.configure("2") do |config|
    config.vm.box = "generic/debian10"

    config.vm.provider "virtualbox" do |vb|
        vb.memory = "2048"
        vb.cpus = "1"
    end

    config.vm.provision "ansible" do |ansible|
        ansible.become = true
        ansible.verbose = "v"
        ansible.playbook = "webserver.yml"
        ansible.extra_vars = {
          chronograph_jar: "./chronograph.jar",
          chronograph_config: "./config.edn"
        }
    end
end
