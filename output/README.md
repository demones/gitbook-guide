# 电子书输出
电子书输出支持 html pdf epub 和 mobi

## html
执行命令 gitbook build 即可生成 html 格式的电子书

## pdf

对于生成 pdf 格式的书，直接运行 `gitbook pdf` 会报以下错误

`Error: Need to install ebook-convert from Calibre`

通过网上查找相关资料，解决如下
1. 安装 [Calibre](http://calibre-ebook.com/) 
2. 设置环境变量，可以参考这里 https://github.com/GitbookIO/gitbook/issues/333

   export PATH=$PATH:/Applications/calibre.app/Contents/MacOS

   或者利用命令 ln -s /Applications/calibre.app/Contents/MacOS/ebook-convert /usr/local/bin

3. 然后执行 gitbook pdf 我们可爱的 pdf 格式电子书就生成了

## epub mobi
有了上面 生成 pdf 所需的 Calibre，生成这两种格式的书就很轻松了，执行以下命令搞定

```
gitbook epub
gitbook mobi
```