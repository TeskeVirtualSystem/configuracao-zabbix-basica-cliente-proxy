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

