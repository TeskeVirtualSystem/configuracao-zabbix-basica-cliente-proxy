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

```bash
sudo apt-get install zabbix-proxy-sqlite3
```

Após a instalação, a primeira coisa que devemos fazer é criar o banco de dados SQLite para o Proxy. A documentação do Debian sugere criar o banco de dados em `/var/lib/zabbix/zabbix.db` e é isso que vamos fazer.

```bash
zcat /usr/share/zabbix-proxy-sqlite3/schema.sql.gz | sqlite3 /var/lib/zabbix/zabbix.db
chown zabbix:zabbix /var/lib/zabbix/zabbix.db
```

Feito isso, o banco de dados estará criado e com as permissões corretas para o Proxy. Agora vamos aos arquivos de configuração. O primeiro arquivo a editar é o `/etc/zabbix/zabbix_proxy.conf` e vamos editar as seguintes linhas:

```
Server=IP Do Seu Servidor Zabbix
Hostname=NomeDoSeuZabbixProxy
DBName=/var/lib/zabbix/zabbix.db
StartPingers=5
StartDiscoverers=5
```

Após isso, caso deseja usar rastreio SNMP (para antenas Ubiquiti, Câmeras ou outros dispositivos) instale o SNMP:

```bash
sudo apt-get install snmp snmp-mibs-downloader
sed -i 's/mibs :/#mibs :/g' /etc/snmp/snmp.conf
```

Vamos agora para configuração do Proxy no servidor Zabbix!