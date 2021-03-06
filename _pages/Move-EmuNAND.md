---
title: "迁移EmuNAND数据"
permalink: /move-emunand.html
---

本节是附加章节，将你的EmuNAND的数据迁移到新的SysNAND自制系统中，然后删除EmuNAND分区。注意EmuNAND和RedNAND是[同一概念](http://3dbrew.org/wiki/NAND_Redirection)的两种略微不同的实现。
{: .notice--info}

你会丢失你的GBA VC和DsiWare存档！
{: .notice--danger}

**你必须已经安装了arm9loaderhax + Luma3DS才能执行接下来的操作。**
{: .notice--danger}

#### 你需要

* 已有的EmuNAND
* 最新版本的[GodMode9](https://github.com/d0k3/GodMode9/releases/latest)

#### 操作指南

1. 解压`GodMode9`压缩包，复制`GodMode9.bin`到你SD卡的`/luma/payloads/`目录下，并重命名`GodMode9.bin`为`up_GodMode9.bin`
2. 将SD卡插回你的3DS
3. 按住(Start)键开机，进入Hourglass9
4. 进入"EmuNAND Backup/Restore"，选择"EmuNAND Backup"，将你的EmuNAND备份到`NANDmin_emu.bin`
5. 按(B)键返回到主菜单
6. 进入"SysNAND Backup/Restore"，选择"SysNAND Restore (keep a9lh)"，从`NANDmin_emu.bin`文件恢复EmuNAND
7. 按(Select)键弹出你的SD卡
8. 将SD卡插入电脑，复制`/files9/`文件夹下的`NANDmin_emu.bin`和`NANDmin_emu.bin.sha`文件到一个安全的位置
  + 在多个位置进行备份
  + 备份文件可以在将来出现错误时将你的机器救砖
  + **你的备份文件应该符合[这个](nand-size)页面上列出的大小。如果不是，你应该删除它并重新做一次！**
9. 删除`/files9/`文件夹下的`NANDmin_emu.bin`文件
10. **备份你SD卡上的所有文件到你的计算机上。SD卡上的所有文件在接下来将被删除**
11. 将SD卡插回3DS
12. 按住(方向上)键开机，重启进入GodMode9
13. 按(Home)键，打开行动菜单
14. 选择"SD format menu"
15. 按(A)键确定
16. 选择"No EmuNAND"
17. 选择"Auto"
18. 输入屏幕提示的组合键以确定
19. 格式化完成后，同时按(R)键和(B)键，弹出你的SD卡
16. 将SD卡插入电脑，然后将所有文件重新复制回SD卡
  + 确保你使用备份的`arm9loaderhax.bin`文件替换了SD卡上已有的文件
18. 将你的SD卡插回你的3DS
19. 按(A)键重新加载你的SD卡
20. 按(Start)键重启
19. 如果出现黑屏，[参见这个问题排查](troubleshooting#ts_sys_down)

返回到[安装arm9loaderhax](installing-arm9loaderhax)继续操作。
