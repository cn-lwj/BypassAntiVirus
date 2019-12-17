# BypassAntiVirus

**本文为Tide安全团队成员`重剑无锋`原创文章，转载请声明出处！**

一直是从事web安全多一些，对waf绕过还稍微有些研究，但是对远控免杀的认知还大约停留在ASPack、UPX加壳免杀的年代。近两年随着hw和红蓝对抗的增多，接触到的提权、内网渗透、域渗透也越来越多。攻击能力有没有提升不知道，但防护水平明显感觉提升了一大截，先不说防护人员的技术水平如果，最起码各种云WAF、防火墙、隔离设备部署的多了，服务器上也经常能见到安装了杀软、软waf、agent等等，特别是某数字杀软在国内服务器上尤为普及。这个时候，不会点免杀技术就非常吃亏了。

但是因为对逆向和二进制都不大熟，编译运行别人的代码都比较费劲，这时候就只能靠现成的工具来曲线救国了。为了，从互联网上搜集了二三十种免杀的方法，对msf或CS进行免杀测试，大部分都是互联网已有的方法，感谢大佬们的无私分享，我只是进行了重新汇总整理。

实验主要是使用了metasploit或cobaltstrike生成的代码或程序进行免杀处理，在实验机器上安装了360全家桶和火绒进行本地测试，在`https://www.virustotal.com/`上进行在线查杀。


# 文章导航

1、远控免杀专题文章(1)-基础篇：[https://mp.weixin.qq.com/s/3LZ_cj2gDC1bQATxqBfweg](https://mp.weixin.qq.com/s/3LZ_cj2gDC1bQATxqBfweg)

2、远控免杀专题文章(2)-msfvenom隐藏的参数：[https://mp.weixin.qq.com/s/1r0iakLpnLrjCrOp2gT10w](https://mp.weixin.qq.com/s/1r0iakLpnLrjCrOp2gT10w)

# 目标可期

<div align=center><img src=images/0.png width=40% ></div>


