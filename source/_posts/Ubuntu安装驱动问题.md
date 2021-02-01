---
title: Ubuntu16.04 触摸板无响应
date: 2020-11-28 22:58:35
tags:
---
# 神州笔记本电脑安装ubuntu16.04系统 触摸板不响应解决办法

sudo gedit /etc/default/grub
把GRUB_CMDLINE_LINUX=" " 改为GRUB_CMDLINE_LINUX="i8042.reset i8042.nomux i8042.nopnp i8042.noloop"
sudo update-grub
sudo reboot
