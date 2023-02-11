### 针对客户端 MD5 验证的问题

注：搭建 V2ray 若是采用 CentOS，建议版本 CentOS 8+

```
// 以下命令只会改变 V2ray 服务端环境配置

// 编辑 V2ray 环境配置文件

vi /etc/systemd/system/v2ray.service

// 关闭 Vmess 协议的强行验证机制 (直接复制写入)

Environment="V2RAY_VMESS_AEAD_FORCED=false"

// 重启 V2ray 服务

systemctl daemon-reload
systemctl restart v2ray

```
