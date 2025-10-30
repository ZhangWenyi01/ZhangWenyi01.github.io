# 部署指南 — 将博客发布到 GitHub Pages

下面的步骤假设你要把站点发布到 `https://your-username.github.io`：

1. 在 `_config.yml` 中把 `github_username` 和 `url` 替换为你的 GitHub 用户名和网址。例如：

   github_username: wang
   url: "https://wang.github.io"

2. 在 GitHub 上创建一个新的 repository，名字必须为 `your-username.github.io`（把 your-username 换成你的用户名）。

3. 在本地初始化 git 并推送到该仓库（在 Windows cmd.exe 中运行）：

```
cd c:\Users\wang\Desktop\WenyiBlog
git init
git add .
git commit -m "Initial commit: Jekyll blog scaffold"
git branch -M main
git remote add origin https://github.com/your-username/your-username.github.io.git
git push -u origin main
```

替换 `your-username` 为你的 GitHub 用户名。推送之后，GitHub 会自动使用 Pages 服务构建并托管你的站点（GitHub Pages 内置支持 Jekyll 和主题 `minima`）。

本地预览（可选）:

如果想在本地预览，你需要安装 Ruby、Bundler 和 Jekyll。示例命令（PowerShell 或 cmd）如下：

```
gem install bundler jekyll
bundle exec jekyll serve
```

然后打开 http://127.0.0.1:4000 查看效果。

注意事项：
- 若你使用自定义 domain，请在 repo 中添加 `CNAME` 文件并在 GitHub Pages 设置中配置。
- 若站点没有按预期构建，检查 GitHub Actions / Pages 构建日志，或在本地运行 `bundle exec jekyll build --verbose` 获取详细信息。
