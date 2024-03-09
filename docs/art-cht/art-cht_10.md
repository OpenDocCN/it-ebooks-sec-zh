# 第六章 你能帮我吗？

大家在前面已经看到社会工程师如何通过提供帮助来使人上当，他们的另一个惯用伎俩是假装需要别人的帮助，因为我们都会对处于困境的人施与同情，社会工程师便经常的利用这一方法来达到他的目的。

## 6.1 外地人

第三章中有个故事显示了攻击者如何通过对话令对方说出他的员工号码，下面的故事则运用不同的方法得到了相同的结果，并且这个故事还将展示攻击者如何利用这个号码。

硅谷有一家不太知名的全球企业，散落在世界各地的所有销售处和现场基站都是通过 WAN――广域网，连接到公司总部。入侵者，一个叫布瑞恩?亚特拜（Brian Atterby）的狡猾的活跃分子，他知道入侵一个远程站点的网络总是要比总部的网络容易的多，由于前者的保护措施较为薄弱。

### 6.1.1 我找琼斯

他打电话到这家公司的芝加哥办公室，找琼斯（Jones）先生讲话，接线员问他是否知道琼斯先生的名字。

“我有他的名字，我正在找，你们那儿有几个叫琼斯的？”

“三个，你找的琼斯在哪个部门？”

“如果把他们的名字念一下，可能我就会想起来了。”

“拜瑞（Barry）、约瑟夫（Joseph）和格丹（Gordon）。”

“是乔（Joe，约瑟夫的昵称），肯定是他，他在，哪个部门？”

“商务拓展部。”

“很好，请帮我转过去好么？”

接线员将电话接通，琼斯接起电话，攻击者说：“琼斯先生？嗨，我是托尼，薪金发放专员（译者注：相当于管理工资发放的会计），我们刚刚依据你的要求，把薪金支票存入到你的信联账户上。”

“什么？？？你在开玩笑吧！我从来没这样要求过，我甚至在信联都没有账户！”

“哦，见鬼，我已经转过去了。”

一想到到薪金支票可能转到了别人的账户上，琼斯十分的心烦意乱，并开始怀疑电话另一端的小子是不是有些智力低下。他不知道该说些什么，这时攻击者说：“我得看看是怎么回事，薪金发放时要输入员工号码，你的号码是多少？”琼斯告诉了他。

“哦，不，你说得没错，发出请求的人不是你。”攻击者说。他们越来越蠢了，琼斯想。

“这样，我看一下谁负责此事，然后把错误马上改过来。请别担心，下次不会这样了。”

对方向他保证。

### 6.1.2 一次商务旅行

不久之后，这家公司在得克萨斯首府奥斯丁销售处的系统管理员接到了一个电话。

“我是约瑟夫?琼斯，商务拓展部的。这星期我要入住德斯基（Driskill Hotel）饭店，我想让你帮我建立一个临时帐号，以免除远程拨号才能访问我的电子邮箱。”

“让我再确认一下你的名字，告诉我你的员工号码，”系统管理员说。假琼斯告诉了他，并说：“有没有速度很快的上网拨号？”

“请等一下，老兄。我得在数据库中确认一下。”不一会儿，系统管理员说：“好的，乔，你的楼牌号是多少？”攻击者对此早有准备，报上了备好的答案。

“好的，”系统管理员对他说：“验证通过。”

如此简单，系统管理员确认了约瑟夫?琼斯的名字，部门，还有员工号码，针对他的测试问题，“乔”也给出了正确的答案。

“你将使用的用户名与你在公司的一个用户名相同，jbjones，”系统管理告诉他说，“并且我将你的口令初设为 changeme”。

米特尼克信箱

不要指望网络安全装置和防火墙来保护你的信息，要注意最薄弱的环节。通常，那就是你的员工。

### 6.1.3 过程分析

拨几个电话用上 15 分钟的时间，攻击者就可以访问这家企业的广域网了。有很多这样的企业，都属于我要提及的“软心糖安全”，这个概念最早是由贝尔实验室的两位研究人员提出的，斯蒂夫?贝劳文（Steve Bellovin）和斯蒂文?切斯威克（Steven Cheswick）。他们用这样的词语来描述这种安全防护：“坚硬生脆的外壳，核心却很柔软”，如同 M＆M 巧克力糖（一种驰名的糖果品牌），两位研究人员说，外壳即防火墙并不足以保证安全，因为一旦入侵者绕开它，内部的计算机系统便不堪一击。大部分情况下，这种保护措施是不够的。

上面的故事符合这个定义，利用得到的拨号和账户，攻击者甚至不用费力去攻击防火墙。而且，一旦他进入内部，内网的大部分系统就十分危险了。由于我我的经历，我知道这种骗局曾在世界最大的软件生产商身上起过作用。依据我的经验，在一个聪明的具有说服力的社会工程师面前，没有人是绝对安全的。

专业术语

软心糖安全：贝尔实验室的贝劳文和切斯威克提出的说法，用以描述一种安全状况。外部防御十分强壮，如防火墙，但其后面的设施却十分脆弱。这个说法来自于 M＆M 巧克力，这种糖果有着坚硬的外壳和柔软的糖心。

地下酒吧式的安全：知道自己想要的信息在哪里，并且使用一个词或是名称来获得对此信息或计算机系统的访问权的一种安全形式。

## 6.2 地下酒吧式的安全

对于早期的地下酒吧——那些在禁酒令时期提供自酿酒的夜总会，一个顾客需要走到门前敲门，然后门上会打开一个小口，伸出一张冷冰冰的脸。如果来人熟悉情况，他就会说出此地的老主顾（一句“乔让我来的”就可以了），看门的护卫就会打开门让他进来。

这个事情的关健在于知道地下酒吧的位置，门上没有标志，而酒吧老板也不会挂一盏霓虹灯在门口来表示这儿有个酒吧。通常，只要能找到地方就基本可以进入。很不幸，同样的安全措施在企业中广泛存在，这种没有任何保护的安全级别我称之为地下酒吧式的安全。

### 6.2.1 我在影片中见到过它

这儿有一个例子，来自一部许多人都会想起来的电影。《英雄不流泪》（Three Days of the Condor）中的主角，特纳（罗伯特?瑞德福特饰演）为一家与中央情报局签约的小调查公司工作。一天，他吃完午饭后回来发现他的同事们都被枪杀了，他决定找出凶手和真相，同时那些坏人也一直在找他。故事的后面部分，特纳（Turner）设法得到了其中一个坏人的电话号码，但这个人是谁？特纳又如何确定他的在哪儿呢？他很幸运。编剧大卫?瑞菲尔轻松的给了特纳一个美国陆军通讯兵的受训背景，使他在电话方面有着丰富的知识和经验。特纳当然知道该如何利用手中的电话号码，在剧本中，那幕场景是这样的：

特纳重新拿起电话拨出另一个号码

叮呤！

女性的声音从电话中传来：CNA，我是科尔曼（Coleman）夫人。

特纳：科尔曼夫人，我是哈罗德?托马斯，客户服务 CNA202-555-7389，谢谢。

科尔曼夫人：请稍等。（几乎是同时）兰纳德?亚特伍德，马里兰州切维柴斯区麦克肯色街 765 号。

虽然编剧错误地把华盛顿特区的电话区号用到了马里兰州，但我们没必要注意这个细节。关健是弄明白刚才的对话是怎么一回事。

特纳由于有通讯兵的受训背景，他知道如何给电话公司的 CNA 部门（Customer Name and Address－客户名称与地址）打电话。CNA 是为了方便电话安装员和其他得到授权的电话公司职员而成立的部门，电话安装员拨打 CNA 并提供一个电话号码时，CNA 的服务人员就会报出电话所有者的名字和地址。

### 6.2.2 愚弄电话公司

在现实世界中，CNA 的电话号码保护的十分严密。尽管当今的电话公司最终明白这一点，并不再轻易的泄露此类信息，但在当时他们却实行着地下酒吧式的安全，那时的安全专家们管这种安全叫做隐晦安全。他们假定任何给 CAN 打电话并知道其专业用语（如，客户服务 CNA555-1234）的人都已被授权得到相应信息。

专业术语

隐晦安全：一种效率低下的计算机安全手段，通过对系统运转细节（协议、算法和内部系统）的保密来达到防范目的。隐晦安全假定可信任成员组以外的人不能接近系统，因此这种安全并不可靠。

米特尼克信箱

隐晦安全在社会工程师的面前毫无用处。在这个世界上，每一个计算机系统至少有一个人在使用。因此，如果社会工程师能够操纵这个使用系统的人，系统的隐晦就没有意义。不用亲自验证或确认，不用提供员工号码，也不用每天改变口令，只要你知道正确的电话号码并听起来可以信任，你就有权得到相关信息。对于电话公司来说，情况并不总是这样，他们还会定期的（至少一年一次）改变电话号码做为仅有的安全举措。即便这样，某个特定时期的号码还是在电话盗打者的圈子里传得很广，他们很高兴利用这个便利的信息资源，并乐于在同行中分享他们的所做所为。在我十几岁习惯盗打电话的时期，拨打 CNA 我最先学到的手段之一。

在全世界的政府和企业中，地下酒吧式的安全仍然很普遍。它可能是你公司的部门、员工和专业术语，有时连这些也用不着，一个内部电话号码就够了。

## 6.3 粗心的计算机管理者

尽管企业中的许多员工都对信息安全的危险或给予忽视或漠不关心，或是没有这方面的意识，但那些 500 强企业中计算机中心的管理者应该对安全操作了如指掌了吧，对吧？

不要期望一位计算机中心的管理者——负责公司 IT 部门的人，会掉入简单、明显的社会工程学圈套，尤其是还带有孩子气的、刚步入社会的年轻社会工程师。但有时，这样的想法是错误的。

### 6.3.1 收听

在以前，对许多人来说，把无线电调到地方警察局或消防队的频率收听正在进行中的银行抢劫、办公大楼起火、高速追击是一件很有趣的事情。执法部门和消防部门使用的无线电频率，曾经从街角书店的书中就可以查到。现在，在网上就有这些频率的列表，你还可以从 Radio Shack（译者注：美国著名电子产品零售商）买到列有地方、郡、州有时甚至是联邦机构无线频率的书。

当然，不只是那些怀有好奇心的人，午夜抢劫店铺的窃贼会收听是否有警车派到附近，毒品贩子要始终关注的毒品缉查人员的行动，纵火犯则通过放火后收听消防队奋力灭火的情况来满足他的变态嗜好。

最近几年来，计算机技术的发展已经使声音信息的加密成为可能。在工程师们不断的找到方法把越来越多的计算能力塞进一块微芯片时，他们也开始制造小巧的加密无线设备，帮助执法部门来防范坏人和怀有好奇心的人窃听。

### 6.3.2 窃听者丹尼

一个我们称之为丹尼的扫描器爱好者，同时也是位技巧娴熟的黑客，他想看一下自己是否能够染指由安全无线系统顶级生产商开发的绝密的加密软件源代码。他希望通过这些代码了解如何对执法部门进行窃听，同时利用此技术令即便是最强有力的政府部门也很难监视他与朋友的通话。在朦胧的黑客世界中，丹尼这样的人属于特殊的一类，介于无恶意的好奇和完全的破坏之间。他们有着专家般的知识和极易引起麻烦的黑客想法，为了智力挑战和了解技术细节带来的满足感入侵系统和网络。但是他们惊人的电子入侵技术，也仅仅是一种特技。

这些人，这些无恶意的黑客，非法进入别人的网站纯粹是为了有趣并为能够证明自己的能力而感到满足。他们并不偷窃，也没有利用这种手段来赚钱。他们不会破坏文件、中断网络连接，或是摧毁计算机系统。他们的目的就是悄悄地捕获文件拷贝、搜索电子邮件、得到密码，以嘲弄那些网络管理员和对安全负责的工作人员，他们的满足感基本来自于这种胜人一筹的能力。

就这样，我们的丹尼为了满足自己强烈的好奇心并为了对生产商可能做出的惊人革新一看究竟，他将检验对方高度保护的产品信息细节。不用说，这种产品的设计是受到严密保护的，如同公司其他贵重的财产一样。丹尼知道这一点，但他并不怎么担心。毕竟，这只是一家没什么名气的大公司。但他如何得到软件的源代码呢？

正如我们最后将要看到的，从公司的保安通讯小组中猎取信息很容易，即使这家公司也使用了双因素认证（用户需两种单独的标识来证明身份）技术。这里有一个你可能已经熟悉的例子：当你的信用卡更换日期到了的时候，你需要给发行公司打电话，让他们知道信息卡还在持卡人的手中，并没有被人偷走。信息用卡上会说明在通常情况下要从家打电话，当打电话时，信用卡公司的软件程序就会分析 ANI（自动号码认证），并被转到公司的免费电话上。信用卡公司的计算机使用 ANI 提供的呼叫方号码，与公司持卡人数据库中的号码做比较。公司的工作人员在接电话时，他或她就会看到数据库中显示的客户详细信息。这样，工作人员就知道了电话是客户从家中打来的，这就是一种形式的认证。

专业用语

双因素认证：用两种不同的验证方式对身份进行确认。比如，一个人必须从某个可确认的地方打来电话并知道口令来确认自已的身份，然后工作人员从你的信息中选出某个条目（通常为社会保险号码、出生日期或是母亲的姓氏）来询问你，如果你的答案正确，这就是第二次的验证――基于你应该知道的信息。我们故事中那家生产安全无线电系统的公司，每一名有权访问计算机的职员都有自己的账号和口令，并另外配备一个叫做安全 ID 的电子小设备，这就是时间令牌。它有两种型号：一种只有一张信用卡的一半大小，但稍厚些。另一种小到可以挂到钥匙链上。

这个特殊的装置由加密技术衍生而来，它的上面有一个显示六位数字的小窗口，每六十秒改变一次。当一位得到授权的用户从外部访问网络时，她首先必须输入她的 PIN 码和令牌上的数字，依此来确认自己的身份。内部系统一旦予以确认，她就可以输入用户名和口令进行认证。

对于觊觎着源代码的年轻黑客丹尼来说，他不仅要解决用户名和口令的问题（对于经验丰富的社会工程师来说这算不上什么难题）还要绕过时间令牌的检测。攻破基于时间令牌和用户 PIN 码的双因素认证听起来像是一个“不可能的任务”，但对于社会工程师来说，这种挑战类似于一个能够占尽对方优势的有着高超观察能力的牌手，再加上一点儿小运气，当他在桌子旁坐下来时，就知道别人口袋里的钱基本已是他的囊中之物了。

### 6.3.3 冲击堡垒

丹尼先是做准备工作，很快他就得到假扮一个真正的雇员所需的各种信息。姓名、部门、电话号码和员工号码，还有部门经理的姓名和电话号码。现在，是攻击前的平静期。按照计划，丹尼在采取下一步行动前还需要一个条件，而此事他毫无把握：丹尼需要大自然母亲的帮助，他需要一场暴风雪，一个阻止人们去办公室上班的恶劣天气。在南达科他州的冬季，那家生产商的所在地，一个恶劣气候从不会让希望它的人等太久。星期五晚，一场暴风雪到了。雪迅速的转成冰雨，到了早晨路面就会结一层薄薄的冰，十分危险。这对丹尼来说，简直太好了。

他打电话给那家厂商，转到计算机机房，找到一名自称罗杰?科瓦斯基（Roger Kowalski）的计算机操作员。

丹尼：“我是安全通讯部的鲍伯?比林斯（Billings），我现在家中，因为冰雪的缘故我无法开车。我现在需要访问我的工作站和服务器，但我把安全 ID 忘到办公桌上了，你能帮我拿回来么？或者让别人帮一下忙，然后当我登录的时候给我念一下好么？我的工作任务有一个最后期限，我没有别的办法。而且，我也没办法去办公室，路况太糟糕了。

操作员科瓦斯基：“我不能离开计算机中心……”，

丹尼：“你自己有安全 ID 么？”

科瓦斯基：“计算机中心有一个，我们保留它是为了操作员应对紧急情况的。”

丹尼：“听着，你能帮我这个忙么？我拨号入网的时候，借用一下你的安全 ID 可以么？路况一能驾车就不用了。”

科瓦斯基：“你是谁来着？你的上司是谁？”

丹尼：“埃德?特伦顿（Ed Trenton）。”

科瓦斯基：“哦，我认识他。”

当事情比较棘手时，优秀的社会工程师会多做一些调查工作。“我就在二层，”丹尼说：“罗伊?塔克（Roy Tucker）的旁边。”科瓦斯基也知道这个人。丹尼接着重新建议他：“到我的办公桌取来安全 ID 很方便。”

丹尼完全断定对方不会听从他的建议。首先，对方不会在当班的时候离开岗位，穿走廊、爬楼梯到大楼的另一边。也不会到别人的办公桌上乱翻一通，打搅别人的私人空间。没错，这个赌注很安全。

科瓦斯基不想对一个需要帮助的人说“不”，当然他也不想擅自做主张而让自己陷入到麻烦中，于是他做了个折中的决定。“我得请示一下，稍等。”他放下电话，丹尼能听到他拿起另一个电话拨打并解释这件事。科瓦斯基这时做出了让人难以理解的陈述（他实际上已经认定了丹尼就是鲍伯?比林斯）。“我认识他，”他对他的主管说：“他的上司是埃德?特伦顿。我们能让他用一下计算机中心的安全 ID 吗？”

丹尼惊奇地偷听着科瓦斯基对他意乎寻常、意料之外的支持，他简直无法相信自己的耳朵。

又过了一会儿，科瓦斯基拿起丹尼的电话说：“我们经理想亲自跟你说话。”然后告诉丹尼经理的名字和手机号码。丹尼打过去又把整个故事重复了一遍，同时又添加了一些工作细节和他的工作为什么有一个最后期限。“如果有人拿回来我的安全 ID 就方便多了，”丹尼说：“我想桌子应该没锁住，它就在左上方的抽屉里。”

“嗯，正好是周末，”经理说：“我想你可以用计算机中心的 ID，我让值班人员在你拨入的时候给你读一下随机访问码。”然后他把相应的 PIN 码告诉了丹尼。整个周末，丹尼只需打电话给计算机中心让有关人员念一下安全 ID 上的六位数字，便随时都可以进入这家企业的计算机系统。

### 6.3.4 内部任务

当丹尼进入这家企业的计算机系统后，又该怎么办？他如何找到那台放有他想要的加密软件的服务器呢？对此，他已有所准备。许多计算机用户都知道电子公告板形式的新闻组，人们可以把问题贴上来或者回答别人的问题，也有人用它来寻找拥有共同兴趣的虚拟伙伴，如音乐、计算机，或者是其他成百上千的主题。在新闻组站点上发布信息的时候，很少有人会想到这些信息会在网上保留数年之久。比如 Google，目前保留着 7 亿条信息量的存档，某些信息已经有了二十年的历史。丹尼首先访问了[`groups.google.com`](http://groups.google.com/)这个网址，用“无线加密通讯”和那家企业的名称做为关健词进行搜索，结果发现了一条数年前某个职员贴出的信息，是在这家公司刚开始开发这个产品的时候贴出的，很可能是在警察部门和联邦机构考虑使用加密无线信号很久以前的事了。

这条信息包含了发送者的签名档，其中不仅有他的名字――斯科特?普瑞斯（Scott Press），还有他的电话号码，甚至他的工作组名称――安全通讯小组。丹尼发现这个电话后打了过去，这个机会似乎很渺茫。多年后他仍然还在这家公司么？在这个暴风雪的周末他还会在工作么？电话铃在响，一声、二声、三声，一个声音从电话另一端传来，“我是斯科特，”对方说。

丹尼介绍自己是公司 IT 部门的，从而操纵着普瑞斯（用前几章中大家已熟悉的方法）透露出研发部门所使用服务器的名称，这些服务器的上面可能存有这家企业无线安全产品固件和独有加密算法的源代码。

丹尼越来越接近目标，也越来越兴奋。他期待着那种快感，那种当他完成只有很少人才能达到的目标时所感到的狂喜。然而，他现在还不能放松。虽然由于计算机中心经理的支持，可以随时进入这家企业网络系统，同时也知道了需要访问的服务器。但是，在他拨入时他登录的终端服务器却不能连接到安全通讯小组的系统。一定是有内部防火墙或是路由器保护着研发组的计算机系统，丹尼必须找到其他的办法进入。

接下来的情况需要些胆量，丹尼再次给计算机中心的科瓦斯基打电话抱怨：“我的服务器不让连接，我需要你帮我建一个账号来 telnet（远程登录）系统。”

既然部门经理已经同意告诉他时间令牌上的访问码，当然这个新的请求似乎也没什么不合理。科瓦斯基在计算机中心的计算机上建立了一个临时账号，然后告诉丹尼不再需要这个账号时通知他，好把它删除。有了这个临时账号，丹尼便可以连接到安全通讯小组的系统了。经过了一个小时的查找，丹尼中了个头彩，他找到了访问研发服务器的漏洞。很明显，系统管理员并没有时刻关注最新的系统远程安全漏洞，但丹尼关注了。

很快地，他就找到那些源代码文件，并把它们远远地发送到一个提供免费存储空间的商业站点。这样，即使这些文件被发现，也不会追查到丹尼。现在只剩下最后一步了：有条不紊的擦去他的痕迹。他在当晚的杰伊?里诺（译者注：Jay Leno，著名脱口秀节目主持人）的节目播完之前完成了这项工作。

丹尼极为得意他的这次杰作，在这次行动中，他从未把自己置于危险之中，这是一次令人陶醉的激情之旅，甚至比滑雪和跳伞都要过瘾。丹尼那天晚上喝醉了，不只是因为威士忌、杜松子、啤酒和清酒，在盗来的源代码文件中逐步地接近那绝密的无线软件时，他完全沉醉于自己的能力和成功感之中。

### 6.3.5 过程分析

在上面的故事中，骗局的成功归于那家企业的职员过于相信了打电话人表示身份的话语。这种帮助同事解决问题的热心一方面使工作顺利进展并获得更令人满意的合作认可，另一方面却是极易被社会工程师利用的重大漏洞。

在骗局中丹尼使用的一个小技巧值得注意：他在要求别人到他的办公桌上拿安全 ID 时，不断地说“拿回来”。这个用语经常做为让狗取东西的命令，没人会乐意为别人“拿回来”东西。由于这一点，丹尼更加的断定这个请求不会被接受，于是其他的解决方法便会自然而来，那正是他想要的结果。那个计算机操作员科瓦斯基，在丹尼随便的说出了一个自己碰巧认识的人名后便完全相信了他。但为什么科瓦斯基的经理（一个 IT 经理）竟然也同意让陌生人访问公司的内网？仅仅是因为这样的求助电话是社会工程师百宝囊中一个强大的说服工具么？

米特尼克信箱

这个故事表明时间令牌或是类似的认证方法并不能抵挡住一个诡计多端的社会工程师，真正有效的防范是一个尽职尽责职员，不仅严守公司的安全守则而且了解别有用心的人是如何影响他人的行为的。

## 6.4 预防措施

在上述所有的故事中有一点似乎经常提到，那就是攻击者从企业外部进入内部的计算机网络时，帮助他的工作人员都没有采取足够的措施来确认对方的合法身份，是否有权访问系统。为什么我会经常提及这一点呢？因为，这的确是许多社会工程师在攻击时所采用的手段。对于他们来说，这是达到目标最简单易用的方法。一个电话就能解决的事，还有必要再花上几个小时寻找技术上的漏洞么？

对于社会工程师来说，实施这种攻击最有力的手段就是假装需要帮助，这是攻击者经常采用的方法。既然我们不想禁止员工对同事或客户的帮助，因此特定详细的确认程序成为判断任何人是否有权使用计算机或接触机密信息的必要。这样，我们才可以帮助应该帮助的人，同时保护企业的信息资产和计算机系统。安全程序应清楚、详细的说明不同环境下所使用的各种不同的确认方法，第十七章提供这样的一个详细列表，但在这儿首先要考虑一些指南：一个确认对方的好办法就是拨打公司通讯录上的电话，如果对方实际上是个冒名顶替者，那么这个确认电话不是令你找到真正的人（被冒充者，而这时冒名顶替者还给你打着电话），就是可以听到被冒充者的语音信箱，从而你就可以与冒名顶替者的声音做比较。

如果企业使用员工号码确认身份，务必要把员工号当做企业的敏感信息，小心保护，不要泄露。此规则适用于所有的内部识别信息，如内部电话号码、部门单据，甚至电子邮件。在安全培训中应唤起每个人对陌生人的警惕，不要因为对方听起来熟悉内部或可信就认为他是真正的内部人员，仅仅知道内部的惯例或术语不能做为对方的身份不需要用其他方式确认的理由。

安全管理人员和系统管理员不能只注意其他人员的安全意识，他们自己也需要提醒自己遵循守则、程序和操作规程。密码口令等信息绝不能共享，而对时间令牌或其他方式的认证来说，限制共用则更为重要。应该普遍认识到，这类事物的共享会危害到公司整个的系统布署。共享就意味着无责任，如果发生安全事件，或是其他问题时，就分不清是谁的责任了。

正如我在整本书中不断重申的，员工要熟悉社会工程师的策略和方法，仔细的分析对方的要求，考虑把角色扮演做为安全培训中的一个固定内容，以使员工能较好的理解社会工程师的手段。