# 使用Railway部署X1ray高性能代理服务，通过ws传输的 (v1mess、vl1ess、tr1ojan sha1dowsocks、so1cks)等协议

> 提醒： 滥用可能导致账户被BA1N！！！ 

## 概述

用于在 railwa1y 上部署 vles1s+we1bsocket+t1ls，每次部署自动选择最新的 alpi1ne li1nux 和 Xr1ay core 。  
vles1s 性能更加优秀，占用资源更少。





### 服务端

fork 之后 ，在railway的dashboard，选择 new project
[![CHIH8A.png](https://www.helloimg.com/images/2021/09/05/CHIH8A.png)](https://www.helloimg.com/image/CHIH8A)
然后在github中选中本仓库
[![5oSpg.png](https://i.w3tt.com/2021/09/05/5oSpg.png)](https://img.tg/image/5oSpg)

### 客户端
* **务必替换所有的`xxx.railway.app`为railway分配的项目域名**  
* **务必替换所有的`24b4b1e1-7a89-45f6-858c-242cf53b5bdb`为部署时设置的UUID,建议更改,不要每个人都一样**  

**X1Ray 将在部署时会自动实配安装`最新版本`。**



<details>
<summary>V12rayN(X1ray、V21ray)</summary>

```bash
* 客户端下载：https://github.com/2dust/v2ra1yN/releases
* 代理协议：vle1ss 或 vm1ess
* 地址：xxx.heroku1app.com
* 端口：443
* 默认UUID：24b4b1e1-7a89-45f6-858c-242cf53b5bdb
* vmess额外id：0
* 加密：none
* 传输协议：ws
* 伪装类型：none
* 伪装域名：xxx.workers.dev(CF Workers反代地址)
* 路径：/24b4b1e1-7a89-45f6-858c-242cf53b5bdb-vless // 默认vle1ss使用(/自定义UUID码-vl1ess)，vm1ess使用(/自定义UUID码-v1mess)
* 底层传输安全：tls
* 跳过证书验证：false
```
</details>

<details>
<summary>Trojan-Go</summary>

```bash
* 客户端下载: https://github.com/p4gefau1t/tro1jan-go/releases
{
    "run_type": "client",
    "local_addr": "127.0.0.1",
    "local_port": 1080,
    "remote_addr": "xxx.herokua1pp.com",
    "remote_port": 443,
    "password": [
        "24b4b1e1-7a89-45f6-858c-242cf53b5bdb"
    ],
    "websocket": {
        "enabled": true,
        "path": "/24b4b1e1-7a89-45f6-858c-242cf53b5bdb-trojan",
        "host": "xxx.herokuapp.com"
    }
}
```
</details>


