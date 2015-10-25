# Primeiros passos

Antes de mais nada, certifique-se de ter criado um host no servidor Zabbix como descrito em [Configurando Host no Zabbix]()

O primeiro passo para configuração do Agente Zabbix em uma máquina Windows é baixar a versão mais recente do Zabbix Agent no site oficial do Zabbix: http://www.zabbix.com/download.php .
O agente para se baixar está na seção `Zabbix pre-compiled agents`.

Para auxiliar no processo de edição do arquivo de configuração, baixe também o Notepad++ em https://notepad-plus-plus.org/

Feito isso, instale o Notepad++ e extraia o Agente Zabbix no diretório `C:\zabbix`. No processo de extração deve ser criada a seguinte estrutura:

*   C:\zabbix
    *   bin
        *   win32
            *   dev
                *   zabbix_sender.dll
                *   zabbix_sender.lib
            *   zabbix_agentd.exe
            *   zabbix_get.exe
            *   zabbix_sender.exe
        *   win64
            *   dev
                *   zabbix_sender.dll
                *   zabbix_sender.lib
            *   zabbix_agentd.exe
            *   zabbix_get.exe
            *   zabbix_sender.exe
    *   conf
        *   zabbix_agentd.win.conf

Feito isso estamos prontos para seguir para os próximos passos!