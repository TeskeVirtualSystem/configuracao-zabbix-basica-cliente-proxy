# Rodando Proxy e configurando agente local

Feitas as configurações por parte do proxy, estamos prontos para iniciá-lo! Para fazer isso, reinicie o serviço `zabbix-proxy`:

```bash
sudo /etc/init.d/zabbix-proxy restart
```

Feito isso, verifique se está tudo certo vendo o arquivo `/var/log/zabbix-proxy/zabbix-proxy.log`

```
# cat /var/log/zabbix-proxy/zabbix_proxy.log 
 16012:20151025:025711.065 Starting Zabbix Proxy (active) [SeuProxy]. 
 Zabbix 2.2.2 (revision 42525).
 16012:20151025:025711.065 **** Enabled features ****
 16012:20151025:025711.065 SNMP monitoring:       YES
 16012:20151025:025711.065 IPMI monitoring:       YES
 16012:20151025:025711.065 WEB monitoring:        YES
 16012:20151025:025711.065 VMware monitoring:     YES
 16012:20151025:025711.065 ODBC:                  YES
 16012:20151025:025711.065 SSH2 support:          YES
 16012:20151025:025711.065 IPv6 support:          YES
 16012:20151025:025711.065 **************************
 16012:20151025:025711.065 using configuration file: /etc/zabbix/zabbix_proxy.conf
 16012:20151025:025711.073 current database version (mandatory/optional): 
 02020000/02020000
 16012:20151025:025711.073 required mandatory version: 02020000
 16015:20151025:025711.080 proxy #1 started [configuration syncer #1]
 16016:20151025:025711.080 proxy #2 started [heartbeat sender #1]
 16017:20151025:025711.080 proxy #3 started [data sender #1]
 16026:20151025:025711.083 proxy #12 started [trapper #3]
 16025:20151025:025711.083 proxy #11 started [trapper #2]
 16027:20151025:025711.083 proxy #13 started [trapper #4]
 16024:20151025:025711.084 proxy #10 started [trapper #1]
 16028:20151025:025711.086 proxy #14 started [trapper #5]
 16012:20151025:025711.090 proxy #0 started [main process]
 16041:20151025:025711.090 proxy #27 started [history syncer #1]
 16033:20151025:025711.090 proxy #19 started [icmp pinger #5]
 16031:20151025:025711.090 proxy #17 started [icmp pinger #3]
 16030:20151025:025711.090 proxy #16 started [icmp pinger #2]
 16045:20151025:025711.090 proxy #31 started [self-monitoring #1]
 16032:20151025:025711.090 proxy #18 started [icmp pinger #4]
 16034:20151025:025711.090 proxy #20 started [housekeeper #1]
 16029:20151025:025711.090 proxy #15 started [icmp pinger #1]
 16034:20151025:025711.090 executing housekeeper
 16035:20151025:025711.090 proxy #21 started [http poller #1]
 16042:20151025:025711.091 proxy #28 started [history syncer #2]
 16043:20151025:025711.091 proxy #29 started [history syncer #3]
 16044:20151025:025711.092 proxy #30 started [history syncer #4]
 16020:20151025:025711.104 proxy #6 started [poller #3]
 16023:20151025:025711.106 proxy #9 started [unreachable poller #1]
 16022:20151025:025711.112 proxy #8 started [poller #5]
 16021:20151025:025711.113 proxy #7 started [poller #4]
 16019:20151025:025711.114 proxy #5 started [poller #2]
 16038:20151025:025711.117 proxy #24 started [discoverer #3]
 16037:20151025:025711.120 proxy #23 started [discoverer #2]
 16018:20151025:025711.121 proxy #4 started [poller #1]
 16040:20151025:025711.122 proxy #26 started [discoverer #5]
 16039:20151025:025711.122 proxy #25 started [discoverer #4]
 16036:20151025:025711.123 proxy #22 started [discoverer #1]
 16034:20151025:025711.227 housekeeper [deleted 0 records in 0.005017 sec, idle 3600 sec]
 16015:20151025:025712.216 Received configuration data from server. Datalen 2594
 ```
 
 Se não houverem erros, você já pode configurar o agente local como em [Configurando Cliente Linux](configuring_client_linux/README.md)