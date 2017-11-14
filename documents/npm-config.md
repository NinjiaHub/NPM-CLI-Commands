# npm config

**管理 npm 配置文件**

### 梗概

```shell
npm config set <key> <value> [-g|--global]
npm config get <key>
npm config delete <key>
npm config list [-l] [--json]
npm config edit
npm get <key>
npm set <key> <value> [-g|--global]

aliases: c
```

### 描述

npm 从命令行、环境变量、**npmrc** 文件获取配置信息，有些情况下，也会从 **package.json** 文件获取。

戳👉[npmrc](https://github.com/NinjiaHub/Tools-Tricks/blob/master/npm/documents/config-npm/npmrc.md)获取更多关于 **npmrc** 的信息。

**npm config** 命令可以用来更修／修改用户或者全局 **npmrc** 文件的内容。

### 子命令

`npm config` 支持下列子命令：

#### set

```shell
npm config set key value
```

设置配置中 **key** 项的值为 **value**。

如果没有传 **value**，则默认为 **true**。

#### get

```shell
npm config get key
```
获取配置项的值。

#### list

```shell
npm config list
```

列出所有的配置信息。使用 **-l** 选项，输出结果仍为默认结果；使用 **--json** 选项会以 JSON 格式输出所有配置项。

#### delete

```shell
npm config delete key
```

从所有配置配置文件中删除关于 **key** 选项的配置。

#### edit

```shell
npm config edit
```

在编辑器中打开配置文件。如果使用了 **--global** 标志，则编辑的是全局配置文件。

## 原文链接

* [npm-config](https://docs.npmjs.com/cli/config)

## 声明

本文翻译源内容来自网络，即NPM官方CLI文档，如有版权问题请联系译者。

侵删。

内容如有不恰当或错误，敬请指正。

译者邮箱：web.taox@gmail.com。

## Translator Info

* [GitHub](https://github.com/Tao-Quixote)
* Email: web.taox@gmail.com
