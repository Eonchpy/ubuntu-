# 关于ubuntu下掉显卡驱动问题
今天开机莫名其妙分辨率变低,也无法调整,运行nvidia-smi查看发现显卡驱动崩了,于是乎只能重装, 在此记录一下蛋疼的重装经历:
很简单...
0. 切入ubuntu控制台模式: Ctrl+alt+F1

1. 删除现有驱动
    sudo apt-get remove --pruge nvidia*

2. 关闭显示系统:
    service lightdm stop
    
3. cd进有对应驱动安装包的目录:

4. 运行***.run程序进行安装, kms选择no, 其他一路yes

5. 开启显示系统
    service lightdm start
