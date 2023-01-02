# Playbook Ansible para configuração Local

Este playbook foi testado nas versões:

Ubuntu 20.04 </br>
Ansible: 2.9

Para execução em outras versões pode ser necessário a  alteração dos nomes dos pacotes.

Link para a Documentação do Ansible https://docs.ansible.com/ansible/latest/index.html
Playbooks Ansible

O diretório principal ansible-main contém dois arquivos hosts e local.yml.</br>
 `hosts` - onde o Ansible consulta para saber em qual dispositivo deverá executar as ações. </br>
 `local.yml` - onde é especificado quais conjuntos de regras serão executadas </br>

O diretório `local-rules` contém mais diretórios.</br>
  `tasks` - onde estão as instruções que o Ansible deve seguir. </br>
  `vars` - onde estão as variáveis que o Ansible irá buscar na execução dos Playbooks. </br>
  `handlers` - onde estão as instruções para manipular os serviços, exemplo restart quando houver alterações nos arquivos de configuração. </br>
  `files` - onde estão os os arquivos de configuração, por exemplo arquivos .conf. </br>
Comando para execução de todo o conjunto de playbook. </br>
ansible-playbook -i hosts local.yml -vvv </br>
Pode ser necessário executar o comando com privilégios de super-usuário utilizando o comando sudo. </br>

