##下载或更新依赖包##
````shell
yum update openssl
````
##生成密码##
````shell
/usr/local/mysql-proxy/bin/encrypt 123456
````
##将密码加入到配置文件中##
````shell
vi /usr/local/mysql-proxy/conf/test.cnf
````
![修改之后](https://raw.githubusercontent.com/piggsoft/Atlas-reseach/master/res/1.png)
