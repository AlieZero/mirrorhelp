===================
Termux 源使用帮助
===================

地址
====

https://mirrors.ustc.edu.cn/termux

说明
====

Termux APT 源镜像

收录架构
========

*   ARM, AArch64, i686, x86_64

使用说明
==============

编辑 :file:`/data/data/com.termux/files/usr/etc/apt/sources.list` 为如下内容

::

    deb https://mirrors.ustc.edu.cn/termux/apt/termux-main stable main

或者，你也可以使用 ``sed`` 命令进行文本替换：

::

    sed -i 's@packages.termux.org@mirrors.ustc.edu.cn/termux@' $PREFIX/etc/apt/sources.list
    pkg up

注：Termux 会自动将环境变量 ``$PREFIX`` 设定为 :file:`/data/data/com.termux/files/usr`

.. tip::
    Termux 目前（2021 年 6 月）的官方源为 packages.termux.org，建议使用 ``termux-change-repo`` 命令先换回官方源，再进行文本替换，以减少出错的可能。

相关链接
========

:Termux 官网: https://termux.com/
:FDroid: https://f-droid.org/zh_Hant/packages/com.termux
:Google Play: https://play.google.com/store/apps/details?id=com.termux
