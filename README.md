# Vercel/Netlify-jsdelivr-mirror

> [!TIP]
> JsDeliv-CN项目已上线！使用本套源码，提供长期免费的JsDelivr中国加速服务：https://jsdelivrcn.netlify.app/

基于 ServerLess 的 jsDelivr 反向代理源码，提供一个简便的方式在 Vercel/Netlify 部署自己的 jsDelivr 代理，以解决 jsDelivr 在部分地区访问受限的问题。

## 功能特点

- **基于 Vercel/Netlify**：轻量级，无需服务器，免费托管  
- **反向代理**：加速访问 jsDelivr 资源  
- **快速部署**：一键部署，几分钟内即可上线  

## 快速部署

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YShenZe/vercel-jsdelivr-mirror&project-name=jsd&repository-name=jsd)  

Netlify部署请克隆本仓库到Netlify控制面板导入

### 重要提醒  
**Vercel 默认域名已被墙，请自行绑定域名！**  
推荐使用以下 CNAME 解析：
```txt
cname-china.vercel-dns.com
```

## 配置

1. 进入 [Vercel 控制台](https://vercel.com/dashboard)  
2. 选择已部署的项目  
3. 进入 **Settings -> Domains**，绑定自己的域名  
4. 将域名 CNAME 解析到 `cname-china.vercel-dns.com`

Netlify类似

## 许可证

本项目采用 [MIT 许可证](LICENSE)。欢迎自由使用、修改和分发。

## 贡献

欢迎提交 Issues 反馈问题或提供改进建议！也可以 Fork 本项目并提交 Pull Request 贡献代码。
