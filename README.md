# 西瓜游戏 (Suika Game)

这是一个基于网页的西瓜游戏项目，提供了漂亮的用户界面和游戏规则说明。

## 项目结构

```
suikagame/
├── index.html          # 主页面文件 (English)
├── zh.html            # 中文版本页面
├── img/               # 水果图片资源
├── _headers           # HTTP头部配置
├── _redirects         # 重定向规则
├── wrangler.toml      # Cloudflare配置
├── .gitignore         # Git忽略文件
└── README.md          # 项目说明
```

## 部署到 Cloudflare Pages

### 方法一：通过 Git 仓库部署

1. 将代码推送到 GitHub/GitLab 仓库
2. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)
3. 进入 "Pages" 页面
4. 点击 "创建项目"
5. 选择 "连接到 Git"
6. 选择你的仓库
7. 配置构建设置：
   - 构建命令：留空
   - 输出目录：`/`
   - 根目录：`/`
8. 点击 "保存并部署"

### 方法二：直接上传文件

1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. 进入 "Pages" 页面
3. 点击 "创建项目"
4. 选择 "直接上传"
5. 将所有文件打包上传
6. 设置项目名称
7. 点击 "部署"

### 方法三：使用 Wrangler CLI

1. 安装 Wrangler：
   ```bash
   npm install -g wrangler
   ```

2. 登录 Cloudflare：
   ```bash
   wrangler login
   ```

3. 部署项目：
   ```bash
   wrangler pages deploy . --project-name suikagame
   ```

## 项目特性

- ✅ 静态网站，无需服务器
- ✅ 双语支持（中文/英文）
- ✅ 响应式设计，支持移动设备
- ✅ 优化的HTTP头部配置
- ✅ 图片资源缓存优化
- ✅ SEO友好
- ✅ 安全头部配置
- ✅ 语言切换功能

## 双语功能

项目提供中英文双语版本：
- 英文版本：`index.html` 
- 中文版本：`zh.html`
- 每个页面右上角都有语言切换按钮
- 支持多种中文路由：`/zh`, `/chinese`, `/cn` 都会重定向到中文版

## 游戏规则

1. 拖放水果进行合并
2. 相同的水果会合并成更大的水果
3. 目标是创造最大的水果 - 西瓜！
4. 水果越大，得分越高

## 自定义域名

部署完成后，你可以在 Cloudflare Pages 设置中添加自定义域名：

1. 在项目设置中找到 "自定义域名"
2. 添加你的域名
3. 按照提示配置 DNS 记录

## 开发

本项目是纯静态项目，只需要在浏览器中打开 `index.html` 即可本地预览。

## 许可证

MIT License