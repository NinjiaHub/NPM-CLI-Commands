# npm bugs

### 梗概

```shell
npm bugs [<pkgname>]

aliases: issues
```

### 描述

该命令会尝试定位一个npm包 bug 跟踪页面 URL 的位置，然后尝试使用 **--browser** 项中配置的命令在浏览器中打开该 URL。

如果命令后没有写包的名字，则该命令会在当前目录下查找 **package.json** 文件，然后使用其中的 **name** 属性的值，重复上面的步骤。

### 配置

#### browser

* 默认：OS X：“**open**”；Windows：“**start**”；Others：“**xdg-open**”
* 类型：String

**npm repo** 命令用来打开仓库网站的**命令**。

#### registry

* 默认：[https://registry.npmjs.org/](https://registry.npmjs.org/)
* 类型：url

npm包注册表地址的基础URL。

### See Also

* [npm-docs](https://github.com/NinjiaHub/NPM-CLI-Commands/blob/master/documents/npm-docs.md "npm-docs")
* [npm-view](https://github.com/NinjiaHub/NPM-CLI-Commands/blob/master/documents/npm-view.md "npm-view")
* [npm-publish](https://github.com/NinjiaHub/NPM-CLI-Commands/blob/master/documents/npm-publish.md "npm-publish")
* [npm-config](https://github.com/NinjiaHub/NPM-CLI-Commands/blob/master/documents/npm-config.md "npm-config")

## 原文链接

* [npm-bugs](https://docs.npmjs.com/cli/bugs)

## 声明

本文翻译源内容来自网络，即NPM官方CLI文档，如有版权问题请联系译者。

侵删。

内容如有不恰当或错误，敬请指正。

译者邮箱：<web.taox@gmail.com>

## Translator Info

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>
