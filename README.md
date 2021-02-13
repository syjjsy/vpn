# vpn
## vps简要原理
虽然这是无脑教程，但是我们还是简单了解一下一些基本概念比较好，比如vps是什么。
VPS（Virtual Private Server 虚拟专用服务器）技术，
将一台服务器分割成多个虚拟专享服务器的优质服务。
实现VPS的技术分为容器 技术，和虚拟化技术 。
在容器或虚拟机中，每个VPS都可分配独立公网IP地址、独立操作系统、
实现不同VPS间磁盘空间、内存、CPU资源、进程和系统配置的隔离，
为用户和应用程序模拟出“独占”使用计算资源的体验。
VPS可以像独立服务器一样，重装操作系统，安装程序，单独重启服务器。VPS为使用者提供了管理配置的自由，可用于企业虚拟化，也可以用于IDC资源租用。

简单说，可以vps就是你自己的一台服务器，你可以随时远程登陆(手机都可以，很方便)，在上面部署任何服务，比如建个网站博客之类的，做个邮件服务器，或者就是当个ftp服务器，做个云盘等等，这就不细说了，但是同样你也可以用它搭建梯子，让它成为你自己独享的一台代理服务器。当这个服务器ip在国外的时候，不受墙的限制，你利用这个服务器的梯子科学上网的时候，相当于是用它代理，比如你要看油管的视频，其实是它代替你上油管，视频先加载在你的代理服务器上，服务器在转给你，因为墙也不是所有国外ip都封锁，基本上你新申请的vps是不会被墙的，所以你和你自己的vps之间的链接是正常的（当然之后用的时间越久流量越大，被封的概率也很高，不过不要担心，这时候我们换个ip就好啦）。这样，就实现了科学上网的功能。
好了讲完原理，看看怎么操作，第一步租个vps，vps当然不是免费的，你也可以把它理解为一台在国外，你可以用它远程上网的，永远不关机的电脑。（所以你要是想不花钱的话，可以直接找你在国外上学的同学，用他的电脑搭梯子，也是可行的)


## 1、	服务器选择
需要购买一个外网的服务器。需要注意的是由于ip池内很多都被污了，所以可能部分服务器需要更换ip才能使用。
我选择的是vultr，这个服务器在网上的帖子比较多，遇到问题也比较容易解决。最低需要充值10美金，可以使用支付宝。注册网址https://www.vultr.com/ 
![image](https://github.com/syjjsy/vpn/blob/main/image/1.png)
也可以用比特币，，，，，，
![image](https://github.com/syjjsy/vpn/blob/main/image/2.png)
充值完选服务器
![image](https://github.com/syjjsy/vpn/blob/main/image/3.png)
![image](https://github.com/syjjsy/vpn/blob/main/image/4.png)
日本的便宜而且网速快，但是我们用的脚本需要服务器系统为centos7，这点需要注意
![image](https://github.com/syjjsy/vpn/blob/main/image/5.png)
一般来说5刀的就够用了，其他都默认就行。
![image](https://github.com/syjjsy/vpn/blob/main/image/6.png)
查看详细信息
![image](https://github.com/syjjsy/vpn/blob/main/image/7.png)
出现这个界面就是成功了
![image](https://github.com/syjjsy/vpn/blob/main/image/8.png)
## 2、	ssh客户端安装
ssh客户端就是我们本地连接服务器的工具，windows下ssh客户端主要有Putty和xshell，我一般用putty，直接百度下载就好，用法都差不多，下载好Putty
以后，打开出现下面的画面

![image](https://github.com/syjjsy/vpn/blob/main/image/9.png)
hostname填刚才邮件的ip，点open，会出现login的登陆画面，填root，之后会要求出入密码，直接复制粘贴邮件里的密码就好，putty里粘贴直接在光标后面点鼠标右键就好，第一次登陆会要求改密码，按照提示改就好。
之后就要安装ssrmu脚本了
## 通过ssrmu.sh脚本安装ShadowsocksR
先明确一点，我们是要安装shadowsocksr这个软件，ssrmu是一个便捷的安装配置ShadowsocksR的脚本。总之，通过上一步登录到我们的vps后我们直接复制黏贴下面的命令
wget –no-check-certificate https://github.com/syjjsy/vpn/shadowsocksR.sh; bash shadowsocksR.sh

![image](https://github.com/syjjsy/vpn/blob/main/image/10.png)
等待几分钟
![image](https://github.com/syjjsy/vpn/blob/main/image/11.png)
请务必将此界面截图保存
## 安装ssr客户端
![image](https://github.com/syjjsy/vpn/blob/main/image/12.png)
将刚刚保存的截图里参数一一对应的填好，点确定，然后你的梯子就搭建成功了，ssh客户端和ssr客户端均上传至github了，请自行下载安装。
![image](https://github.com/syjjsy/vpn/blob/main/image/13.png)

如有其他疑问可邮件至syj@njust.edu.cn
