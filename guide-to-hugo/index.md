# Guide to Hugo




### 网站图标

利用 [https://realfavicongenerator.net/](https://realfavicongenerator.net/) 生成图标文件，放在 `/static` 目录
- apple-touch-icon.png (180x180)
- favicon-32x32.png (32x32)
- favicon-16x16.png (16x16)
- mstile-150x150.png (150x150)
- android-chrome-192x192.png (192x192)
- android-chrome-512x512.png (512x512)

可以自定义 `browserconfig.xml` 和 `site.webmanifest` 文件来设置 theme-color 和 background-color.



### blog发布

touch deploy.sh &emsp;&emsp;//content is as follows

. ./deploy.sh   &emsp;&emsp;//if there is "cd..." in bash

```bash
!/bin/bash

cd ~/myblog/
echo -e "\033[0;32mDeploying updates to GitHub...\033[0m"

# Build the project.
hugo --theme=LoveIt --baseUrl="https://lianfengyeo.github.io/" --buildDrafts

# if using a theme, replace with `hugo -t <YOURTHEME>`

# Go To Public folder
cd public

# Add changes to git.
git add .

# Commit changes.
msg="rebuilding site `date`"
if [ $# -eq 1 ]
  then msg="$1"
fi
git commit -m "$msg"

# Push source and build repos.
git push origin master

# Come Back up to the Project Root
cd ~/Downloads
```
