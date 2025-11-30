# 一、链接
## 官方文档
[The Open vSwitch Database Management Protocol](https://datatracker.ietf.org/doc/html/rfc7047)
[OVS文档](https://www.openvswitch.org/support/dist-docs/)
## 官方视频
[Introduction to OVN - OVS Conference 2015](http://youtube.com/watch?v=v1xkJjnuzhk)
## 他人
[网络虚拟化介绍（OVS、DVS）](https://blog.csdn.net/m0_49864110/article/details/134291580)
## 他人视频
[Introduction to Open vSwitch (OVS)](https://www.youtube.com/watch?v=rYW7kQRyUvA)
物理端口，vm端口，bridge三者的连接情况

[Some Insight into Open vSwitch Configuration](https://blog.scottlowe.org/2012/10/04/some-insight-into-open-vswitch-configuration/)
这些对象（网桥、端口、绑定、接口）实际上是 OVSDB 中的_表_ ，因此需要使用 `ovs-vsctl` 中与 OVSDB 相关的参数才能修改它们的属性。
`ovs-vsctl <command> <table name> <record name> <setting=value>`
在这个通用命令中， `<command>` 可以是类似 set、get 或 list 这样的命令，而 `<table name>` 将被替换为特定的 OVSDB 表名。例如， `port` 就是这样一个表
`ovs-vsctl set port <record name> <setting=value>`
`ovs-vsctl set port bond0 trunks=10,20,30,40,50`