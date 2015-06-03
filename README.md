# Atlas-research
本项目旨在帮助正在research Atlas或者在使用Atlas中遇到问题的人。  
同时也希望大家能将自己遇到的问题和解决办法push到项目中。  
push方法，fork这个项目。在question文件夹中加入你的md。  
然后在首页的md的[Question](#question)中加入你的问题，然后push你的文件。  
请在md第一行加上您的个人信息。让大家记住你的贡献。
````
 首页加入链接的方法
 [your question name](your question href) //href 使用相对路径 like question/xx.md
 
 md加入个人信息
 ####author piggsoft@163.com
 ####date 2015-04-29
 ####atlas version
````
#Atlas 介绍
Atlas是由 Qihoo 360, Web平台部基础架构团队开发维护的一个基于MySQL协议的数据中间层项目。它是在mysql-proxy 0.8.2版本的基础上，对其进行了优化，增加了一些新的功能特性。360内部使用Atlas运行的mysql业务，每天承载的读写请求数达几十亿条。  
####Atlas sharding####
[Atlas sharding](sharding/readme.md)看这里

#github 地址
[Atlas GitHub](https://github.com/Qihoo360/Atlas)  
[Rlease 包](https://github.com/Qihoo360/Atlas/releases)
#资料文档
[mysql中间件研究（Atlas，cobar，TDDL）](http://www.guokr.com/blog/475765/)  
[Atlas 中文手册](https://github.com/Qihoo360/Atlas/blob/master/README_ZH.md)  
[一步一步安装Atlas](http://leboit.blog.51cto.com/blog/1465210/1582835)

#部分设定 
 [环境设定](https://github.com/piggsoft/Atlas-research/tree/master/setup)  
 [MySQL主从设定](https://github.com/piggsoft/Atlas-research/tree/master/config)  

###查阅网站
[Markdown 语法说明](http://wowubuntu.com/markdown/)  
[Atlas的安装](https://github.com/Qihoo360/Atlas/wiki/Atlas%E7%9A%84%E5%AE%89%E8%A3%85)  
[Atlas的架构](https://github.com/Qihoo360/Atlas/wiki/Atlas%E7%9A%84%E6%9E%B6%E6%9E%84)

#Question
* [ERROR 2006 (HY000): MySQL server has gone away](question/01.md)
* [一主三从，其中某个从的连接数非常多，是怎么回事](https://github.com/Qihoo360/Atlas/issues/22)
* [That had some errors in Mac Air compiled the Atlas from source code](https://github.com/Qihoo360/Atlas/issues/19)
* [字符集的问题](https://github.com/Qihoo360/Atlas/issues/3)
* [Atlas是不支持prepare statement吗](https://github.com/Qihoo360/Atlas/issues/26)
