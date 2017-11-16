# npm prune

**移除无关的包**

### 梗概

```shell
npm prune [[<@scope>/]<pkg>...] [--production]
```

### 描述

该命令用来移除**无关**的包。如果 **npm prune** 命令后填写了包名，则只有匹配这些包名的包才会被移除。

**无关的包**指不在 ***父包(parent's package)*** 依赖列表中的包。

如果指定了 **--production** 标志，或者环境变量 **NODE_ENV** 的值设置为 **production**，则该命令会移除 **package.json** 文件中的 **devDependencies** 部分中列出的依赖。如果设置了 **--production=false** ，即使设置 **NODE_ENV** 为 **production** 也是无效的()。

**译者注**：即 **--production=false** 的优先级高于 **NODE_ENV**，这是符合开发规范的，通常情况下，当命令中指定的选项和环境变量以及配置文件中的配置有冲突时，命令行中指定的选项优先级高于环境变量以及配置文件中的配置，符合就近原则。

### See Also

* [npm-uninstall](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-uninstall)
* [npm-ls](https://NinjiaHub.github.io/NPM-CLI-Commands/docs/npm-ls)

## 原文链接

* [npm-prune](https://docs.npmjs.com/cli/prune)

## 声明

本文翻译源内容来自网络，即NPM官方CLI文档，如有版权问题请联系译者。

侵删。

内容如有不恰当或错误，敬请指正。

译者邮箱：web.taox@gmail.com。

## Translator Info

* [GitHub](https://github.com/Tao-Quixote)
* Email: web.taox@gmail.com
