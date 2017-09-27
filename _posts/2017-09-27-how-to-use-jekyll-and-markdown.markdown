---
layout: post
title:  "学习实用Jekyll和markdown"
author: Gary
date:   2017-09-27 14:27:21 +0800
comments: false
categories:
- Works
- Tech
tags:
- markdown
- jekyll
---
安装Jekyll并部署在github pages上 （Mac 环境）

##安装Jekyll
```
gem install jekyll #如果权限不足，前面加sudo
jekyll new my-awesome-site
cd my-awesome-site/
jekyll serve
```

以上命令可以在本地创建一个jekyll站点，并且可以通过http://localhost:4000来预览
下一步就是将站点部署在github上，以后就可以通过git来更新站点了，符合我们程序员的习惯

##创建github帐号
在`http://www.github.com`注册帐号，假设用户名myusername，那么就创建一个myusername.github.io 的仓库，这个仓库的master讲作为myusername.github.io的源。比如我的就是 `codingdonkey.github.com`。至此，只要将上一步创建的my-awesome-site目录git push到该仓库即可。注意 .gitignore文件应忽略_site目录， 因为该目录github pages会自动生成，无需上传。

现在你可以在本地_posts 目录下愉快地写文章了。one more thing，别忘了每篇文章开头的yaml格式。

```
---
layout: post
title:  "学习实用Jekyll和markdown"
author: Gary
date:   2017-09-27 14:27:21 +0800
comments: false
categories:
- Works
- Tech
tags:
- markdown
- jekyll
---
```
