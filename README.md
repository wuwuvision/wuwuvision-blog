# 北京吾悟视觉技术博客

基于 Jekyll 构建的静态技术博客，用于发布工业视觉相关技术文章。

## 快速部署指南

### 1. 创建 GitHub 仓库

1. 登录 GitHub
2. 点击右上角 "+" → "New repository"
3. 仓库名：`wuwuvision-blog`
4. 选择 "Public"（公开）
5. 不勾选 "Initialize this repository with a README"
6. 点击 "Create repository"

### 2. 上传文件

将本文件夹中的所有文件上传到仓库：

```
blog/
├── _config.yml          # 博客配置
├── _posts/              # 文章目录
│   └── 2026-05-22-非标视觉检测方案选型指南.md
├── index.html           # 首页
├── about.md             # 关于页面
├── README.md            # 本文件
└── .nojekyll            # 禁用 Jekyll 处理（空文件）
```

**上传方法：**
- 使用 GitHub Desktop 客户端
- 或使用 Git 命令：
  ```bash
  git init
  git add .
  git commit -m "Initial commit"
  git branch -M main
  git remote add origin https://github.com/你的用户名/wuwuvision-blog.git
  git push -u origin main
  ```

### 3. 启用 GitHub Pages

1. 进入仓库页面
2. 点击 "Settings" → "Pages"
3. 在 "Source" 中选择 "Deploy from a branch"
4. 在 "Branch" 中选择 "main" 分支，文件夹选择 "/ (root)"
5. 点击 "Save"
6. 等待 1-2 分钟，页面会显示 "Your site is live at https://你的用户名.github.io/wuwuvision-blog/"

### 4. 配置自定义域名（可选但推荐）

**将 wuwuvision.cn/blog 指向博客：**

1. 在域名注册商处（如阿里云万网）添加 CNAME 记录：
   ```
   Type: CNAME
   Name: blog
   Value: 你的用户名.github.io
   TTL: 600
   ```

2. 在 GitHub Pages 设置中添加自定义域名：
   - 在 "Custom domain" 中输入：`blog.wuwuvision.cn` 或 `wuwuvision.cn/blog`
   - 勾选 "Enforce HTTPS"

3. 等待 DNS 生效（通常 10-30 分钟）

### 5. 在官网首页添加链接

在 `wuwuvision.cn` 首页的导航栏或页脚添加：
```html
<a href="/blog" target="_blank">技术博客</a>
```

## 添加新文章

1. 在 `_posts/` 目录下创建新的 Markdown 文件
2. 文件名格式：`YYYY-MM-DD-文章标题.md`
3. 文件头部添加 YAML 头信息：
   ```yaml
   ---
   layout: post
   title: "文章标题"
   date: 2026-05-22 10:00:00 +0800
   categories: 分类
   tags: 标签1 标签2 标签3
   author: 北京吾悟视觉技术有限公司
   description: "文章描述，用于 SEO"
   excerpt: "文章摘要，显示在列表页"
   keywords: 关键词1, 关键词2, 关键词3
   ---
   ```

4. 正文使用 Markdown 格式

## SEO 优化

博客已配置：
- 自动生成 sitemap.xml
- 自动生成 RSS feed
- 结构化数据标记
- 移动端适配
- 快速加载（静态页面）

## 后续维护

1. **发布新文章**：直接在 `_posts/` 目录添加 Markdown 文件
2. **修改配置**：编辑 `_config.yml`
3. **更新主题**：如需更换外观，可修改主题设置

## 技术支持

如有问题，请联系：
- 邮箱：contact@wuwuvision.cn
- 官网：wuwuvision.cn