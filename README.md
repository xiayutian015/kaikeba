# kaikeba
开课吧架构师课程笔记

## 引流课

### 高并发性能优化&压力测试

#### 概念

+ 并发

  根据`时间片轮转算法`，单个cpu在1个周期内，有几个程序在同时进行，就叫有几个并发

+ 并行

  在同一时刻，多个任务确实在同时进行（多核CPU）

#### 高并发

+ 如果要想系统能够适应高并发状态，则需要从各个方面进行系统优化，包括，硬件、网络、系统架构、开 发语言的选取、数据结构的运用、算法优化、数据库优化……而多线程只是其中解决方法之一。 
+ 其实大部分业务场景不存在并发竞争数据的情况，那么加服务 加机器 基本上都能解决问题，你要事务压力大 那就分表，要是查询压力大 就主从 + 缓存
+ 实现高并发需要考虑： 
  + 系统的架构设计，如何在架构层面减少不必要的处理（网络请求，数据库操作等）例如：使用Cache 来减少IO次数，使用异步来增加单服务吞吐量，使用无锁数据结构来减少响应时间； 
  + 网络拓扑优化减少网络请求时间、如何设计拓扑结构，分布式如何实现？ 
  + 系统代码级别的代码优化，使用什么设计模式来进行工作？哪些类需要使用单例，哪些需要尽量减少 new操作？ 
  + 提高代码层面的运行效率、如何选取合适的数据结构进行数据存取？如何设计合适的算法？ 
  + 任务执行方式级别的同异步操作，在哪里使用同步，哪里使用异步？ 
  + JVM调优，如何设置Heap、Stack、Eden的大小，如何选择GC策略,控制Full GC的频率？ 
  + 服务端调优（线程池，等待队列） 
  + 数据库优化减少查询修改时间。数据库的选取？数据库引擎的选取？数据库表结构的设计？数据库索 引、触发器等设计？是否使用读写分离？还是需要考虑使用数据仓库？ 
  + 缓存数据库的使用，如何选择缓存数据库？是Redis还是Memcache? 如何设计缓存机制？ 
  + 数据通信问题，如何选择通信方式？是使用TCP还是UDP，是使用长连接还是短连接？NIO还是 BIO？netty、mina还是原生socket？ 
  + 操作系统选取，是使用winserver还是Linux？或者Unix？ 
  + 硬件配置？是8G内存还是32G，网卡10G还是1G? 例如：增加CPU核数如32核，升级更好的网卡如 万兆，升级更好的硬盘如SSD，扩充硬盘容量如2T，扩充系统内存如128G； 
+ 以上的这些问题在高并发中都是必须要深入考虑的，就像木桶原理一样，只要其中的某一方面没有考虑 到，都会造成系统瓶颈，影响整个系统的运行。而高并发问题不仅仅涉及面之广，同时又要求有足够的深 度！！！ 
+ 而多线程在这里只是在同/异步角度上解决高并发问题的其中的一个方法手段，是在同一时刻利用计算 机闲置资源的一种方式。 多线程在解决高并发问题中所起到的作用就是使计算机的资源在每一时刻都能达到最大的利用率，不至于 浪费计算机资源使其闲置。

## 预习课



## VIP课

