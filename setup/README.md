##下载或更新依赖包##
    yum update openssl
##生成密码##
    /usr/local/mysql-proxy/bin/encrypt 123456
##将密码加入到配置文件中##
    vi /usr/local/mysql-proxy/conf/test.cnf
