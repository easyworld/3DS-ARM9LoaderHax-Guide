---
title: "Decrypt9（系统设置）"
permalink: /decrypt9-(mset).html
---

本教程要做的第一件事就是让你运行Decrypt9，它是一个多用途的工具，可以允许我们安装包含漏洞的2.1.0版本的固件。我们需要这一漏洞以便完成后续的破解。
{: .notice}

如果你的3DS之前已经破解，并安装了基于EmuNAND的自制系统，请务必注意本教程仅适用于SysNAND，教程内的步骤应当应用在你的SysNAND上。注意EmuNAND和RedNAND是[同一概念](http://3dbrew.org/wiki/NAND_Redirection)的两种略微不同的实现。
{: .notice--info}

#### 你需要

* 可以在你3DS正常工作的DS烧录卡
* 最新版本的[Decrypt9WIP](https://github.com/d0k3/Decrypt9WIP/releases/)

#### 操作指南

1. 在SD卡根目录下创建`files9`文件夹如果没有的话
2. 复制Decrypt9WIP压缩包的`Launcher.dat`和`Decrypt9WIP.dat`到你SD卡的根目录
3. 将SD卡重新插入你的3DS
4. 把Decrypt9压缩包的`Decrypt9.nds`放入你的烧录卡中
5. 用你的3DS运行烧录卡
6. 使用你的烧录卡启动`Decrypt9.nds`
7. 正确选择你系统的版本
  + 4.X.X -> "4.x Decrypt9WIP"
  + 6.X.X -> "6.x Decrypt9WIP"
8. 重启，然后进入系统设置（System Settings），然后“其它选项”（"Other Settings"），然后"Profile"，最后"Nintendo DS Profile"（译者注：没错，就是传说中的414）
9. 如果漏洞利用成功，Decrypt9将会启动

继续进行[2.1.0 ctr迁移](2.1.0-ctrtransfer)
{: .notice--primary}
