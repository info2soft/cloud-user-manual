## I2node安装 {#i2node}

### Windows安装 {#windows}

#### 安装

双击安装程序包，出现如下界面，点击下一步；
![](/assets/V6.02690.png)

勾上“我接受许可证协议中的条款”，点击下一步；
![](/assets/V6.02716.png)

输入用户名和公司名称，点击下一步；
![](/assets/V6.02736.png)

选择安装类型，必须选择“云客户端”，点击下一步；
![](/assets/V6.02763.png)

选择“全部”则按程序默认方式安装，选择“定制”可自定义安装目录；
![](/assets/V6.02798.png)

假如选择“定制”安装会出现如下界面；
![](/assets/V6.02819.png)

下一步；
![](/assets/V6.02826.png)

下一步；
![](/assets/V6.02833.png)

点击“安装”后，如下图安装完成；
![](/assets/V6.02852.png)

点击“完成”，开始配置客户端，请按照如下配置向导配置您的客户端。

#### 配置向导 {#-0}
![](/assets/V6.02892.png)

点击“下一步”；
![](/assets/V6.02903.png)

输入云灾备地址，点击“提交”；
![](/assets/V6.02921.png)

点击“下一步”；
![](/assets/V6.02932.png)

点击“升级”；
![](/assets/V6.02942.png)

升级成功，如下图；
![](/assets/V6.02954.png)

点击“下一步”；
![](/assets/V6.02966.png)

输入客户端名称，云备份帐号，云备份密码，点击“绑定客户端”；

如果云备份帐号没有足够的服务套餐可用，则会跳出如下界面, 此时用户需要联系运营商或管理员分配服务套餐或者自己登录到i2Cloud界面订购服务套餐；
![](/assets/V6.03074.png)

如果有足够的服务套餐可用，则会跳出如下界面；
![](/assets/V6.03099.png)

添加客户端成功，点击“确定”；
![](/assets/V6.03117.png)

点击“添加数据备份规则”，跳出网页, 在此网页可创建复制规则;
![](/assets/V6.03151.png)
![](/assets/V6.03153.png)

点击“下一步”；
![](/assets/V6.03164.png)

点击“进入监控状态”；
![](/assets/V6.03178.png)


配置向导到此全部完成。

配置向导完成后确认复制服务、RPC服务、日志服务处于运行状态，并确认版本号信息。

关于服务状态，复制服务对应任务管理器中的sdatad.exe进程，RPC服务对应任务管理器中的rpcserver.exe进程，日志服务对应任务管理器中的sdatalogd.exe进程。

只要任务管理器中sdatad.exe、rpcserver.exe、sdatalogd.exe这些进程开启了，服务状态就是运行中；如果这些进程没有开启，服务状态就是已停止。

如下图，假如复制服务已停止，可以在菜单“文件-&gt;“客户端设置”中开启此服务，或者在“计算机管理-&gt;服务”中开启此服务；

点击菜单“文件-&gt;“客户端设置”；
![](/assets/V6.03498.png)

点击复制服务后的“启动”按钮，可启动复制服务；
![](/assets/V6.03525.png)

#### 登录云备份平台 {#-1}

用该账号登录云备份平台，进入“云备份”-&gt;“设置”，可以查看修改客户端配置；
![](/assets/V6.03574.png)

点击“修改”按钮；
![](/assets/V6.03587.png)

按照界面提示完成客户端配置，详细说明请参考第5章。

### Linux安装 {#linux}

以centos6.5_64bit为例：

打开终端或者是SSH方式连接到服务器，按如下命令行的方式进行。
![](/assets/V6.03678.png)

Install mode: 请选择2；

Login ID：请选择n，采用默认的Login ID；

Control Server Address: 请选择y，然后输入：运营商指定的控制机地址；

Linux的认证码和控制机地址配置文保存在：/etc/sdata/i2id.conf. 文件的内容和格式与Windows客户端产生的相同。

Linux客户端的添加请参考第5章。

可以通过查看后台守护进程确认I2node安装成功，

[root@station64 ~]# ps -ef | grep sdata

root 9484 1 0 08:04 ? 00:00:00 /usr/local/sdata/sbin/sdatad

root 9490 1 0 08:04 ? 00:00:00 /usr/local/sdata/sbin/rpcserver

root 9493 1 0 08:04 ? 00:00:00 /usr/local/sdata/sbin/sdatalogd

root 9495 1 0 08:04 ? 00:00:00 /usr/local/sdata/sbin/I2Availability

root 9499 1 0 08:04 ? 00:00:00 /usr/local/sdata/sbin/i2monitor

root 9536 6371 0 08:09 pts/1 00:00:00 grep sdata