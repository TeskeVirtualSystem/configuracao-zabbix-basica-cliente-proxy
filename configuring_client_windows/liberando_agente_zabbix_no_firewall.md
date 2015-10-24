# Liberando Agente Zabbix no Firewall

Para rodar o Agente Zabbix, temos de liberar 3 processos no Firewall do Windows:

*   zabbix_agentd.exe
*   zabbix_sender.exe
*   zabbix_get.exe

Para isso, abra o menu iniciar e procure por `Firewall do Windows` e abra-o. Vá até `Regras de Entrada` e clique em `Nova Regra`

![Regras de Entrada](../images/zabbix6.png)

![Nova Regra](../images/zabbix7.png)

Na primeira página, selecione `Programa` e clique em `Avançar >`

![Primeira Página](../images/zabbix8.png)

Na segunda página selecione `Este caminho para o programa` e vá até `C:\zabbix\bin\win64\` e selecione `zabbix_agentd.exe`. Clique em `Avançar >`

![Segunda Página](../images/zabbix9.png)

Na terceira página, selecione `Permitir a conexão` e clique em `Avançar >`

![Terceira Página](../images/zabbix10.png)

Na quarta página, selecione todas as opções e clique em `Avançar >`

![Regras de Entrada](../images/zabbix11.png)

Na última página, coloque como nome `Zabbix Agent` e clique em `Concluir`.

![Regras de Entrada](../images/zabbix12.png)

Repita os passos para `zabbix_get.exe` e `zabbix_sender.exe`