Multi Instance Redis Discovery Template for Zabbix
======

Requirements
------
Zabbix server must be >= 3.4 And Tested on CentOS 6    
Put the 'userparameter_redis_lld_plus.conf' into $UserParameter's directory.    
On the zabbix server web page import XML template file.    
If password auth is set, Need change the host macro `{$REDIS_PW}`. If there is no password required, use any non-empty string.    
Needs commands: telnet ss (grep awk sed tr)    
> Because redis has different startup users , Here  zabbix-agent use root to run.    
> Trigger "Redis {#REDIS_PORT} latest fork time is too long" Default not enable.    
> Trigger "Redis {#REDIS_PORT} mem fragmentation ratio Too high" Default not enable.     
> "Redis {#REDIS_PORT} Port Net traffic"  Graphs need redis server >= 2.8    

Features
------
* Discovering redis instances and who is slave through ports
* Get redis info/config/slaveinfo and output json format
* Create "Dependent Item" by "preprocessing"
* Generate graphs and Key indicators trigger
    
Charts
------
![Example graphs](https://github.com/cuimingkun/zbx_tem_redis/blob/master/graphs.png)

