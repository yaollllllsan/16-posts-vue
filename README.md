# myblog vue


## 首先，创建项目

使用 Idea，创建一个 Empty 项目

预期目录结构是:
```
- myblog
  + .git/
  + server
    - src/
    - web/
  + client
    - node_modules/
    - public/
    - src/
    - package.json
    - vue.config.json
```

## 创建服务端模块

勾选 Web Application

## 创建客户端模块

使用脚手架创建一个 vue 项目:
```shell script
vue create server

vue add element
vue add axios

编辑 package.json
编辑 vue.config.js

npm run serve
```

然后，添加这个为 idea 的一个模块:
```
在 idea 中选择 create module with exists source，然后选择该文件夹
```

## 上传到 Github，方便团队协作

首先，在 Github 上注册一个账号，并 New Repositoy (创建一个新仓库)，比如名字为 myblog。

其次，将本地的项目转换为一个 git 项目:
```shell script
cd myblog
git init .      # 转换
编辑 .gitignore  # 排除某些文件

# 删除 client 下面的 .git 文件夹。因为 vue 脚手架默认为新建的项目初始化了 git，我们不需要
```

保存第一次修改:
```shell script
git add . 
git commit -m 'first'
```

推送到服务器:
```shell script
git remote add origin git@github.com:yaollllllsan/myblog
git push -u origin master
```

之后，进了若干修改，就可以随时记录并上传了:
```shell script
# 记录
git add .
git commit -m "记录"

# 上传
git push
```

另外，可以自己思考下，如何下载并更新。