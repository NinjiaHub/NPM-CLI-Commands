# npm help-search

**查找 npm 帮助文档**

### 梗概

```shell
npm help-search <text>
```

### 描述

### 配置

#### long

* 类型：Boolean
* 默认：false

如果 **long** 标志设置为 **true**，**help-search** 命令会显示出查找的 **text** 出现在文档中的位置，如：

```shell
$ npm help-search star -l

npm help restart                                                         star:16
————————————————————————————————————————————————————————————————————————————————
npm-restart(1) -- Restart a package
===================================
## SYNOPSIS
    npm restart [-- <args>]


npm help scripts                                                         star:16
————————————————————————————————————————————————————————————————————————————————
Run by the `npm stop` command.
* prestart, start, poststart:
  Run by the `npm start` command.
* prerestart, restart, postrestart:
...
```

如果为 **false**，**help-search** 命令只列出找到的供 **help** 命令使用的 **主题(topics)**。

### See Also

* [npm](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm "npm")
* [npm-help](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-help "npm-help")

## 原文链接

* [npm-help-search](https://docs.npmjs.com/cli/help-search)

## 声明

本文翻译源内容来自网络，即NPM官方CLI文档，如有版权问题请联系译者。

侵删。

内容如有不恰当或错误，敬请指正。

译者邮箱：<web.taox@gmail.com>

## Translator Info

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>
