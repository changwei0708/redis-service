# redis-service
java spring redies：

订阅/发布系统: pubsub；

统一配置管理: disconf；

lua脚本实现分布式锁；

缓存应用（连接池，切片连接池，哨兵模式）

附注：哨兵、分片、集群

哨兵模式集群（一主多从）：每个节点拥有所有数据，内存限制
|
改进（解决内存问题）
|
分片多主多从：客户端分配key存储。数据分布在多个节点。扩容麻烦（预分片：初期设置预估需要的分片数）。
|
升级(解决扩容问题)
|
3.0集群（数据分散在集群中的库节点上，支持一定的访问性及故障恢复，拥有与单节点同样的性能）（注意不同节点上key的多健命令；只能使用0号数据库，禁select）

哨兵为集群的子集，是用于不需数据分片，或者使用客户端分片的情况。