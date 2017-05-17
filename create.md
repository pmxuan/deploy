# 项目搭建

## 一、Fork 示例项目

示例项目：<https://github.com/zitiaocn/simple>

## 二、项目结构

这里只罗列需要关注的部分，我们的初衷是先以最小的代价将项目跑起来再说，至于优化或进阶的功能后面再去摸索，讲的太多反倒容易让人觉得这个框架很复杂。  

- images `用于存放图片`   
- README.md `关于文档，在 SUMMARY.md 进行配置`   
- SUMMARY.md `文档目录`      
- book.json `文档框架，最核心的文件`      
- deploy.md `一个示例文档，可以删除`  

下面重点阐述几个文件：

### 1、SUMMARY.md
文档的目录结构，所有需要展示的文档都需要在它里面进行罗列。

详细 GitBook 官方英文文档：<https://toolchain.gitbook.com/pages.html>

> 注：GitBook 支持文件夹，但是文件夹的根目录下必须要指定文件，否则在前台的菜单中点击父级目录的时候无法展开。比如说有一个文档路径是：   
> `xxx.com/simple/create.html`   
>  那么 `xxx.com/simple/` 必须要对应一个文件，在 `SUMMARY.md` 里面；否则点击 `create.html` 父级菜单将不会展开子菜单。 

### 2、book.json
需要注意的参数有 `root`，就是文档内容的根目录，如果文档结构如下：   

```
-- book.json   
-- docs 就是文档全部放在这个目录下   
----doc1.md  
----doc2.md   
``` 

那么 book.json 中 root 的值应该是 `./docs`。     

```
head_title
head_description
head_keywords
```
上面三个参数在标准的 GitBook 框架里面没有，是我们自己改造的，就是页面 SEO 相关的 title、description、keywords。  

还有一个参数需要留意 `prefix`，它是通过插件自动生成 `sitemap.xml` 网站地图的前缀路径，我们当前生成的地图为：<http://zitiao.org/deploy/sitemap.xml>      

其它没有提及的参数保持原样，如果想要深入了解，请参考 GitBook 的官方英文文档：<https://toolchain.gitbook.com/config.html>   

## 三、修改 book.js 文件

按照上面章节中 book.js 各个字段的含义进行修改，修改成适合自己项目的就可以了。

## 四、填充文档内容

### 1、SUMMARY.md
完成目录文档，可以参考本文档的 `SUMMARY.md` 文件的写法，比较简单，不展开了：   

<https://github.com/zitiaocn/deploy/edit/master/SUMMARY.md>

### 2、撰写具体文档内容
不懂 Git 也没关系，可以直接在 GitHub 的网页端在线编辑。

**完成上面的所有工作，下一步就是 `项目部署`，请看下一章。**


