# 更新文档

## 一、手动更新

进入到项目路径，依次运行下面的命令：

```
git pull
```
> 拉取最新的项目文件

```
gitbook build
```
> 编译文件，编译后生成的静态文件会放置在 `_book` 目录。

```
rm -rf _book_cache
cp -r _book _book_cache
```
> 将编译的文件从 `_book` 复制到 `_book_cache`，最终网站运行时是读取 `_book_cache` 目录下的文件。

## 二、自动更新

### 1、在 GitHub 仓库中配置 webhook
![](http://cdn.zitiao.org/deploy/jup78.jpg) 

### 2、在服务器上通过程序来接收事件
当代码有提交的时候，GitHub 会往上面的地址推送消息，服务器接收到消息之后，执行 `手动更新` 里的脚本就可以了。    

具体的代码如何实现，就交给公司的研发人员了，我们就不在此细说，因为我也不懂代码，惭愧。

## 三、注意事项

如果在更新的时候 `book.js` 发生了变更，需要执行 `gitbook install`。
