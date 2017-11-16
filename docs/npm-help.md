# npm help

**获取 npm 中的相关命令的帮助文档**

### 梗概

```shell
npm help <term> [<terms..>]
```

### 描述

如果提供给一个 **主题(topic)**，即想查看的帮助项，则显示相关的文档页面。

如果该 **主题** 不存在，或者提供了多个项，则使用 **help-search** 命令查找相关匹配。注意，如果 **help-search** 只匹配到一个单独的对象，则会将该对象所对应的 **主题** 会作为 **help** 命令的参数，所以，唯一匹配与指定一个 **主题** 是等价的。

**译者注**：如果匹配到多个相关对象，则会使用表格的形式将相关的内容列出来，如下：

```shell
$ npm help star stars

Top hits for "star" "stars"
————————————————————————————————————————————————————————————————————————————————
npm help index                                                    star:6 stars:1
npm help stars                                                    star:4 stars:2
npm help restart                                                         star:16
npm help scripts                                                         star:16
npm help package.json                                                     star:8
npm help start                                                            star:6
npm help star                                                             star:6
npm help run-script                                                       star:6
npm help coding-style                                                     star:5
npm help config                                                           star:4
npm help developers                                                       star:3
npm help test                                                             star:2
npm help stop                                                             star:2
npm help version                                                          star:1
npm help package-lock.json                                                star:1
npm help bugs                                                             star:1
npm help install                                                          star:1
npm help repo                                                             star:1
npm help search                                                           star:1
npm help disputes                                                         star:1
npm help docs                                                             star:1
npm help folders                                                          star:1
npm help semver                                                           star:1
npm help package-lock                                                     star:1
————————————————————————————————————————————————————————————————————————————————
(run with -l or --long to see more context)
```

### 配置

#### viewer

* 默认：Posix系统 - **man**；Windows - **browser**
* 类型：path

查看**帮助内容**的程序。

如果设置为 **browser**，则使用系统默认浏览器查看 **HTML** 版的帮助内容。

### See Also

* [npm](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm "npm")
* [npm-config](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-config "npm-config")
* [npm-help-search](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-help-search "npm-help-search")

## 原文链接

* [npm-help](https://docs.npmjs.com/cli/help)

## 声明

本文翻译源内容来自网络，即NPM官方CLI文档，如有版权问题请联系译者。

侵删。

内容如有不恰当或错误，敬请指正。

译者邮箱：<web.taox@gmail.com>

## Translator Info

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>
