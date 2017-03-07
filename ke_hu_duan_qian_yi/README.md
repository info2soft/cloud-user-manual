# 客户端迁移

客户端迁移是指实现客户端保护的转移，即放弃对原有服务器的保护，转向对新服务器的保护。比如原有服务器宕机，需要一台新的服务器代替原有的服务器，则需要将数据从云端恢复到新的服务器，然后需要保护新服务器上的数据到云端。再比如，随着应用访问量的增大，客户需要升级服务器系统，那也需要做客户端的迁移。

要完成客户端的迁移，通常需要如下步骤：

1\. 在新的服务器上安装应用程序和I2客户端软件，停止应用程序，通过云备份界面添加“数据恢复专用”的客户端；

2\. 从云端将原有客户端的数据恢复到新的服务器（客户端）上；

3\. 启动迁移向导，完成复制规则的转移，进而完成客户端保护的转移；

4\. 最后启动新服务器上的应用程序，应用程序的数据将被实时复制到云端。

需要说明的是，如果迁移的原客户端和目标客户端操作系统类型不同，则原客户端上的复制规则无法迁移到新的客户端上。客户必须在完成客户端迁移之后，手动建立新客户端到云端的复制规则。在完成客户端迁移之后，原客户端下的所有复制规则将被删除，以避免原客户端和新客户端同时备份数据到云端而造成云端数据冲突。