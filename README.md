#### 1、安装依赖库 yum -y install snappy snappy-devel zlib zlib-devel bzip2 bzip2-devel lz4 lz4-devel zstd

#### 2、解压 rocksredis_centos7_x86_64.tar.gz 拷贝rocksredis_centos7_x86_64.tar.gz 到目标机器 /opt/ 解压 tar -zxvf rocksredis_centos7_x86_64.tar.gz
[百度网盘下载](https://pan.baidu.com/s/1njZUdAQ6jm8ABbxWkanh1g)    
提取码： **6w8e**  

#### 3、配置 rocksdb相关，redis.conf文件中修改

```
# rocksdb 的 data 路径
rocksredis_db_select 15

# redis 持久化 db
rocksredis_db_dir  /home/data
```



#### 4、启动执行脚本

```
./runstart.sh
```

![运行](https://images.gitee.com/uploads/images/2021/0506/141251_64f8e766_1205442.png)

#### 5、Rocksredis 完全兼容redis的驱动和操作方式，rocksredis支持的操作指令，

| num  | command                                                      |
| ---- | ------------------------------------------------------------ |
| 1    | [HDEL key field1 field2] 删除一个或多个哈希表字段            |
| 2    | HEXISTS key field 查看哈希表 key 中，指定的字段是否存在。    |
| 3    | HGET key field 获取存储在哈希表中指定字段的值。              |
| 4    | HGETALL key 获取在哈希表中指定 key 的所有字段和值            |
| 5    | HKEYS key 获取所有哈希表中的字段                             |
| 6    | HLEN key 获取哈希表中字段的数量                              |
| 7    | [HMGET key field1 field2] 获取所有给定字段的值               |
| 8    | [HMSET key field1 value1 field2 value2 ] 同时将多个 field-value (域-值)对设置到哈希表 key 中。 |
| 9    | HSET key field value 将哈希表 key 中的字段 field 的值设为 value 。 |
| 10   | HSETNX key field value 只有在字段 field 不存在时，设置哈希表字段的值。 |
| 11   | HVALS key 获取哈希表中所有值。                               |
| 12   | HSCAN key cursor [MATCH pattern] [COUNT count] 迭代哈希表中的键值对。 |
| 13   | DEL 命令用于删除已存在的键                                   |
| 14   | Strlen 命令用于获取指定 key 所储存的字符串值的长度           |
| 15   | Scan 命令用于迭代数据库中的数据库键                          |
| 16   | Type 命令用于返回 key 所储存的值的类型                       |
| 17   | Sadd 命令将一个或多个成员元素加入到集合中，已经存在于集合的成员元素将被忽略 |
| 18   | Scard 命令返回集合中元素的数量                               |
| 19   | Sismember 命令判断成员元素是否是集合的成员                   |
| 20   | Smembers 命令返回集合中的所有的成员。 不存在的集合 key 被视为空集合 |
| 21   | Spop 命令用于移除集合中的指定 key 的一个或多个随机元素，移除后会返回移除的元素 |
| 22   | Sscan 命令用于迭代集合中键的元素                             |
| 23   | Srem 命令用于移除集合中的一个或多个成员元素                  |
| 24   | SET 命令用于设置给定 key 的值。如果 key 已经存储其他值， SET 就覆写旧值，且无视类型 |
| 25   | Get 命令用于获取指定 key 的值。如果 key 不存在，返回 nil 。如果key 储存的值不是字符串类型，返回一个错误 |



#### 6、下载

gitee

- [centos7 64bit server](https://gitee.com/RocksCloud/rocksredis_centos7_x86_64)



github

- [centos7 64bit server](https://github.com/RocksCloud/rocksredis_centos7_x86_64)


