# DUOWeb配置说明

[TOC]

## 写在前面

1. 本项目的所有配置文件均为`json`格式。一个`json`文件的格式大约如下：

```json
{
    "节点1": "",
    "节点2": [
        "第一项",
        "第二项",
        "第三项"
    ],
    ...
}
```

​		其中`{}`描述了一种”键 - 值对“（key - value pairs）的结构，如需描述一篇文章的几大要素：`{"标题": "...", "正文": "...", "作者": "..."}`。”键 - 值对“是一种无序的结构，即它只描述了”XX的XX是XX“的语义，并不对其组织的顺序做限制。

​		而`[]`描述了一种”列表“（list）的结构，如需描述一篇文章的几个作者甲乙丙丁：`{"作者": ["甲", "乙", "丙", "丁"]`。由于作者有排名先后关系，因此采用列表的形式描述。

​		通过这种配置方式，本项目可以抛弃后台，无需购买阿里云等云服务器，免费托管于第三方网站[GitHub](https://github.com)。Github提供免费的存储空间及全球可访问的公网链接。如果需要使用自己的域名，只需要将自己购买的域名绑定到GitHub提供的链接上即可。

2. 本项目的所有修改，创建文件，上传文件都需要在GitHub上登陆帐号再进行。

3. 本项目所有的文件（图片，视频，配置文件等）都在[https://github.com/duowebmaster/duowebresources](https://github.com/duowebmaster/duowebresources)

4. 本项目的源代码（如需后续升级开发）在[https://github.com/duowebmaster/duowebdev](https://github.com/duowebmaster/duowebdev)

5. **公开部署的网站为[https://duowebmaster.github.io/duoweb/](https://duowebmaster.github.io/duoweb/)**



## 配置文件一览

本项目初步有以下两个配置文件：

### config.json

位置：[https://raw.githubusercontent.com/duowebmaster/duowebresources/master/config.json](https://raw.githubusercontent.com/duowebmaster/duowebresources/master/config.json)

作用：是主要配置文件。logo，首页幻灯片，公司描述等都在这里配置。

### hongguozhuo.json

位置： https://github.com/duowebmaster/duowebresources/blob/master/hongguozhuo.json

作用：描述合伙人Hong Guozhuo的作品



## 如何配置

### 基础步骤

以修改`config.json`为例：

1. 打开GitHub上的配置文件（[https://github.com/duowebmaster/duowebresources](https://github.com/duowebmaster/duowebresources)）

2. 点击文件列表中的`config.json`

3. 点击这个🖊按钮

   ![](https://i.imgur.com/MMjmYpA.png)

4. **修改后点击最下面的`Commit Changes`保存修改。**

5. 可能需要等待几分钟缓存刷新使网站上的改动生效，如果没有生效则试一下`Ctrl + F5`来刷新浏览器缓存。

### 使用配置工具

`json`是一种使用非常广泛的数据描述格式，因此网上有许多在线的`json`修改器可供使用。例如这个[https://jsoneditoronline.org/](https://jsoneditoronline.org/)。

![](https://i.imgur.com/4pWNWa3.png)

可以将需要修改的`json`文件全文复制到这个网站的左栏，点击中间的▶按钮，修改完后点击中间的◀按钮重新生成文本，全文复制到GitHub中，最后Commit Changes。

### 如何上传图片

1. 打开GitHub上的配置文件（[https://github.com/duowebmaster/duowebresources](https://github.com/duowebmaster/duowebresources)）
2. 点击upload files
3. 点击choose your files，上传
4. 点击Commit Changes
5. **点击刚才创建的文件，点击在🖊按钮旁边的Raw按钮，复制浏览器上的网址。**
6. 粘贴到对应的地方，**记得加英文双引号`""`**

### 添加配置文件

因为项目提供的素材限制，我不知道其他两位合伙人的projects，（Photography部分也是），因此没有做其他两位合伙人的配置文件。如果需要添加其他两位合伙人的配置文件，应按照以下步骤进行：

1. 打开GitHub上的配置文件（[https://github.com/duowebmaster/duowebresources](https://github.com/duowebmaster/duowebresources)）
2. 点击Create New File。
3. 在Name Your File处写上任意文件名（如`guanyuan.json`）。
4. 将`hongguozhuo.json`原文复制过来，修改后点击最下面的Commit New File。
5. **点击刚才创建的文件，点击在🖊按钮旁边的Raw按钮，复制浏览器上的网址。**
6. 回到`config.json`，将复制出来的网址粘贴在对应的位置中`projects`字段后，**记得加英文双引号`""`**

## 配置选项说明

| 字段名                 | 说明                            | 备注                                                         |
| ---------------------- | ------------------------------- | ------------------------------------------------------------ |
| logo                   | 顶栏上的logo图片                | 因为需求文档中的logo复制不出来，因此我在网上随便找了一张图做代替 |
| logo.src               | logo的图片链接                  | 可以上传到GitHub或Imgur.com上，然后把链接复制过来            |
| logo.style             | 设置logo的长宽                  |                                                              |
|                        |                                 |                                                              |
| slides                 | 首页幻灯片                      |                                                              |
| slides[].src           | 图片链接                        |                                                              |
| slides[].title         | 图片标题                        |                                                              |
|                        |                                 |                                                              |
| profile                | profile页配置                   |                                                              |
| profile.content        | profile页说明                   |                                                              |
| profile.content.src    | 说明文件地址                    | 如需修改内容，请直接修改GitHub上的profile.txt                |
| profile.content.style  | 可以调节两边边距                |                                                              |
| profile.clients        | profile页客户图片               |                                                              |
| profile.clients.src    | 客户图片链接                    |                                                              |
| profile.clients.style  | 可以调节图片大小                |                                                              |
|                        |                                 |                                                              |
| story                  | story页的项目                   |                                                              |
| story[].images         | story项目图片                   |                                                              |
| story[].title          | story项目标题                   |                                                              |
| story[].description    | story项目描述                   |                                                              |
| story[].url            | story项目链接，点击后跳转到这里 |                                                              |
|                        |                                 |                                                              |
| projects               | 项目描述json文件链接            |                                                              |
| projects[].title       | 项目标题                        |                                                              |
| projects[].cover       | 相册封面                        |                                                              |
| projects[].detail      | 相册其他照片                    |                                                              |
| projects[].description | 相册描述                        | 该项可选，可有可无                                           |
|                        |                                 |                                                              |