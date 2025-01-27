# chelly.site

这是一个简单的个人网站项目。

## 部署到 Cloudflare Pages

1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com)
2. 进入 Pages 部分
3. 点击 "Create a project" 创建新项目
4. 选择 "Connect to Git" 并连接到您的 GitHub 仓库
5. 配置部署设置：
   - 构建命令：留空（不需要构建）
   - 输出目录：.（根目录）
   - 环境变量：无需配置
6. 点击 "Save and Deploy"

部署完成后，Cloudflare 会提供一个 `*.pages.dev` 的域名。要将您的域名（如 chelly.site）绑定到此网站，请按照以下步骤操作：

1. 确保您的域名已经转移到 Cloudflare 的 DNS 服务器
   - 在 Cloudflare 控制面板中添加您的域名
   - 按照指示更新您域名注册商处的 DNS 服务器
   - 等待 DNS 服务器变更生效（通常需要几分钟到几小时）

2. 配置域名解析
   - 在 Cloudflare 的 DNS 设置页面中
   - 添加一条 CNAME 记录
   - 将 chelly.site 指向 Cloudflare Pages 提供的 *.pages.dev 域名
   - 确保代理状态（小云朵图标）是开启的

3. 在 Pages 项目设置中添加自定义域名
   - 进入项目的 "Custom Domains" 设置
   - 点击 "Add a domain"
   - 输入您的域名（chelly.site）
   - 按照提示完成验证步骤

完成以上步骤后，您的网站就可以通过 chelly.site 访问了。DNS 解析生效可能需要一些时间，请耐心等待。

## 本地开发

```bash
npm install    # 安装依赖
npm start      # 启动本地服务器
```

## 项目结构

- `index.html`: 主页面
- `styles/main.css`: 样式文件
- `package.json`: 项目配置文件