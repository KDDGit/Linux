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
