# 在线编辑电子书
## 注册自己的账号
登录官网 https://www.gitbook.com/ 注册一个自己的账号，这里推荐使用 github 的账户来注册

## 创建自己的电子书
创建电子书后可以在线编辑、在线生成 pdf、ePub 或 Mobi 格式的电子书
目前官网在线编辑功能还是比较强大的，包括新建文章，目录，上传已有写好的电子书。还可以选择语言
当然对于国内的朋友来说，网速有点慢，你懂得

## 本地编辑电子书
我们可以通过下载官网上的电子书到本地来编辑，编辑好后再利用 git 命令来提交，实际上 gitbook 也是基于 git 来搭建的。
当前只支持 https clone，不支持 git clone
比如执行以下命令，下载到本地

` git clone https://git.gitbook.com/hopefuture/h5-learning.git`

本地编辑好后，用 git 命令提交到 gitbook 上

这里介绍一款本地编辑 Markdown 软件，国产的，简单易用

https://www.zybuluo.com

可在线编辑，也可下载客户端本地编辑

## 发布到 github 上

写完电子书，有的同学想把电子书发布到 github 上，我们不用手工放到 github 上，gitbook 替我们想到了，而且提供了很好的解决方案。

### 从 gitbook 导入到 github 上
从 gitbook 中选择你要导入的电子书，点击 setting，以下是示例链接

`https://www.gitbook.com/book/hopefuture/h5-learning/settings`

选择 Export to GitHub ，然后进入到 github 上，按照提示进行操作就可以把 gitbook 中的资源导入到 github 上了

这里需要注意一下：**如果还没有跟 github 关联账户或者没有设置许可（permission）**，需要点击 Manage Permission 按钮来设置

唯一有点遗憾的是，采用这种方式，提交到 gitbook 上的内容不能自动同步到 github 上 (也可能是没有找到设置，待处理)

### 从 github 上导入到 gitbook 上

在 github 上创建的电子书（或者从 gitbook 导入的）通过设置 GitHub Repository 来与 github 管理，详见以下示例链接

`https://www.gitbook.com/book/hopefuture/h5-learning/settings/github`

设置好后，就可以往 github 中提交代码，对应的也会提交到 gitbook 中

如果关联过程中遇到一些问题，可以参考这里
https://help.gitbook.com/github/index.html





