VAGRANT_DISABLE_VBOXSYMLINKCREATE=1

Vagrant.configure("2") do |config|
    (1..2).each do |i|
        config.vm.define "debian#{i}" do |v|
            v.vm.box = "debian/bullseye64"
            v.vm.hostname = "vm#{i}"
            v.vm.box_version = "11.20220328.1"
            v.vm.provision "shell", path: 'script.sh'

            v.vm.provider :virtualbox do |vm|
                vm.name = "debian#{i}"
                vm.memory = 1024
                vm.cpus = 2
            end
        end
    end   
end