# vnts-lzcapp

[VNT 异地组网服务端 vnts](https://github.com/lmq8267/vnt_s) 的懒猫微服打包（镜像模式，源仓库 [lazycat-contrib/vnts-lzcapp](https://github.com/lazycat-contrib/vnts-lzcapp)，仅发布喵喵商店）。

## 说明

- 数据端口 `29872`（TCP/UDP）经 L4 ingress 暴露，VNT 客户端连接盒子 IP:29872。
- Web 管理后台走应用默认 HTTP 入口（容器内 29870）。
- Web 后台账号密码在安装时通过部署参数设置（默认 `admin` + 随机密码），已配置免密自动填充。
- WireGuard 客户端配置持久化在 `/lzcapp/var/wg`。
- 升级：CI 定时检查上游 `docker.io/lmq8267/vnts` SemVer tag（镜像模式 digest 校验），自动发版并发布喵喵商店。
