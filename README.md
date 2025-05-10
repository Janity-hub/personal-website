# README.md

## 项目简介：Fragments 个人展示网站

这是一个基于 **Hugo + Stack 主题** 构建的静态网站，作为我 Janity 的个人博客、作品集、能力展示平台，未来将托管在 GitHub Pages 上对外公开。

## 技术栈

* Hugo 静态网站生成器
* Stack Hugo 主题（作为 Git 子模块）
* Git 版本控制
* VS Code + Git Bash
* Markdown 编写文章内容

## 构建步骤（含 Git 操作）

### 初始化 Hugo 项目

```bash
hugo new site Fragments
cd Fragments
git init
git add .
git commit -m "初始 Hugo 项目"
```

### 添加 Stack 主题（子模块方式）

```bash
git submodule add https://github.com/CaiJimmy/hugo-theme-stack themes/hugo-theme-stack
git add .gitmodules themes/hugo-theme-stack
git commit -m "添加 Stack 主题为 Git 子模块"
```

### 设置主题（编辑 hugo.toml 或 config.toml）

```toml
theme = "hugo-theme-stack"
```

### 添加 `.gitignore`

```bash
echo "public/" >> .gitignore
echo "resources/" >> .gitignore
echo ".DS_Store" >> .gitignore
echo "themes/*" >> .gitignore
echo "!themes/hugo-theme-stack" >> .gitignore
git add .gitignore
git commit -m "添加 .gitignore 忽略编译文件和缓存"
```

### 加载 Stack 官方配置模板（解决初始页面空白）

```bash
git clone https://github.com/CaiJimmy/hugo-theme-stack-starter.git tmp
cp -r tmp/config ./
cp -r tmp/content ./
cp -r tmp/assets ./
cp -r tmp/static ./
rm -rf tmp
git add config content assets static
git commit -m "导入 Stack starter 配置"
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

## 下一步计划：部署到 GitHub Pages

> TODO

* 连接 GitHub 仓库
* 构建 `public/` 静态文件夹
* 推送至 `gh-pages` 分支
* 配置 GitHub Pages 自动发布

## 作者

* Name: Janity
* Keywords: 创作、设计、编程、表达、自我构建

> 本项目由本人独立设计开发，如需联系或引用请注明出处。
