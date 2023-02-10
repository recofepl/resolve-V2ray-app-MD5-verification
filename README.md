### 针对客户端 MD5 验证的问题

* 对于在 2022 年没有进行维护的客户端，它们仍然在使用 MD5 验证，这会导致服务无法正常进行
* 如果您需要使用这种客户端，那么，个人提供以下一种参考方式

```
// 在您执行完脚本内容之后，继续执行下面的指令以改变环境兼容性

// 编辑 V2ray 环境配置文件

vi /etc/systemd/system/v2ray.service

// 关闭 Vmess 协议的强行验证机制 (直接复制写入)

Environment="V2RAY_VMESS_AEAD_FORCED=false"

// 重启 V2ray 服务

systemctl daemon-reload
systemctl restart v2ray

```
