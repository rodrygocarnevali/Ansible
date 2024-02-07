# Ansible Main Configuration

Este repositório contém a configuração principal do Ansible para automatizar tarefas de configuração em hosts locais.

## Estrutura do Projeto

### 1. `.gitattributes`

Este arquivo configura as preferências do Git para lidar com quebras de linha em arquivos de texto.

### 2. `hosts`

O arquivo de inventário do Ansible, definindo hosts e variáveis globais.

### 3. `local.yml`

O playbook principal do Ansible que executa a role `myroles` em todos os hosts.

### 4. `Readme.md`

Este arquivo de documentação contém informações detalhadas sobre o propósito do programa e a estrutura do projeto.

### 5. `myroles/handlers/main.yml`

Define handlers do Ansible que reiniciam serviços como logrotate e systemd-journald.

### 6. `myroles/tasks/conf_log.yml`

Configura tarefas relacionadas a logs, incluindo a localização e ajuste de arquivos logrotate.d e configuração do systemd-journald.

### 7. `myroles/tasks/conf_prog.yml`

Configura tarefas para instalar programas específicos usando o módulo `apt` e inicia serviços como Apache e MySQL.

### 8. `myroles/tasks/main.yml`

Arquivo principal da role `myroles` que importa tarefas específicas de instalação de programas e configuração de logs.

### 9. `myroles/vars/main.yml`

Define variáveis utilizadas nas tarefas, como a lista de programas a serem instalados.

## Como Usar

1. Certifique-se de ter o Ansible instalado em seu sistema.
2. Clone este repositório em sua máquina local.
3. Personalize o arquivo `hosts` conforme necessário.
4. Execute o playbook principal com o comando `ansible-playbook local.yml`.

## Contribuições

Contribuições são bem-vindas! Se encontrar problemas ou tiver sugestões, sinta-se à vontade para abrir uma issue ou enviar um pull request.
