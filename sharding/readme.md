#Sharding是Atlas的一个分支
这个是分布式版本的Atlas，是接下来重点开发的一个分支（一般人我不告诉他） 
  
Sharding的基本思想就是把一个数据表中的数据切分成多个部分, 存放到不同的主机上去(切分的策略有多种), 从而缓解单台机器的性能跟容量的问题. sharding是一种水平切分, 适用于单表数据庞大的情景. 目前atlas支持静态的sharding方案, 暂时不支持数据的自动迁移以及数据组的动态加入.

Atlas以表为单位sharding, 同一个数据库内可以同时共有sharding的表和不sharding的表, 不sharding的表数据存在未sharding的数据库组中.

目前Atlas sharding支持insert, delete, select, update语句, 只支持不跨shard的事务. 所有的写操作如insert, delete, update只能一次命中一个组, 否则会报"ERROR 1105 (HY000):write operation is only allow to one dbgroup!"错误.

由于sharding取替了Atlas的分表功能, 所以在Sharding分支里面, Atlas单机分表的功能已经移除, 配置tables将不会再有效.

关于垂直切分与水平切分的区别与优缺点, 在这里就不详细解释了.

````javascript
上面这段摘录于官方文档，想要看详细的请戳下面的介绍  
````
[分支地址](https://github.com/Qihoo360/Atlas/tree/sharding)  
[分支安装介绍](https://github.com/Qihoo360/Atlas/wiki/Atlas-Sharding)
