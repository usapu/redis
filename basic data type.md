- string（字符串）
  - string 类型是二进制安全的。意思是 redis 的 string 可以包含任何数据。比如jpg图片或者序列化的对象。
  - string 类型是 Redis 最基本的数据类型，string 类型的值最大能存储 512MB。
- hash（哈希）
  - Redis hash 是一个键值(key=>value)对集合。
  - Redis hash 是一个 string 类型的 field 和 value 的映射表，hash 特别适合用于存储对象。
  - HMSET runoob field1 "Hello" field2 "World"
  - HGET runoob field1
  - HGET runoob field2
- list（列表）
  - Redis 列表是简单的字符串列表，按照插入顺序排序。你可以添加一个元素到列表的头部（左边）或者尾部（右边）。
  - lpush runoob redis
  - lpush runoob mongodb
  - lrange runoob 0 10
- set（集合）
  - 添加一个 string 元素到 key 对应的 set 集合中，成功返回 1，如果元素已经在集合中返回 0。
  - sadd key member
  - sadd runoob redis
  - smembers runoob
- zset(sorted set：有序集合)
  - Redis zset 和 set 一样也是string类型元素的集合,且不允许重复的成员。
  - 不同的是每个元素都会关联一个double类型的分数。redis正是通过分数来为集合中的成员进行从小到大的排序。zset的成员是唯一的,但分数(score)却可以重复。
  - zadd key score member 
  - ZRANGEBYSCORE runoob 0 1000