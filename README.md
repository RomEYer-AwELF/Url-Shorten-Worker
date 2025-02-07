# 修改说明：
直接访问域名返回404。在KV中设置一个entry，保存秘密path，只有访问这个path才显示使用页面。

https://zelikk.blogspot.com/2022/07/url-shorten-worker-hide-tutorial.html

支持自定义短链

https://zelikk.blogspot.com/2022/07/url-shorten-worker-custom.html

API 不公开服务

https://zelikk.blogspot.com/2022/07/url-shorten-worker-api-password.html

页面缓存设置过的短链

https://zelikk.blogspot.com/2022/08/url-shorten-worker-localstorage.html

长链接文本框预搜索localStorage

https://zelikk.blogspot.com/2022/08/url-shorten-worker-bootstrap-list-group-oninput.html

增加删除某条短链的按钮

https://zelikk.blogspot.com/2022/08/url-shorten-worker-delete-kv-localstorage.html

# 完整的部署教程
https://zelikk.blogspot.com/2022/07/url-shorten-worker-hide-tutorial.html


# Url-Shorten-Worker
A URL Shortener created using Cloudflare Worker

# API

[API Documentation (API文档)](API.md)

# Getting start
### 去Workers KV中创建一个命名空间

Go to Workers KV and create a namespace.

<img src="https://cdn.jsdelivr.net/npm/imst@0.0.4/20201205232805.png">

### 去Worker的Settings选选项卡中绑定KV Namespace

Bind an instance of a KV Namespace to access its data in a Worker.

<img src="https://cdn.jsdelivr.net/npm/imst@0.0.4/20201205232536.png">

### 其中Variable name填写`LINKS`, KV namespace填写你刚刚创建的命名空间

Where Variable name should set as `LINKS` and KV namespace is the namespace you just created in the first step.

<img src="https://cdn.jsdelivr.net/npm/imst@0.0.4/20201205232704.png">

### 复制本项目中的`index.js`的代码到Cloudflare Worker 

Copy the `index.js` code from this project to Cloudflare Worker. 

### 点击Save and Deploy

Click Save and Deploy

# Demo
https://lnks.tools/
 
Note: Because someone abuse this demo website, all the generated link will automatically expired after 24 hours. For long-term use, please deploy your own.

注意：所有由Demo网站生成的链接24小时后会自动失效，如需长期使用请自行搭建。
