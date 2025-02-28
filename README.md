# Vercel/Netlify-jsdelivr-mirror

> [!TIP]
> 🚀 JsDeliv-CN 项目已上线！使用本套源码，提供长期免费的 JsDelivr 中国加速服务：  
> **[立即访问](https://jsdelivrcn.netlify.app/) ➡️**

基于 Serverless 架构编写的 Jsdelivr 反向代理解决方案模板仓库，提供零成本、高可用的 CDN 加速服务，解决中国内陆地区因GFW拦截，Jsdelivr官方节点访问受限问题。

![License](https://img.shields.io/badge/license-MIT-green)

## 🌟 核心优势

- **零成本运营** - 基于 Vercel/Netlify 免费额度，无需服务器投入  
- **智能缓存加速** - 自动缓存资源到边缘节点，访问速度提升 300%+  
- **一键全球分发** - 自动同步 jsDelivr 资源，支持 npm/gh 全生态  
- **多平台支持** - 同时兼容 Vercel/Netlify 两大 Serverless 平台  
- **HTTPS 加密** - 自动启用 SSL 证书，数据传输更安全  

## 🚀 快速部署

### Vercel 一键部署
[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YShenZe/Vercel-Netlify-JsDelivr-Mirror&project-name=jsd-mirror&repository-name=jsd-mirror)

### Netlify 一键部署
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/YShenZe/Vercel-Netlify-JsDelivr-Mirror)

> [!WARNING]
> **重要安全提醒**  
> 1. 必须绑定自定义域名！Vercel 默认 `*.vercel.app` 域名在中国大陆无法访问  
> 2. 推荐使用未被污染的域名（建议注册时间 >6 个月）  
> 3. 新域名建议先进行 DNS 污染检测（可使用 [DNS Checker](https://dnschecker.org/)）

## 🔧 配置指南

### 域名解析设置

| 平台    | 记录类型 | 主机名       | 指向地址                     |
|---------|----------|--------------|-----------------------------|
| Vercel  | CNAME    | @ 或 www     | `cname-china.vercel-dns.com`|
| Netlify | CNAME    | @ 或 www     | 自动分配的 xxx.netlify.app  |

### 平台配置步骤

**Vercel 配置流程**：
1. 登录 [Vercel Dashboard](https://vercel.com/dashboard)
2. 进入项目 → Settings → Domains
3. 添加已解析的域名（如 `cdn.yourdomain.com`）
4. 等待 SSL 证书自动签发（约2分钟）

**Netlify 配置流程**：
1. 登录 [Netlify 控制台](https://app.netlify.com/)
2. 进入 Site configuration → Domain management
3. 添加自定义域名并验证所有权
4. 开启 [HTTPS 强制跳转](https://docs.netlify.com/domains-https/https-ssl/#automatic-https)

## 💡 使用示例

将原 jsDelivr 链接中的域名替换为你的镜像域名：

```bash
# 原链接
https://cdn.jsdelivr.net/npm/vue@3/dist/vue.global.js

# 替换后
https://cdn.yourdomain.com/npm/vue@3/dist/vue.global.js
```

支持所有 jsDelivr 资源类型：
- npm 包：`/npm/包名@版本/文件路径`
- GitHub 资源：`/gh/用户/仓库@版本/文件路径`
- 组合加速：`/combine/...`

## 🤝 参与贡献

欢迎通过以下方式参与项目：
1. 提交 [Issue](https://github.com/YShenZe/vercel-jsdelivr-mirror/issues) 反馈问题
2. Fork 项目并提交 Pull Request
3. 加入技术讨论群：[Telegram Group](https://t.me/jsdelivr_cn)

贡献者名单：  
[![Contributors](https://contrib.rocks/image?repo=YShenZe/vercel-jsdelivr-mirror)](https://github.com/YShenZe/vercel-jsdelivr-mirror/graphs/contributors)

## 📜 开源协议

本项目采用 [MIT License](LICENSE) 开源

---

> 如果本项目对您有帮助，请点亮 ⭐ Star 支持！您的认可是我们持续优化的动力！
