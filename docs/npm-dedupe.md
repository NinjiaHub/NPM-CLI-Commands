# npm dedupe

**npm包去重**

### 梗概

```shell
npm dedupe
npm ddp

aliases: find-dupes, ddp
```

### 描述

该命令会搜索本地npm包树，然后尝试通过将被依赖的npm包往树结构上层移动的方式来简化总体的结构，以便于对这些npm包有依赖的npm包可以更高效地共享这些被依赖的npm包。

例如，假设有如下依赖结构：

```shell
a
+-- b <-- depends on c@1.0.x
|   `-- c@1.0.3
`-- d <-- depends on c@~1.0.9
    `-- c@1.0.10
```

在这种情况下，**npm dedupe** 命令会将目录转换为下面的结构：

```shell
a
+-- b
+-- d
`-- c@1.0.10
```

因为 Node 的模块查找机制的分层特性，**b** 和 **d** 都会在依赖树的根目录中找到它们依赖的 **c** 包。

去重算法会遍历依赖树，然后将每一个依赖(npm包)尽量往依赖树的顶层移动，即使没有重复的依赖也会向上移动依赖。这会使依赖树扁平且尽量去重。

如果一个合适的依赖版本已经存在于依赖树中的目标位置，去重算法不会移动这个依赖，但是该依赖的其他版本将会被删除。

去重作用于整个依赖树，所以任何参数都会被忽略。

#### Modules

注意，该操作会改变依赖树的结构，但是并不会安装新的模块。

### See Also

* [npm-ls](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-ls "npm-ls")
* [npm-update](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-update "npm-update")
* [npm-install](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-install "npm-install")

## 原文链接

* [npm-dedupe](https://docs.npmjs.com/cli/dedupe "npm-dedupe")

## 声明

本文翻译源内容来自网络，即NPM官方CLI文档，如有版权问题请联系译者。

侵删。

内容如有不恰当或错误，敬请指正。

译者邮箱：<web.taox@gmail.com>

## Translator Info

* [GitHub](https://github.com/Tao-Quixote)
* Email: <web.taox@gmail.com>
