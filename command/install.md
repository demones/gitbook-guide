# 安装与运行

Gitbook 是基于 Node.js 环境运行的，首先需要安装 Node.js，如果之前没接触过 Node.js 可以参照官网或是网上其他人写的安装步骤

## 全局安装 gitbook

`$ npm install gitbook-cli -g`

注意是 gitbook-cli 而不是 gitbook

## 创建一个电子书目录文件，然后初始化电子书项目
`$ gitbook init`
会生成电子书必须的两个文件 README.md 和 SUMMARY.md

## 编写书的目录结构
在 SUMMARY.md编写目录结构，可以支持多级目录，以下给出一例子

```
* [section 1](section1/README.md)
    - [section 1-1](section1/README.md)
       * [example 1](section1/section 1-1/example1.md)
       * [example 2](section1/section 1-1/example2.md)
    - [section 1-2](section1/README.md)
      * [example 1](section2/section 1-2/example1.md)
      * [example 2](section2/section 1-2/example2.md)
* [section 2](section2/README.md)
    * [example 1](section2/example1.md)
```

SUMMARY.md 文件中的目录，可以一开始就设置好，也可以边写文章边设置。如果开始设置好，执行 gitbook init 
会根据目录结构动态的生成对应的物理路径，对于已经规划好目录的电子书来说，建议采取这种方式

## 启动服务

执行以下命令，可以启动电子书服务，该服务会实时监测电子书内容的，如有变化，则会刷新浏览器

`gitbook serve`

然后就可以在浏览器中打开 http://localhost:4000/

## 编译打包电子书

`gitbook build`

默认会打包到 _book 下
