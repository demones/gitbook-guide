# gitbook 配置与插件

自定义配置与插件是在 book.json 配置的
```json
{
    "variables": {
        "myVariable": "Hello World"
    }
}
```
上面给出的代码，配置了一个全局模板变量 `myVariable`，我们可以通过 `{{ book.myVariable }}` 来调用改变量

### Plugin
插件可以在[这里](http://plugins.gitbook.com/)下载安装和配置

```json
{
    "plugins": ["myPlugin", "anotherPlugin"]
}
```
设置好插件后，需要运行命令 `gitbook install` 来安装插件

#### 插件 [gitbook-plugin-search-pro](https://plugins.gitbook.com/plugin/search-pro)
该插件支持中文搜索，在安装过程中可能会报 `node-gyp rebuild` 错误，解决方法，先删除已安装的插件，
运行命令 `npm install nodejieba`，再 `gitbook install`

### [Emphasize](https://plugins.gitbook.com/plugin/emphasize) 给文字加背景色

例子
```
This text is {% em %}highlighted !{% endem %}

This text is {% em %}highlighted with **markdown**!{% endem %}

This text is {% em type="green" %}highlighted in green!{% endem %}

This text is {% em type="red" %}highlighted in red!{% endem %}

This text is {% em color="#ff0000" %}highlighted with a custom color!{% endem %}
```
预览效果

This text is {% em %}highlighted !{% endem %}

This text is {% em %}highlighted with **markdown**!{% endem %}

This text is {% em type="green" %}highlighted in green!{% endem %}

This text is {% em type="red" %}highlighted in red!{% endem %}

This text is {% em color="#ff0000" %}highlighted with a custom color!{% endem %}

### [splitter](https://plugins.gitbook.com/plugin/splitter) 侧边栏的宽度可以自由调节

### [include-codeblock](https://plugins.gitbook.com/plugin/include-codeblock) 代码块包含引入的文件

使用代码块格式显示所包含文件的内容，该文件必须存在，否则会报错，可以截取显示部分包含内容

例子

[import:1-5, book.json](../book.json)

### [tbfed-pagefooter](https://plugins.gitbook.com/plugin/tbfed-pagefooter)

为页面添加底部页脚

```json
"plugins": [
   "tbfed-pagefooter"
],
"pluginsConfig": {
    "tbfed-pagefooter": {
        "copyright":"Copyright &copy 2016",
        "modify_label": "最后修改时间：",
        "modify_format": "YYYY-MM-DD HH:mm:ss"
    }
}
```
### [toggle-chapters](https://plugins.gitbook.com/plugin/toggle-chapters)
左侧目录可以折叠

```json
"plugins": ["toggle-chapters"]
```
### [sectionx](https://plugins.gitbook.com/plugin/sectionx)
页面分块显示插件

```json
"plugins": ["sectionx"]
```

例子

gitbook-plugin-sectionx
===

<!--sec data-title="Introduction" data-id="intro" ces-->
This page is implemented using the two plugins developed by me: ```gitbook-plugin-sectionx```, please check the [Github repo](https://github.com/ymcatar/gitbook-plugin-sectionx) for the plugin.

The source code for this page is available [here](https://raw.githubusercontent.com/ymcatar/gitbook-test/master/testing_sectionx.md).
<!--endsec-->

<!--sec data-title="Example" data-id="section1" ces-->
This is a section that is by default visible (with ```data-show=true```). You can toggle this with the button in the title. The next section is hidden by default, you can add a custom button to toggle it (see GitHub for the syntax).

<button class="section" target="section2" show="Show the next  hidden section" hide="Hide the next hidden section"></button>
<!--endsec-->

<!--sec data-title="Hidden Section" data-id="section2" data-show=false ces-->
This section can only be opened with that button.
<!--endsec-->


源代码看这里 https://github.com/ymcatar/gitbook-test

该插件的作者还实现了一些其他插件，详情点击这里 https://github.com/ymcatar

### [baidu](https://plugins.gitbook.com/plugin/baidu)
百度统计插件

你需要在百度统计中添加一个 token，比如：`c12134efe8099063bacebecb25df3b7d`
然后配置

```json
{
    "plugin": ["baidu"],
    "pluginsConfig": {
        "baidu": {
            "token": "YOUR TOKEN"
        }
    }
}

```

### 分享
可以这样配置

```json
"sharing": {
    "weibo": true,
    "facebook": true,
    "twitter": true,
    "google": false,
    "instapaper": false,
    "vk": false,
    "all": [
        "facebook", "google", "twitter",
            "weibo", "instapaper"
    ]
}
```

## 代码高亮
gitbook 中代码高亮是基于 [highlightjs](https://highlightjs.org/)实现的

## 参考资料
* [Gitbook 实用配置及插件介绍](http://blog.csdn.net/zhangjk1993/article/details/50380403)
* [Gitbook 实用配置及插件介绍 - gitbook 版](http://zhangjikai.com/gitbook-use/)
