# 运行部署

## 一、将项目拉到服务器

进入到服务器对应目录（本地电脑和远程服务器都可以，我拿我的本地 mac 电脑来演示），并将代码克隆下来，我将项目克隆到我的 `wwwroot` 目录：

```
vincent4j-mac:wwwroot vincent4j$ git clone git@github.com:zitiaocn/deploy.git
```

自动打出下面的文字，代表克隆代码成功：

```
Cloning into 'deploy'...
remote: Counting objects: 40, done.
remote: Compressing objects: 100% (26/26), done.
remote: Total 40 (delta 6), reused 36 (delta 5), pack-reused 0
Receiving objects: 100% (40/40), 23.04 KiB | 0 bytes/s, done.
Resolving deltas: 100% (6/6), done.
Checking connectivity... done.
```

## 二、安装环境

### 1、进入到项目目录

```
vincent4j-mac:wwwroot vincent4j$ cd deploy
vincent4j-mac:deploy vincent4j$
```

### 2、安装依赖环境

```
npm install gitbook-cli -g
```

执行完之后，再执行：

```
npm install
```

上面两个命令执行的时间会比较长，请耐心等待，在这期间会将 `Node.js` 环境也一并安装。

### 3、安装 GitBook 模块

```
gitbook install
```

会安装所需的所有插件，当自动打印如下文字，代表安装成功：

```
info: >> plugin "sitemap-general" installed with success
```

### 4、编译文件

依次执行下面三行命令：

```
gitbook build
```
> 编译文件，编译后生成的静态文件会放置在 `_book` 目录。


```
rm -rf _book_cache
cp -r _book _book_cache
```

> 将编译的文件从 `_book` 复制到 `_book_cache`，最终网站运行时是读取 `_book_cache` 目录下的文件。

### 5、运行

```
gitbook serve
```

当自动打印出如下文字，就代码运行成功：

```
Starting server ...
Serving book on http://localhost:4000
```

在浏览器里访问 <http://localhost:4000> 就能看到文档了，就可以 `乐开怀` 咯。

![](http://cdn.zitiao.org/deploy/3h9zg.jpg)

## 三、注意事项

同一台服务器部署多个项目时，只需要安装一次 `安装依赖环境`。
