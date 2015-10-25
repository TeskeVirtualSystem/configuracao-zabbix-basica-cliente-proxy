# Instalando Agente Zabbix

Vamos começar instalando o Agente Zabbix usando o `apt-get`:

```bash
sudo apt-get install zabbix-agent
```

Instalado o agente Zabbix, vamos editar o seu arquivo de configuração em `/etc/zabbix/zabbix_agent.conf`:

```
Server=IP Do Seu Servidor / Proxy
ServerActive=IP Do Seu Servidor / Proxy
Hostname=Nome do Host
```

Feito isso, basta reiniciar o processo `zabbix-agent`:

```bash
sudo /etc/init.d/zabbix-agent restart
```

Verifique o log `/var/log/zabbix-agent/zabbix_agentd.log` para ver se está tudo OK:

```
# cat /var/log/zabbix-agent/zabbix_agentd.log 
 22135:20151025:031456.368 Starting Zabbix Agent [Seu Host]. Zabbix 2.2.2 (revision 42525).
 22135:20151025:031456.369 using configuration file: /etc/zabbix/zabbix_agentd.conf
 22136:20151025:031456.369 agent #0 started [collector]
 22137:20151025:031456.370 agent #1 started [listener #1]
 22139:20151025:031456.370 agent #2 started [listener #2]
 22140:20151025:031456.370 agent #3 started [listener #3]
 22141:20151025:031456.370 agent #4 started [active checks #1]
 22142:20151025:031456.371 agent #5 started [active checks #2]
```