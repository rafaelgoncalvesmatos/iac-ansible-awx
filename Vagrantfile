API_VERSAO = "2"
BOX_NOME = "centos/7"
BOX_IP = "192.168.56.10"
DOMAIN = "pensandoemlinux.com"
CHAVE_PRIVADA = "~/.ssh/id_rsa"
CHAVE_PUBLICA = "~/.ssh/id_rsa.pub"

Vagrant.configure[API_VERSAO] do |config|
    config.vm.box = BOX_NOME
    config.vm.network "private_network", BOX_IP
    config.vm.host_name = BOX_IP + '.' + DOMAIN
    config.ssh.insert_key = false
    config.ssh.private_key = [CHAVE_PRIVADA, "~/.vagrant.d/insecure_private_key"]
    config.vm.provision "file", source: CHAVE_PUBLICA, destination: "~/.ssh/authorized_keys"

    config.vm.provider "virtualbox" do |v|
        v.memory = "2024"
        v.cpus = "2"
    end

    config.vm.provider "vmware_fusion" do |v|
        v.vmx["memsize"] = "2024"
        v.vmx["numvcpus"] = "2"
    end
end