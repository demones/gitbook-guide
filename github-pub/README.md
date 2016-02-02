# github 发布

## 本地编译
个人喜欢把源码和生成的电子书分别放在 master 和 gh-pages 分支下，所以需要按照以下步骤来操作

1. 执行命令 `gitbook build` 生成 html 格式的电子书，把生成的电子书 _book 复制一份
2. 执行命令 `git branch gh-pages` 创建分支 gh-pages，**注意：分支名称必须是 ph-pages**
3. 切换到分支 gh-pages 下 `git checkout gh-pages`
4. 删除掉源代码，即 .md 格式的文件，当然也可以不删除
5. 把之前生成的电子书复制到该目录下
6. 执行命令