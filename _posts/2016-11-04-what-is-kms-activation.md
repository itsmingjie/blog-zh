---
layout: post
title: 所以你们这样用盗版，KMS到底是个什么鬼？
date: 2016-11-04
categories:
- original
- technology
tags: [original,technology,user]
status: publish
type: post
published: true
author:
  login: mj66
  email: jiang@mingjie.info
  display_name: Mingjie
  first_name: 'Mingjie'
  last_name: 'Jiang'
---
不少人啊，真的是不知好歹。明知盗版违法，还是知法犯法。那么既然你们问了，我，作为软件系的和平使者，为了避免大家“看不懂的都是XXX”的心态，就来解释一下，什么是你们口中的“KMS激活”。

首先，回答下大多数人的问题：密钥，读音（mì yào），指解密需要的特殊代码。

KMS，全称Key Management Service。很多人可能不知道，KMS其实是微软官方认可的一种系统激活方式。这个激活方式主要用于企业计算机的批量激活。打个比方，你们公司买了3000台一模一样的台式机，然而都是空机没有内置OEM系统。这样怎么办呢？于是，你们就需要一个系统管理员（System Administrator），由这个系统管理员大神用你们公司的票子购买一个批量激活密钥（也就是大家经常看到的Volume Key，Vol密钥，一定特别贵）。然而有这个密钥还是不够啊，总不见得3000台机器一台一台开机设置输入密钥激活吧？这时KMS的优势就体现了。管理员需要设置一个激活服务器（Activation Server），并在每一个客户机上安装KMS的客户端，就可以进行批量激活和管理。也就是说，管理员不光可以远程激活你的电脑，还能够远程取消激活乃至控制你的电脑。

我们用图来解释下：
 
![](http://mmbiz.qpic.cn/mmbiz_png/CxuqMvxicw8jAfia8lMVXahVn40L6EMDaPsLVlINicm4Uia0GDODgUq0dFaeXmrCaguNvxBKribm1r3Aonj4QdQyABw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1)

![](http://mmbiz.qpic.cn/mmbiz_png/CxuqMvxicw8jAfia8lMVXahVn40L6EMDaPG4kRFewV1mv2XKD4iav6zskypkpZ8PsDzhQw7icFMuK2ZWLia484KZPug/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1)


恩大概就是这样。
那么你们手上那些自称能免费激活Windows的软件（比如KMS Pico，小马等等），是怎么操作的呢？我进行了一些搜索，发现这些软件使用的算法无非三种：

1. 在本地计算机中建立一个虚拟的任务，无限试用系统（低级，容易被封杀）
2. 使用该软件开发者的激活服务器来激活（高级，不容易被封杀）
3. 在本地计算机中建立一个虚拟激活服务器（服务），并发送已激活的模拟信号（中级）

然而，每一种算法都有弊端。第一种无限试用，微软只要轻轻松松给你个补丁你就完事了，毫无难度；第二种，微软要是发现了你激活服务器的违规使用也会直接封杀密钥，从该服务器激活的所有计算机都会出现未激活的状态；最后一种，微软已经采取了措施，不仅让Windows Defender报毒，还在系统更新时直接删除该任务。	

有人说，这些都是临时问题，要是激活掉了重新破解就好。来我们看看更严重的问题：当你的电脑被远程激活时，通常会这样显示：

![](http://mmbiz.qpic.cn/mmbiz_png/CxuqMvxicw8jAfia8lMVXahVn40L6EMDaPt4ZP4uHHznRH7icVzeVWL4P51cVb8uehPOqDiagGNUzP0kiamKn3oVPDw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1)

什么意思？也就是说你的系统不再是你的了——变成属于一个团队或管理员的了。不要不以为然——管理员能够执行的操作那可就多了，拷贝个数据收集个信息简直是小菜一碟，更厉害的还能直接reset你的系统而保留KMS的权限。说不定，哪天KMS Pico的开发者不开心，就按下了那个红色的按钮……

所以，不是优越感，不是无脑黑。用正版，用得放心，心里也踏实。

保护正版，人人有责。