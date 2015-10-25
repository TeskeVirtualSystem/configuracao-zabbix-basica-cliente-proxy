# Instalando Proxy Zabbix

Nesta parte irei usar o `Ubuntu 14.04` como base, porém o procedimento será similar para qualquer distribuição Linux.

Procurando por `zabbix-proxy` no `apt-cache` vemos que há três opções de zabbix proxy:

```
# apt-cache search zabbix-proxy
zabbix-proxy-mysql - network monitoring solution - proxy (using MySQL)
zabbix-proxy-pgsql - network monitoring solution - proxy (using PostgreSQL)
zabbix-proxy-sqlite3 - network monitoring solution - proxy (using SQLite3)
```

Eu irei usar a versão que usa o SQLite como banco de dados pelo fato de ser mais rápido e prático para se configurar.