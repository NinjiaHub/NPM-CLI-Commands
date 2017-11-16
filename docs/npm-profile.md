# npm profile

**修改注册表中的设置**

### 梗概

```npm
npm profile get [--json|--parseable] [<property>]
npm profile set [--json|--parseable] <property> <value>
npm profile set password
npm profile enable-2fa [auth-and-writes|auth-only]
npm profile disable-2fa
```

### 描述

修改注册表中的信息。如果使用的不是npm注册表则该命令无效。

* **npm profile get [<property>]**：展示注册表中的所有信息，或者指定项的信息。结果如下：

```text
+-----------------+---------------------------+
| name            | example                   |
+-----------------+---------------------------+
| email           | me@example.com (verified) |
+-----------------+---------------------------+
| two factor auth | auth-and-writes           |
+-----------------+---------------------------+
| fullname        | Example User              |
+-----------------+---------------------------+
| homepage        |                           |
+-----------------+---------------------------+
| freenode        |                           |
+-----------------+---------------------------+
| twitter         |                           |
+-----------------+---------------------------+
| github          |                           |
+-----------------+---------------------------+
| created         | 2015-02-26T01:38:35.892Z  |
+-----------------+---------------------------+
| updated         | 2017-10-02T21:29:45.922Z  |
+-----------------+---------------------------+
```

* **npm profile set \<property> \<value>**：设置指定项的值。可以通过该方式设置如下项的值：email，fullname，homepage，freenode，twitter，github。
* **npm profile set password**：重置密码。该命令是交互式的，在使用时会提示输入当前密码和新密码。如果开启了[2FA](https://github.com/NinjiaHub/Tools-Tricks/blob/master/npm/documents/getting-started/npm%E4%B8%AD%E4%BD%BF%E7%94%A82FA.md)，还会要求输入OTP。
* **npm profile enable-2fa [auth-and-writes|auth-only]**：开启2FA，默认使用**auth-and-writes**模式。模式详情：
	* **auth-only**：在登陆或者修改账户认证方式的时候要求输入OTP。涉及前面的操作时，[npm官网](npmjs.com)和命令行都要求输入OTP。
	* **auth-and-writes**：包括在**auth-only**模式中需要输入OTP的场景，以及发布模块、设置**latest**标签、通过**npm access**和**npm owner**修改权限，都需要输入OTP。
* **npm profile disable-2fa**：关闭双因子验证(2FA)。

### 详情

`npm profile`命令的所有子命令都接受`--json`和`--parseable`选项，并且会根据输入的选项定制输出结果。其中一些子命令在非npm官网的注册表中可能是无效的。

### See Also

* [npm-config](https://github.com/NinjiaHub/NPM-CLI-Commands/blob/master/documents/npm-dist-tag.md)

## 原文链接

* [npm-profile](https://docs.npmjs.com/cli/profile)

## 声明

本文翻译源内容来自网络，即NPM官方CLI文档，如有版权问题请联系译者。

侵删。

内容如有不恰当或错误，敬请指正。

译者邮箱：web.taox@gmail.com。

## Translator Info

* [GitHub](https://github.com/Tao-Quixote)
* Email: web.taox@gmail.com
