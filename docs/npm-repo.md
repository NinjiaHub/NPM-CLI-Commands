# npm repo

**在浏览器打开nnpm包的仓库地址页面**

### 梗概

```shell
npm repo [<pkg>]
```

### 描述

该命令会尝试解析出npm包仓库的URL地址，然后通过 **--browser** 项中配置的命令来打开该URL。

如果命令后没有写包的名字，则该命令会在当前目录下查找 **package.json** 文件，然后使用其中的 **name** 属性的值，重复上面的步骤。

### 配置

#### browser

* 默认：OS X：“**open**”；Windows：“**start**”；Others：“**xdg-open**”
* 类型：String

**npm repo** 命令用来打开仓库网站的**命令**。

**译者注：注意这里的 browser 中配置的是 npm repo 命令用来打开浏览器的命令，而不是浏览器的名字。npm使用第三方npm包 - opener，来完成所有跟打开浏览器相关的动作，其中opener包的底层实现是通过 Node 中的 child_process.exce 来调用系统命令的，其中 OS X 系统打开文件的命令为 open，windowns中为 start， 以及其他 \*nix 系统打开文件的命令为 xdg-open。所以 browser中设置的其实为各个操作系统中内置的打开文件的命令名称。**

### See Also

* [npm-docs](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-docs "npm-docs")
* [npm-config](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-config "npm-config")

## 原文链接

* [npm-repo](https://docs.npmjs.com/cli/repo)

## 声明

本文翻译源内容来自网络，即NPM官方CLI文档，如有版权问题请联系译者。

侵删。

内容如有不恰当或错误，敬请指正。

译者邮箱：<web.taox@gmail.com>

## Translator Info

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>
