# 用Github记笔记，做图库和MarkDown笔记文档空间
> Written with [StackEdit中文版](https://stackedit.cn/).
> 作者：[LeonYew | 黎恩瑜](http://leonyew.fun)
> 日期：2024年1月7日

# 引言
**前排提示：可以不看**

请原谅我的思维很跳跃，我常常会因为做一个东西，但是缺其他东西，然后把注意力转到其他东西，跳了好几次再转回来，我暂且把这种现象叫做**高墙悖论**。这么折腾的过程也是我写这篇文章的原因：

需要做Unity的期末作业 --> 需要写文档 --> 需要记录一些灵感 --> MarkDown --> 需要一个博客存放 --> 搭建halo --> 需要Docker -->需要DockerCompose --> 配置DockerCompose --> halo需要设置主题的HTML语言为中文，否则浏览器会弹出翻译 --> 自己修改官方的主题包 --> halo自带的编辑器不好用 --> StackEdit --> 需要连接到我自己的Github --> 配置Github文档空间和Github图库

总之，绕了一大圈之后，我是终于完成了可以开始记录的我的开发日志，但其实这一切我完全可以单独新建一个实验文档以外的docx文档就可以了，没办法，**人生乐在折腾**。
# 一、使用StackEdit中文版写MarkDown
## 你不会MarkDown?
没事，你进入到StackEdit中之后，会有一份Welcome的文档，里面有StackEdit支持的各种语法，**不用记，忘记的时候查一下就行，熟能生巧**。
## 中文版 or 国际版？
这里我推荐你使用StackEdit中文版，为什么？见下表：
||StackEdit中文版|StackEdit|
|--|--|--|
|文档空间|✅**Gitea** <br>✅**Gitee** <br>✅GitHub <br>✅GitLab <br>✅Google Drive <br>✅CouchDB|✅GitHub <br>✅GitLab <br>✅Google Drive <br>✅CouchDB |
|图床支持|✅当前文档空间<br> ✅SM.MS <br> ✅自定义图床账号<br> ✅Gitea仓库<br> ✅GitHub仓库|✅Google Photos|
|网址|stackedit.cn|stackedit.io|
|其他|没有广告和bar弹窗|有赞助bar弹窗|
所以我建议你使用中文版，毕竟支持Gitee，毕竟哪天梯子倒了，还可以访问 *StackEdit 中文版* 和自己的 *笔记仓库* 。
## StackEdit的使用
接下来的教程，我默认你使用了 StackEdit 中文版。
打开 stackedit.cn 你会看到如下界面：
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/6PaJoOKpDcEYOC03.png)

在说明一下StackEdit有什么用：
- 一款网页的MarkDown编辑器
- 不用登陆，用的是浏览器本地缓存，所以，不要随便清理浏览器缓存，也不要使用隐身模式！
- 可以连接到云端仓库，把文件同步上去

我们继续来，点击开始写作，你就会来到StackEdit的欢迎文档（Welcome File）
![输入图片说明](https://raw.githubusercontent.com/LeonYew-SWPU/FileTem/main/imgs/2024-01-07/q2Xhb5XeZmUPL5IL.png)

你可以点击下一步学习一下SE的基本操作，我就直接跳过了。点击左上角打开文件资源管理器，可以查看文件有哪些。接下来，我们将SE链接到Github，并且
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEwNDA0MjI1MjNdfQ==
-->