# xray-frontend-release-public

这是 **公开的带前端安装包仓库**。

你需要这样理解它：
- 这里只放 **带前端 / 面板版** 安装包
- 仓库根目录始终保留当前最新的带前端包
- 用它来直接下载可访问网页面板的版本

它 **不是**：
- 无前端安装包仓
- 私有源码仓

当前文件：
- `xray-backend-release.tar.gz`
- `SHA256SUMS.txt`

对应私有源码提交：
- `9f69fed` `Remove SSH knock and ship real traffic monitoring`

当前根目录同步的公开包：
- 基于带前端私有完整源码仓 `main` 的最新安装包
- 已对齐官方正式版 `Xray-core v26.3.27`
- 已移除 SSH knock 入口与后端逻辑，SSH `22` 固定开放
- 已接入真实流量统计链路：Xray stats API、配额字节化、重启后差分持久化
- 已补齐 `XHTTP / gRPC / ALPN(h2/h3/http/1.1)` 与官方当前行为的兼容
- 当前固定版本 tag：`v2026.03.30-frontend-direct-1`

仓库根目录直链：

```bash
curl -fL --progress-bar -o xray-backend-release.tar.gz https://raw.githubusercontent.com/huotian420-cyber/xray-frontend-release-public/main/xray-backend-release.tar.gz
```

固定版本下载：

```bash
curl -fL --progress-bar -o xray-backend-release.tar.gz https://raw.githubusercontent.com/huotian420-cyber/xray-frontend-release-public/v2026.03.30-frontend-direct-1/xray-backend-release.tar.gz
```

校验命令：

```bash
curl -fL --progress-bar -o SHA256SUMS.txt https://raw.githubusercontent.com/huotian420-cyber/xray-frontend-release-public/main/SHA256SUMS.txt
sha256sum -c SHA256SUMS.txt
```

和另外 3 个仓的关系：
- 带前端私有完整源码仓：
  - [huotian420-cyber/xray-](https://github.com/huotian420-cyber/xray-)
- 无前端私有源码仓：
  - [huotian420-cyber/xray-headless-source](https://github.com/huotian420-cyber/xray-headless-source)
- 公开无前端安装包仓：
  - [huotian420-cyber/xray-release-public](https://github.com/huotian420-cyber/xray-release-public)

说明：
- 这里是带前端公开包
- Release 页面会保留历史带前端版本
- 仓库根目录只保留当前最新的带前端包
- 如果你要改代码，不要看这个仓，去 `xray-`
- 如果你只要无前端 headless 包，不要下这个仓，去 `xray-release-public`
