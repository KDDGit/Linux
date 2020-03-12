# Linux
linux相关知识

Q：   
    以下三句命令分别是什么意思？   
    sudo add-apt-repository ppa:maco.m/ruby    
    sudo apt-get update    
    sudo apt-get install rubygems    


A:   
  1)add-apt-repository将PPA添加到您的源列表中,以便Ubuntu知道从该PPA以及官方Ubuntu源中查找更新.通常,
  这用于允许开发人员比官方Ubuntu存储库中的更快地提供更新.

  2)apt-get update告诉apt-get更新其数据库,可以安装哪些软件包以及从哪里安装它们.在这种情况下,apt-get将
  看到你新添加的PPA并发现ppa：maco.m / ruby拥有它所知道的最新版本的rubygems,所以它会记下下次有人从PPA安装rubygems要求安装它.

  3)apt-get install导致apt-get在其数据库中找到包并下载并安装指定的文件.在这种情况下,它会找到rubygems包,从ppa：maco.m/ruby 下载并安装它.
  如果你只是运行apt-get install rubygems,你会得到一个不太新的版本(或者根本没有任何东西,这取决于rubygems是在Ubuntu存储库中还是仅在PPA中).
  
  
 常用软件
     1、WPS
        在“Ubuntu软件”中搜索WPS安装即可
     2、搜狗输入法
        在浏览器中搜索“搜狗输入法”下载Linux版本，安装即可
        注：在命令行输入fcitx-configtool 打开fcitx界面进行设置
     3、引导修复
        Q：
          Windows一更新，Ubuntu就进不去了
        A：
        安装boot-repair    
            sudo add-apt-repository ppa:yannubuntu/boot-repair
            sudo apt-get update
            sudo apt-get install boot-repair
        先备份下grub引导菜单
            cd /boot/grub
            sudo cp grub.cfg grub.cfg.bak
        然后打开“引导修复”或输入 sudo boot-repair &，待它自动扫描后点击“推荐修复”就可以了。然后重启电脑，此时应该能正确进入Ubuntu，
        但grub菜单多了一大堆东西。如果你原来备份的菜单没有问题，直接恢复
            sudo cp grub.cfg.bak grub.cfg
        否则就只能手动删掉这个grub.cfg中的无用内容了。
      4、VLC
        在“Ubuntu软件”中搜索 VLC (视频播放器)安装即可
      5、GIMP
         GIMP免费的，可以实现 PS 的大部分功能
      6、Dash to Dock
         在“Ubuntu软件”中搜索 Dash to Dock 安装即可，修改启动栏、修改主题用
        
        
        
        
