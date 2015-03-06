#设定主从同步
* master:
````
#Master start  
#日志输出地址 主要同步使用    
log-bin=master-bin.log  
#同步数据库  
binlog-do-db=test  
#主机id 不能和从机id重复  
server-id=1  
#Master end
````
