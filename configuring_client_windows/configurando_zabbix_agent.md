# Configurando Agente Zabbix

Para configurar o Zabbix Agent vamos abrir o arquivo `C:\zabbix\conf\zabbix_agentd.win.conf` e editar as seguintes linhas:

```
Server={IP DO SEU SERVIDOR/PROXY}
ServerActive={IP DO SEU SERVIDOR/PROXY}
Hostname={NOME DO HOST CRIADO NO ZABBIX}
```

![Edição do Server](../images/zabbix1.png)
![Edição do ServerActive](../images/zabbix2.png)
![Edição do Hostname](../images/zabbix3.png)

Certifique-se de que os endereços para o Servidor / Proxy estão corretos e que o nome do Hostname bate com o criado no servidor Zabbix.