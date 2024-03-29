# 前言

> 作者: KEVIN D.MITNICK & William L.Simon
> 
> 译者：王小瑞 jroclee[AT]163.com
> 
> 来源：龍之冰点 Hhacker[AT]Hhacker.com

一些黑客毁坏别人的文件甚至整个硬盘，他们被称为电脑狂人（crackers）或计算机破坏者（vandals）。另一些新手省去学习技术的麻烦，直接下载黑客工具侵入别人的计算机，这些人被称为脚本小子（script kiddies）。而真正有着丰富经验和编程技巧的黑客，则开发黑客程序发布到网站或论坛（BBS）。还有一些人对黑客技术没有丝毫兴趣，他们把计算机仅仅当做窃取金钱、商品和服务的辅助工具。

尽管媒体神话了凯文·米特尼克，但我并不是一个用心险恶的黑客，我只是喜欢不断地超越自己。

## 人之初

我的人生之路，也许在我很小的时候就注定了。三岁时，由于父亲的离去，使我无忧无虑的生活发生变故。做招待的母亲支撑着家庭。那时的我（一个由深受没有工作规律之苦的母亲养活着的独生子），除了睡觉以外，大部位时间都没人管，我就是我自己的保姆。

在圣费尔南多谷（San Fernanado Valley）的成长经历给予我探索整个洛杉矶的机会，十二岁时，我发现了一个可以免费周游洛杉矶的方法。我发现到坐公车时购买的换乘券，是由一种非常规的打孔机打出来的，公车司机用它来在换乘券上标记日期、时间和路线。一位司机友好地回答了我精心准备的问题，于是我知道了在哪里可以买到这种特殊的打孔机。换乘券用来改乘车次从而到达目的地，但是我想出的方法，可以让我使用换乘券免费到达我想去的任何地方。

获得空白换乘券很容易，如同去公园散步般简单，因为公车终点站的废物箱中总是充斥着公车司机换班时未用完的换乘券本子。用一叠空白换乘券加上打孔机，我可以制作出我自己的换乘券，并用它行遍全洛杉机公车能够到达的任何地方。很快，我就差不多记住了整个公交系统的公车时刻表。（我对某种信息的记忆力总是让人惊讶，这一个较早的例子。直到现在，我还能记住远在童年时的电话号码、口令以及其它一些看上去十分琐碎的事情。）

另一个在小时候就显露出来的个人兴趣是对魔术的迷恋。一旦我知道了某个魔术的变法，我就会不断的练习、练习，再练习，直到我完全掌握。从某种程度上说，正是由于魔术，才让我发现获取秘密信息的乐趣。

## 从盗打电话到黑客

我首次接触社会工程学的时候是在中学时期，那时我遇到了一位喜欢盗打电话的同学。“电话盗打”是一种利用电话公司雇员和电话系统来探测电话网络的黑客行为。他向我展示了使用电话的高级窍门，比如从电话公司获取任何一位客户的资料，以及使用秘密测试号码拔打免费长途电话。实际上这只是对我们来说免费，因为我后来发现这根本就不是一个秘密测试号码，那些话费事实上从某些倒霉公司的 MCI（译者注：美国著名通讯公司）帐户上划出了。

这就是我对社会工程学的入门，也可以说是我的启蒙阶段。我的朋友还有后来认识的另外一个盗打电话的人，他们在给电话公司打电话时让我在旁边听，他们是如何让电话公司相信他们所说的话。于是，我知道了许多电话公司的办公地点，他们的业内用语，还有办公程序。这种“训练”并没有花多长时间，不久我便可以完全自己来做这些事情，甚至比我的启蒙老师们做的还要好。

我生命中下一个 15 年的生活已经注定。

在中学，我最为喜欢的恶作剧就是获得对电话交换机未授权的访问，然后改变某个电话盗打者的话费设置。当他从家里打电话时，他的电话就会告诉他需要投入一角硬币，因为电话公司交换机的记录被我更改，从而认为他拔打的是一个投币电话。

我开始关注有关电话的任何事情，不只是电子学、交换机和计算机，还有公司组织、业务手续和行业术语。不久之后，我就比任何一个电话公司的雇员都更加了解电话系统。我对社会工程学的运用也达到了娴熟的阶段，十七岁时，我就能与大多数电信公司的员工谈论几乎任何事情，无论是当面聊还是打电话。

实际上我较为公开化的黑客之路，始于中学。尽管在这里我无法说清原委，但其实一句话也能表达了。在我黑客生涯的早期，一个驱使我的动力就是被黑客圈子的人所接受。在那时，黑客这个词是指一个花费大量的时间调置软硬件的人，或是开发更有效的程序，或是绕过不必要的步骤来更快的完成工作。这个词如今已经是一个带有贬义的“恶意犯法者”的意思了，但在本书中，我仍然按原来对它更为善意的理解使用这个词汇。

中学之后，我在洛杉矶计算机学习中心攻读计算机。没几个月的时间，学校的计算机管理人员就意识到我发现了操作系统的漏洞，并取得了管理员权限，但是在学校的教学人员中，最好的计算机专家也无法弄清我是如何这样做的。这也许是最早雇佣黑客的例子之一吧，他们给了我一个无法拒绝的提议：要么做出一个荣誉学位的毕业设计来加强学校的计算机安全，要么由于黑客行为而中止学业。当然，我选择了前者，以本科优等成绩荣誉学士毕业。

## 成为社会工程师

每天早晨，许多人从床上一爬起来，便开始对千篇一律的繁重工作犯愁。我却很幸运，因为我喜欢我的工作。你简直无法想像我作为一个秘密调查者而得到的挑战、奖赏和快乐。我的天份在称为社会工程学（使人们做在通常情况下不会为陌生人做的事情）的表演艺术中得到磨练和回报。

对我来说，成为社会工程学的行家里手并不困难。我父亲家一连好几代都从事销售领域，因此家里人都有着说服和影响别人的家族特征。当把这种特征与骗人的爱好结合起来时，这就是一个社会工程师的基本轮廓了。可以说行骗艺术的分类有两种，一种是通过诈骗、欺骗来获得钱财，这就是通常的骗子。另一种则通过蒙敝、影响、劝导来达到获取信息的目的，这就是社会工程师。从我使用诡计免费乘车的时候（我那时还小，并没有认识到这样做有什么不对），就逐渐意识到我具有一种以前没有料想到的挖掘秘密的天份。通过使用诡计、了解术语和培养良好的操纵技巧，更为加强了这种天份。一个用来发展我的专业技艺（如果这可以称为一个专业的话）的方法就是看我是否能与电话另一端的人攀谈，并获得相关信息，即便这些信息对我毫无用处，这样做只是为了证明我的专业技巧。同样，我还用此种方法，练习奇巧的计谋、托辞，不久我发现我可以取得我想关注的任何信息。正如我在数年后的国会听证会上，在利伯曼（Lieberman）和汤姆森（Tompson）参议员面前所做的证词中描述的那样：

“我未经授权进入了世界上最大的几家公司的计算机系统，并成功渗透了一些防范最好的电脑系统。我使用技术和非技术手段来取得各种操作系统和通讯设备的源代码，以研究它们的漏洞和工作机理。所有的这些行为都是为了满足自己的好奇心。看看自己能做什么，并发现其中的秘密，比如操作系统、移动电话以及任何能引起我好奇心的东西。”

## 最后的想法

自从被捕以后，我已经承认了自己这些行为的非法，侵犯了他人的秘密。我的错误行为是由于好奇心引起的，我抑制不住的想知道电话网络是如何运转的，以及了解计算机安全的每个细节。我从一个喜欢魔术戏法的孩子成为一个最具恶名的、被政府和企业害怕的黑客。当我反省过去的这 30 年时，我承认自己做出了极其拙劣的选择，被好奇心驱使，被学习技术的欲望和智力挑战的虚荣所驾驭。

但我现在已经转变，我正在运用我的才能和信息安全、社会工程学的许多有关知识来帮助政府、企业、个人来检测、防范和应对信息安全的威胁。本书可以把我的经验较好地介绍给他人，以避免那些怀有恶意的信息盗贼可能带来的危害。我相信，你将会从本书中得到乐趣、教育和启发。