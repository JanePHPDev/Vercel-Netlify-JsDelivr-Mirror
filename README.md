## 泽客CDN / ZeinkCDN Proxy

> [!TIP]
> 🚀 基于 Serverless 的多功能CDN反向代理服务，零成本、高可用  
> **支持国内外主流前端资源库、API服务及字体加速**  
> 🌐 **[演示站点：cdn.zeinklab.com](https://cdn.zeinklab.com)**

基于 Netlify/Vercel Serverless 架构编写的全能CDN反向代理解决方案，不仅解决 jsDelivr 在中国大陆访问受限问题，更扩展支持 Google Fonts、Gravatar、Gemini API 等多种服务。

![License](https://img.shields.io/badge/license-MIT-green)
![Deploy](https://img.shields.io/badge/Deploy-Netlify%7CVercel-blue)

---

## ✨ 核心特性

| 服务类型 | 本地路径 | 目标CDN | 用途说明 |
|----------|----------|---------|----------|
| **AI API** | `/gemini/*` | Google Generative Language API | Gemini 模型接口代理 |
| **NPM加速** | `/npm/*` | jsDelivr NPM | NPM 包文件加速 |
| **GitHub加速** | `/gh/*` | jsDelivr GitHub | GitHub 仓库文件代理 |
| **WordPress加速** | `/wp/*` | jsDelivr WordPress | WordPress 插件/主题加速 |
| **头像服务** | `/avatar/*` | Gravatar | 头像服务反代 |
| **NPM浏览器化** | `/unpkg/*` | unpkg | 自动解析NPM包浏览器入口 |
| **前端库** | `/cdnjs/*` | cdnjs.cloudflare.com | 通用前端库加速 |
| **字体样式** | `/fonts/*` | Google Fonts CSS | Web字体样式表代理 |
| **字体文件** | `/fonts-gstatic/*` | Google Fonts Static | WOFF2字体文件加速 |
| **jQuery官方** | `/jquery/*` | code.jquery.com | jQuery 官方CDN |
| **Bootstrap** | `/bootstrap/*` | BootstrapCDN | Bootstrap 框架加速 |
| **图标库** | `/fontawesome/*` | Font Awesome | 图标字体库代理 |


[![Star History Chart](https://api.star-history.com/svg?repos=JanePHPDev/ZeinkCDN-Proxy&type=Date)](https://star-history.com/#JanePHPDev/ZeinkCDN-Proxy&Date) 


## 🚀 快速部署

### Vercel 一键部署
[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/JanePHPDev/ZeinkCDN-Proxy&project-name=ZeinkCDN-Proxy&repository-name=ZeinkCDN-Proxy)

### Netlify 一键部署
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/JanePHPDev/ZeinkCDN-Proxy)

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
1. 提交 [Issue](https://github.com/JanePHPDev/ZeinkCDN-Proxy/issues) 反馈问题
2. Fork 项目并提交 Pull Request

## 📜 开源协议

本项目采用 [MIT License](LICENSE) 开源

---

> 如果本项目对您有帮助，请点亮 ⭐ Star 支持！您的认可是我们持续优化的动力！

[![mm_reward_qrcode_1743497808845.png](https://cdn.mengze.vip/gh/YShenZe/Blog-Static-Resource@main/images/mm_reward_qrcode_1743497808845.png)](https://cdn.mengze.vip/gh/JanePHPDev/Blog-Static-Resource@main/images/mm_reward_qrcode_1743497808845.png)