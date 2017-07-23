# 项目介绍

**思路：通过将 Wiki 文档内容的仓库托管在 GitHub 之上，并且将 GitBook 框架的代码放在仓库中 ，然后找一台有 Node.js 环境的服务器，通过简单的几行命令就能部署成功，十分钟内能搞定。从而具备多人协作、版本控制、Markdown 写作、代码高亮、实时更新的特性。**

## 一、效果展示

### 1、Material Design 中文版（有侧边栏菜单）
- 页面效果：<http://zitiao.org/material-design/>
- 文档仓库：<https://github.com/zitiaocn/material-design>

![](http://om0iml27u.bkt.clouddn.com/2017/02/ti8wn.jpg)

### 2、GitBook Help Center（无侧边栏菜单）
- 页面效果：<https://help.gitbook.com/>
- 文档仓库：<https://github.com/GitbookIO/help.gitbook.com>

![](http://cdn.zitiao.org/deploy/s5daq.jpg)     
    
![](http://cdn.zitiao.org/deploy/s011v.jpg)

## 二、功能特性

### 1、页面美观       
主要体现在两个方面：其一，页面的外观，请回头看看上面的效果图。其二，链接的格式，如下：   

- GitBook 链接示例：<http://zitiao.org/material-design/usability/accessibility.html>
- MDwiki 链接示例：<http://dynalon.github.io/mdwiki/#!layout.md> （我个人见不得 `#`、`!` 之类的字符）

### 2、多人协作 & 版本控制
文档内容托管于 GitHub 之上，GitHub 本身就具备 `多人协作` 和 `版本控制` 的功能。当然所有的 Git 托管平台都可以，比如说国外的 GitLab、Bitbucket，或者国内的 git.oschina.net、coding.net 都行。

如果希望仓库私有，国外产品推荐 Bitbucket，因为他私有仓库免费，而 GitHub 私有仓库收费。国内的好像私有仓库都免费，在安全性和稳定性方面可能不如 Bitbucket。

### 3、Markdown 写作
文档内容托管于 GitHub 之上，GitHub 本身就具备 `Markdown 写作` 的功能。  

### 4、代码高亮
通过 GitBook 的插件能很容易支持代码高亮（这就是站在巨人的肩膀上的好处）。

### 5、实时更新
通过给 GitHub 仓库配置 `webhook` 进行 push 时的消息推送，能触发服务器实时更新（服务器上需要些代码）。

### 6、一键部署
只需要简单的几行命令就部署完毕。

## 三、所需资源

唯一的一个条件就是，一台支持 Node.js 的服务器（公网和内网服务器都行）。

## 四、交流学习

欢迎加群详聊

![](http://cdn.zitiao.org/deploy/weixinqun.jpeg)

如果扫码加群不成功，请添加四勾的个人微信，再由四勾邀请入群，加好友时请填写验证信息「字条网加群」

添加 `四勾 4J` 个人微信 `vincent4j`。

via <http://4jplus.com>



