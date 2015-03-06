#设定主从同步
* **Master**:
````
#Master start  
#日志输出地址 主要同步使用    
log-bin=master-bin.log  
#同步数据库  
binlog-do-db=atlas  
#主机id 不能和从机id重复  
server-id=1  
#Master end
````  
master的配置比较少，server-id是为这一组master/slave服务器定的唯一id，master/slave服务器中不能重复。在binlog-do-db中填写对象要同步的数据库，如果有多个，用逗号分隔，或再写一行如binlog-do-db=test2。  
* **Slave**
````
report-host = 10.50.147.145  
report-user = root  
report-password = 123456   
log-bin = slave-bin.log  
replicate-do-db = atlas  
server-id = 2
````  
The server is not configured as slave; fix in config file or with CHANGE MASTER TO

可以通过下面语句解决：
````
change master to master_host='10.50.147.145',master_user='root',master_password='123456',master_log_file='master-bin.000001' ,master_log_pos=120;
````
