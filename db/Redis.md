# Redis介绍
## 简介
  - Redis 是一款开源的,基于BSD许可的,**单线程模式**,高级键值(key-value)缓存(cache)和存储(store)系统
## 官网
  - [https://redis.io/](https://redis.io/)
## GitHub源码
   - [https://github.com/antirez/redis](https://github.com/antirez/redis)
## 客户端推荐
- [Redis Desktop Manager](https://redisdesktop.com/) *强烈推荐*
- [FastoRedis ](<https://fastoredis.com/>)  ***分收费与付费两种***



# 学习
- 视频讲解资料
- 数据结构
- 部署方式
- 持久化方式
   - ***RDB:***在指定的时间间隔内生成数据集的时间点快照(point-in-time snapshot).安全性较差、尺寸小、速度快;适用于备份和灾难恢复。
   - ***AOF***持久化记录服务器执行的所有写操作命令，并在服务器启动时，通过重新执行这些命令来还原数据集。

      
      
      
## Redis常用命令

|Redis命令|具体功能|参考|
|----------|---------|----------|
|select|Select the Redis logical database having the specified zero-based numeric index. New connections always use the database 0|https://redis.io/commands/select|
|auth|Request for authentication in a password-protected Redis server|https://redis.io/commands/auth|




## 部署
#### docker部署




## 问题解决

- [redis启动出错Creating Server TCP listening socket 127.0.0.1:6379: bind: No error](<https://www.cnblogs.com/shaosks/p/7089786.html>)

