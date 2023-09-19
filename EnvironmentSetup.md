# Environment setup/环境搭建

## How to use C++ in Mac/ Mac 中

- 需要安装 xcode 作为 Cpp的运行环境
- 检查是否安装XCode： xcode-select -p
  - 安装： 输出 Xcode 的安装路径
  - 未安装： 输出 ‘xcode-select: command not found’
- 安装方法：
  - A： 软件商店安装XCode
  - B： 使用命令行安装 Xcode Command Line Tools： xcode-select --install // 它是 Xcode 的一部分，包含开发所需的一些工具和库。

## In Linux / Linux 中 

- [参考文档](https://www.freecodecamp.org/chinese/news/5-ways-to-use-linux-on-a-windows-machine/)
  - 其中，我选择： 
    - 1. （本地）[WSL](https://www.freecodecamp.org/news/how-to-install-wsl2-windows-subsystem-for-linux-2-on-windows-10/)， 
      - 按照文档安装完之后：
        “
          WslRegisterDistribution failed with error: 0x80370102
          Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS.
          For information please visit https://aka.ms/enablevirtualization
        ”
        --> 解决问题的link： https://learn.microsoft.com/en-us/windows/wsl/troubleshooting
          1. BIOS 设置
             1. [确认是否开启](https://cloud.tencent.com/developer/article/1352525)
             2. 开启：
                1. 进入BIOS：我的主板是 技嘉 b550m aorus elite （华硕），通过按 Delete 进入（常见的键包括 F2、Del、F12、Esc、F1 或 F10，）
                2. 您通常可以在 "Advanced"（高级）或 "Advanced CPU Configuration"（高级 CPU 配置）等部分中找到虚拟化相关设置。 我的是“ SVM Mode” 
          2. CPU 版本是否足够新
             1. 如何在命令提示符下查找CPU体系结构类型
                1.打开一个新的命令提示符窗口。
                2.键入echo %PROCESSOR_ARCHITECTURE%，并按Enter键。
             2.  [windows 查看CPU是否支持SLAT的一种方法](https://answers.microsoft.com/zh-hans/windows/forum/all/%E6%9F%A5%E7%9C%8Bcpu%E6%98%AF%E5%90%A6%E6%94%AF/db3fbde8-7607-40d8-a510-9e9909ba4b3e):经确认，windows PC 支持
           3.  开启后：

               1.  * Documentation:  https://help.ubuntu.com
               2.  * Management:     https://landscape.canonical.com 
               3.  * Support:        https://ubuntu.com/advantage
               4.  To run a command as administrator (user "root"), use "sudo <command>". See "man sudo_root" for details.
    - 2. （线上）[在线代码编辑器-Replit](https://replit.com/) 或者 [基于网络的 Linux 终端-JSLinux](https://jslinux.org/)(使用基于浏览器的解决方案访问Linux)