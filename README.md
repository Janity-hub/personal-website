# README.md

## Project: Fragments – Personal Website

This is a personal website built with **Hugo** and the **Stack theme**, designed for showcasing my blog posts, creative projects, skills, and personal identity. Authored by Janity, this site is intended for publication via **GitHub Pages**.

## Tech Stack

- Hugo Static Site Generator  
- Stack Theme (via starter template)  
- Git for version control  
- VS Code + Git Bash / PowerShell  
- Markdown for content writing  

## Build Steps (with Git versioning)

### Initialize Hugo project

```bash
hugo new site Fragments
cd Fragments
git init
git add .
git commit -m "Initial Hugo site"
```

### Add .gitignore

```bash
echo "public/" >> .gitignore  
echo "resources/" >> .gitignore  
echo ".DS_Store" >> .gitignore  
echo "node_modules/" >> .gitignore  
git add .gitignore  
git commit -m "Add .gitignore to exclude build/cache files"  
```

### Import Stack Starter Template

Download or clone the Stack Starter Template, then copy its config/, content/, static/, and assets/ folders into your Hugo site root.

```bash
git add .
git commit -m "Add Stack starter template files"
```

### Run local preview

```bash
hugo server
```

Open: [http://localhost:1313](http://localhost:1313)

### Create your first article

```bash
hugo new posts/my-first-post.md
```

Edit it under content/posts/.

## Deploying to GitHub Pages

### Connect your GitHub repository

- Create a new GitHub repository named personal-website
- Link it to your local project:

```bash
git remote add origin https://github.com/Janity-hub/personal-website.git
```

### Build the public/ folder (generate the static site)

- This generates the production-ready HTML site in the public/ folder:

```bash
hugo
```

### Create gh-pages branch and push public/

```bash
cd public
git init
git remote add origin https://github.com/Janity-hub/personal-website.git
git checkout -b gh-pages
git add .
git commit -m "Deploy Hugo site to GitHub Pages"
git push -f origin gh-pages
cd ..
```

### Configure GitHub Pages settings

- Open your GitHub repository

- Go to Settings → Pages (in the sidebar)

- Select the gh-pages branch as the source → Save

### Author

Name: Janity

Keywords: creativity, design, development, self-expression, personal brand

> This project was created and maintained by me. Please credit appropriately if referenced or reused.

---

## 项目简介：Fragments 个人展示网站

这是一个基于 **Hugo + Stack 主题** 构建的静态网站，作为我 Janity 的个人博客、作品集、能力展示平台，未来将托管在 GitHub Pages 上对外公开。

## 技术栈

- Hugo 静态网站生成器
- Stack Hugo 主题（作为 Git 子模块）
- Git 版本控制
- VS Code + Git Bash
- Markdown 编写文章内容

## 构建步骤（含 Git 操作）

### 初始化 Hugo 项目

```bash
hugo new site Fragments
cd Fragments
git init
git add .
git commit -m "初始 Hugo 项目"
```

### 添加 .gitignore文件

```bash
echo "public/" >> .gitignore  
echo "resources/" >> .gitignore  
echo ".DS_Store" >> .gitignore  
echo "node_modules/" >> .gitignore  
git add .gitignore  
git commit -m "添加 .gitignore 忽略构建和缓存文件"  
```

### 设置 Stack 官方配置模板

将 Stack starter 项目的 config、content、static、assets 文件夹内容复制到当前项目中。

```bash
git add . 
git commit -m "添加stack starter模板"  
```

### 本地预览网站

```bash
hugo server
```

访问：[http://localhost:1313](http://localhost:1313)

### 创建文章示例

```bash
hugo new posts/my-first-post.md
```

在 `content/posts/` 目录编辑该 Markdown 文件。

## 部署到 GitHub Pages

### 连接 GitHub 仓库

- 去 GitHub 新建一个仓库 personal-website
- 绑定远程地址 <https://github.com/Janity-hub/personal-website>

```bash
git remote add origin https://github.com/你的用户名/fragments-site.git
```

### 构建 public/ 文件夹（生成网站）

- 在项目根目录生成一个 public/ 文件夹，里面是可以发布的 HTML 静态网页。

```bash
hugo
```

### 创建 gh-pages 分支并推送 public/

```bash
cd public
git init
git remote add origin https://github.com/你的用户名/fragments-site.git
git checkout -b gh-pages
git add .
git commit -m "部署 Hugo 站点到 GitHub Pages"
git push -f origin gh-pages
cd ..
```

### 配置 GitHub Pages

- 打开 GitHub 仓库
- 进入「Settings」→ 左侧菜单中点击「Pages」
- 选择 gh-pages 分支作为发布源 → 保存

## 作者

- Name: Janity
- Keywords: 创作、设计、编程、表达、自我构建

> 本项目由本人独立设计开发，如需联系或引用请注明出处。
