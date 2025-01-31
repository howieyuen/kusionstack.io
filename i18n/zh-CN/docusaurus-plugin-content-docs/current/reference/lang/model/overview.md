---
sidebar_position: 0
---

# Overview

KCL 是面向配置的编程语言，通过内置模块、KCL 模块和插件模块提供工程化的扩展能力。

![](/img/docs/reference/lang/model/kcl-module.png)

用户代码中不用导入直接使用 builtin 的函数（比如用 len 计算列表的长度、通过 typeof 获取值的类型等），而对于字符串等基础类型也提供了一些内置方法（比如转化字符串的大小写等方法）。对于相对复杂的通用工作则通过标准库提供，比如通过 import 导入 math 库就可以使用相关的数学函数，可以通过导入 regex 库使用正则表达式库。而针对 KCL 代码也可以组织为模块，比如 Konfig 大库中将基础设施和各种标准的应用抽象为模块供上层用户使用。此外还可以通过 Plugin 机制，采用 Python 为 KCL 开发插件，比如目前有 meta 插件可以通过网络查询中心配置信息，app-context 插件则可以用于获取当前应用的上下文信息从而简化代码的编写。
