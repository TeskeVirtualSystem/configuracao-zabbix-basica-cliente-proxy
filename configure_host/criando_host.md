# Criando Host

O primeiro passo para se criar o host é ir no `Menu Superior` -> `Configurações` e clicar em `Hosts`.

![Hosts](../images/zabbix_hostconfig.png)

Feito isso, uma lista de hosts criados irá aparecer. No canto superior direito há um botão ![Criar Host](../images/zabbix_createhost.png)

Neste tela, preencha os campos da seguinte maneira:

| Campo | Descrição | Exemplo |
|-------|-----------|---------|
|Nome do Host| Este é o nome que será especificado no arquivo de configuração do agente. Ele deverá ser único. | minha-nova-maquina |
|Nome visível| Este é o nome que irá aparecer nos relatórios e em qualquer seção do Zabbix. Use um nome fácil de reconhecer.| Minha nova máquina |
| Grupos | Aqui você poderá selecionar grupos existentes para associar este host. Use para organizar. | Clientes |
| Interfaces do Agente: IP| Este é o endereço de IP da máquina alvo. Ele precisa ser um IP acessível pela internet ou acessível pelo Proxy | 10.0.5.1 |
|Monitorado por Proxy| Selecione aqui o Proxy que irá monitorar a máquina caso ela não esteja direto ná internet. | Proxy do Cliente |

![Configurações do Host](../images/zabbix_createhost2.png)

Feito isso, clique no menu logo abaixo de `Configuração de Hosts` na opção `Templates`. Aqui selecionaremos os templates a serem usados para este host.

Escreva uma parte do nome do template no campo `Vincular a novos templates`. Por exemplo se a máquina for Linux, escreva `Linux`. Um popup deve aparecer com a lista de templates que tenham a palavra pesquisada.

![Templates](../images/zabbix_createhost3.png)

Clique no template desejado e ele ficará marcado. Após isso clique em adicionar.

![Template Linux](../images/zabbix_createhost4.png)

![Template Linux](../images/zabbix_createhost5.png)

Feito isso o(s) template(s) estarão associados ao host que será criado.

Esses templates definirão os dados a serem coletados do host.

Após terminar as configurações clique em ![Salvar](../images/zabbix_save.png)