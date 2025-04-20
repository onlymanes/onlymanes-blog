cd D:\Canada
mkdir onlymanes-blog
cd onlymanes-blog
git init

在仓库根目录建 _config.yml，写入：
title: onlymanes Blog
url: "https://onlymanes.ai"
baseurl: "/about"
remote_theme: jekyll/minima
plugins:
  - jekyll-feed
  - jekyll-seo-tag

git add .
git commit -m "init blog"