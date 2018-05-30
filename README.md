# Multi Instance Redis Discovery Template for Zabbix 3.4
------
Zabbix server must be >= 3.4 br
Put the 'userparameter_redis_lld_plus.conf' into $UserParameter's directory. br
On the zabbix server web page import XML template file. br
Need command: telnet and redis-cli br

> * Discovering redis instances and who is slave through ports
> * Get redis info/config/slaveinfo and output json format
> * Create "Dependent Item" by "preprocessing"
> * Generate graphs and Key indicators trigger
