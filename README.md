Ansible AWX

Este repositorio e voltado para construcao do Ansible AWX em qualquer distro padrao Red Hat.

De forma simples e facilitada de forma que todos possam entender e aplicar em sua propria infraestrutura.

Clone o repositorio:

$ git clone https://github.com/rafaelgoncalvesmatos/iac-ansible-awx

Entre no diretorio para execucao:

$ cd iac-ansible-awx

Suba a instancia ( Leie Vagrantfile ):

$ vagrant up 

Execute a automacao, no inventario voce tem que atentar ao ip que esta no inventario:

$ ansible-playbook -i inventory site.yml

O playbook pode ser utilizado no seu host atual ele sendo CentOS.

Obrigado.
