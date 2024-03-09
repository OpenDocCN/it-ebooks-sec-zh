# 第十三章 聪明的骗局

现在你已经知道了，当接到陌生人请求敏感信息（或其它对攻击者有用的东西）的来电时，接电话的人必须被培训询问呼叫者的电话号码，然后打过去核实这个人的身份是否和他声称的一样——例如，一名公司员工，一名商业伙伴员工，或者一名供应商技术支持代表。

甚至当一家公司明确规定员工必须小心核实呼叫者的身份时，经验丰富的攻击者仍然可以利用许多骗局使受害人相信他们是他们声称的人，即使是安全意识较高的员工也会被下面所述的方法所骗。

## 13.1 骗人的来电显示

任何用手机接过电话的人都曾看到过来电显示——显示屏上呼叫者的电话号码。在商业环境下，员工只要看一眼便能知道打来的电话是公司同事还是外部人员。

很多年前，一些雄心壮志的电话盗打者就已经用上了来电显示功能，那时电话公司甚至还没有向公众开放这一服务，有一段时间他们吓坏了不少人，接电话的时候总是在对方还没来得及说话之前就喊出他们的名字。

当你养成了看来电显示的习惯时，你认为它是安全的并以此判断呼叫者的身份——这正是攻击者想要的。

### 13.1.1 琳达的电话

日期/时间：7 月 23 日，星期二，下午 3:12

地点：星级漫游航空公司财政部办公室

当琳达?希尔（Linda Hill）的电话响起的时候她正在为她的老板书写备忘录，她看了一眼来电显示，发现是一个叫维克托?马丁（Victor Martin）的人从公司在纽约的办公室打来的——她不认识这人。

她本来想把电话转到语音信箱，这样她就不会中断写备忘录的思路，但好奇心还是占了上风，她拿起了电话，然后对方自我介绍说他是产品推广部的员工，正在为 CEO 整理一些材料，“他正在赶往波士顿和我们的一些银行家开会，他需要本季度的财务报表，”他说，“另外，他还需要 Apache 项目的财政预算。”维克多提到了公司春季主打产品代号。

她问他要电子邮件地址，但是他说他现在无法接收电子邮件，技术人员正在想办法解决，能否传真过来？她说也可以，然后他把他的内部传真号给了她。

几分钟后她发出了传真。

但维克多并不在产品推广部工作，事实上，他甚至不是这家公司的员工。

### 13.1.2 杰克的故事

杰克?道金斯很年轻的时候就开始了他的职业生涯——在纽约人体育场、拥挤的地铁月台和夜间聚集着游人的泰唔士广场行窃。他可以从一个人的手腕上取下手表而不被发现，可见他动作之敏捷手法之高超。但在他充满烦恼的少年时期，他却因失手而被抓了。在少管所里，杰克学到了一个新职业，被抓住的可能性非常之低。

他当前的任务是获得一家公司的季度损益表与现金流量信息，要在这些数据被提交到美国证券交易委员会( SEC ) 并公布之前。他的客户是一个不愿意解释为什么需要这些信息的牙医，这个人的小心翼翼在杰克看来十分有趣，他之前的推测是——这家伙可能赌博赢了钱，要么就是有一个一直没被他的妻子发现的有钱的女朋友，或者也有可能是向他的妻子吹嘘了自己在股票市场的英明神武，总之现在他已经失去了所有的管束，只想进行一大笔投资，在这家公司公布他们的季度财务报表之前，预测他们的股票价格将如何变化。

人们惊讶地发现，细心的社会工程师可以迅速地应对从未遇到过的情况。当杰克从牙医那里回到家的时候，他已经想好了一个计划。他的一个朋友查尔斯?贝茨（Charles Bates）在 Panda 进出口公司工作，这家公司有自己的电话交换机或 PBX（译者注：专用分组交换机）。

在了解电话系统的人熟悉的术语中，PBX 连接着数字电话服务 T1，并被设置为初始速率接口 ISDN（综合服务数字网络）或 PRI ISDN，这意味着从 Panda 打出的每一个电话都会通过一个数据频道发送呼叫处理信息到电话公司的交换机：这些信息包括将转到（除非被锁定了）对方来电显示上的主叫号码。

杰克的这个朋友知道怎样修改交换机让接到电话的人在来电显示上看到伪造的号码，而事实上电话是从 Panda 办公室打来的。这种骗局之所以有效，是因为当地电话公司懒得去验证客户的呼叫号码是不是实际上付钱的那个号码。

杰克?道金斯需要的只是使用这种电话服务，幸运的是他的朋友与合作伙伴查尔斯?贝茨总是乐于伸出援助之手，而只收取象征性的费用。在这里，杰克和查尔斯临时修改了电话交换机的设置，让 Panda 公司的一条指定电话线路使用维克托?马丁的内部电话号码，这样电话看上去就是从星际漫游航空公司打出的了。

你的来电显示不会出错，很多人都这样想，在这里，琳达愉快地把资料传真给了她认为是产品推广部员工的人。

当杰克挂上电话时，查尔斯又把交换机的设置给改了回来。

### 13.1.3 过程分析

一些公司不想让客户或供应商知道他们员工的电话号码。比如，福特公司规定，从他们的客户支持中心打来的电话应当显示 800 号码和“福特支持”字样，而不是每一个客户支持代表真实的电话号码。微软公司则让员工自己选择是否把电话号码告诉别人，并不是每一个接到他们电话的人都能看到来电显示并找出他们的位置。通过这种方法公司便能保持内部号码的隐匿性。

但是修改交换机设置对于一些人而言是在是太简单了，比如，恶作剧爱好者、收账单的人、电话销售员，当然，还有社会工程师。

## 13.2 变奏：美国总统来电

作为洛杉矶 KFI 谈话节目"互联网黑暗面"的客串主持人，我认识电台的节目总监大卫，他是我见过的最勤奋最负责的人，你很难电话联系到他，因为他实在是太忙了。他不接任何电话，除非来电显示上出现了他必须谈话的人。

当我打电话给他时候，因为我的手机出了问题，他不知道是谁的电话所以没有接，而让它转到了语音信箱，这让我觉得很失败。

我和一个老朋友详细地讨论了这件事，他创办了一家专门为高科技公司提供办公室的房地产公司。我们一起制定了一个计划，他可以使用他们公司的子午线电话交换机，也就是说他可以修改主叫号码，就像刚才的故事描述的那样。每当我需要联系节目总监但又打不通电话时，我就请我的朋友帮忙修改来电显示上的号码，有时候我想让电话看上去是大卫的办公室助理打来的，有时候则是电台的控股公司。

但我最喜欢的还是把它改成大卫自己家的电话号码，他总是会接，因为他信任这个人。当他拿起电话并发现我再一次和他开了个玩笑时，他永远都是那么幽默。当然，他会在线足够长的时间解决我的所有问题。

当我在阿特响铃秀上证明这一小小的骗局时，我让我的来电显示出现了 FBI 洛杉矶总部的名字和号码。阿特对整件事情非常震惊，他警告我说这是违法的，但我告诉他这是完全合法的，只要不用来诈骗。在那次节目之后我收到了几百封电子邮件，他们想知道我是怎么做到的，现在你知道了。

这对社会工程师而言是获得信任的绝佳工具，例如，在社会工程学攻击的调查阶段，只要目标有来电显示，攻击者就可以让他或她的电话看上去是从可信的公司或员工打来的，收账单的人也可以让他或她的电话看上去是从你的办公场所打来的。

想一下这意味着什么，计算机入侵者可以在家里打电话给你，声称自己是你公司的 IT 部门员工，然后说服务器崩溃了，他需要你的密码来恢复你的文件；或者电话上出现了你的银行或证券交易所的名字，一个声音甜美的女孩想确认一下你的账户号码和你妈妈的婚前姓，另外，因为系统出了一些问题，她还需要核对你的 ATM PIN 码；股票市场的证券欺诈经营者可以让他们的电话看上去是来自美林证券公司或花旗银行；某个想盗窃你身份的人可以从移民局打来电话，让你告诉他你的签证卡号；一个嫉恨你的家伙可以打来电话声称自己来自 IRS（译者注：美国国税局）或 FBI。

如果你通过一个电话系统连接上了一个初始速率接口（PRI），那么再加上一点点从系统供应商的网站上学到的编程知识，你就可以用这种方法和你的朋友开玩笑。认识的某个人有强烈的政治愿望？你可以把呼叫号码改成 202-456-1414，这样他的来电显示就会出现“白宫”的名字。

他会认为自己接到了总统的电话！

这些故事要表达的意思很简单：不能信任来电显示，除非已经确认是内部号码。无论是在工作中还是在家里，每个人都需要知道这种骗局并意识到来电显示上出现的名字和电话号码是无法验证身份的。

米特尼克语录

下一次当你接到电话时，如果来电显示上的是你亲爱的老妈，谁知道啊——她可能是个年轻可爱的社会工程师。

## 13.3 无形的员工

雪莉?卡特拉斯（Shirley Cutlass）找到了一个新的令人激动的赚钱方法，告别长时间的既辛苦又乏味的工作，她加入到上百个侵淫此道数十年的行骗艺术家当中，成了一名身份窃贼。

现在她的目标是获取一家信用卡公司客户服务部门的机密信息，在常规的准备之后，她打到目标公司，告诉接线员她想要连线电信部门，然后她对电信部门的人说她想和语音信箱的管理员通话。

利用她之前搜集的信息，她自称为克里夫兰办公室的诺玛?托德（Norma Todd），现在你应该很熟悉这个骗局，她说她将在一周后前往公司总部，她需要一个这里的语音信箱，这样她就不用打长途电话查看她的语音信息。他说他会在办好之后回电话给她，因为会有一些她需要的信息。

她用迷人的声音说，“我在去开会路上，我能在一小时后打给你吗？”

当她打回去的时候，他说已经设置好了，然后是一些必要的信息——她的分机号和临时密码。他问她是否知道怎样更改语音信箱的密码，虽然她知道的并不比他少，但她还是让他讲解了一遍操作步骤。

“顺便问一句，”她说，“从我的旅馆，要打哪个号码才能查看我的信息？”他给了她那个号码。

然后雪莉打了进去，更改了密码并录入了新的问候语。

### 13.3.1 雪莉的入侵

到目前为止一切都很简单，现在她准备施展欺骗的艺术了。

她打电话到目标公司的客户服务部门，“克里夫兰办公室人力资源部，”她说，然后变化了一下这个耳熟能详的借口，“技术支持人员正在修理我的电脑，我需要你帮忙查找这些信息。”接着她提供了一些她想要窃取身份的人的名字和生日，然后她列出了她想要的信息：地址、母亲的婚前姓、卡号、信贷限额、可用信用、支付历史。“按这个号码打给我，”她给出了语音信箱管理员为她设置的内部分机号，“如果我不在的话，只要在我的语音信箱里留言就可以了。”

她一早上都在忙其它事情，然后在下午查看了她的语音信箱，她想要的信息都在。在挂电话之前，雪莉清除了问候语：如果不小心的话会留下她的声音记录。

身份盗窃是美国增长率最高的犯罪形式，“在”新世纪的犯罪中，总会有下一个受害者。雪莉用她刚刚得到的信用卡与身份信息开始了刷卡消费。

### 13.3.2 过程分析

在这个骗局中，攻击者首先让语音信箱管理员相信她是公司的一名员工，这样他就帮她设置了一个临时的语音信箱。如果他进一步进行了核实，他会发现她给出的名字和电话号码可以和公司的员工数据库列表匹配。

接下来的事情很简单了，以电脑故障为由，请求需要的信息，并要求在语音信箱中留言。有什么能阻止员工和同事分享信息？只要看到雪莉提供的内部分机号，就没有任何怀疑的理由。

米特尼克语录

试着偶尔打到你自己的语音信箱，如果你听到问候语不是你的声音，你可能已经遇到你的第一个社会工程师。

## 13.4 提供帮助的秘书

骇客（Cracker）罗伯特?乔迪（Robert Jorday）经常入侵一家环球公司的网络，鲁道夫海运公司。最终这家公司发现有人入侵了他们的终端服务器，通过这台服务器用户可以连接到公司的任意一台计算机。为了维护公司网络，这家公司决定在每一台终端服务器上添加一道拨号密码。

罗伯特伪装成法务部的律师打电话到网络操作中心说他无法连接网络，接电话的网络管理员解释说出台了新的安全措施，所有的拨号访问用户都必须从他们的经理那里获得一个每月密码。罗伯特想知道经理是怎样得到这个每月密码，得到的回答是，下个月的密码会写入备忘录，然后通过办公室邮寄给每一位公司经理。

这让事情变得很简单，罗伯特稍微调查了一下，然后在月初打电话到这家公司，连线了一位经理的秘书，她说自己叫珍妮特。他说，“嗨，珍妮特，我是研发部的兰迪?古德斯丁（Randy Goldstein），我知道备忘录里有从公司外部登录终端服务器的每月密码，但是我怎么也找不到，你能从你的备忘录找到它吗？”

是的，她说，她找到了。

他问她是否可以把它传真过来，然后她同意了，他给了她一个前台接待员（在这家公司的另一栋大楼里）的传真号码，他已经安排好了一切，包括把密码传真转发出去。在这里，罗伯特转发传真的方法有点与众不同，他给了接待员一个在线传真服务的号码，如果他们收到了传真，系统会自动转发到客户的电子邮箱地址。

新密码将被发送到一个 Email 秘密传送点，罗伯特选择了中国的免费电子邮箱。他知道如果这个传真被跟踪了，调查者可以与中国官方合作把他给揪出来，但是，他们也许并不想被这种小事打扰。最棒的是，他甚至没见过那台传真机。

米特尼克语录

人们总是乐于帮助一名熟练的社会工程师，接收一份传真并把它转发到另一个地方似乎是无害的，让一个接待员（或其他人）答应帮忙实在是太简单了。当有人向你请求一些信息时，如果你不认识他或无法核实他的身份，只要拒绝就可以了。

## 13.5 交通法庭

或许每一个接到过超速罚单的人都做过关于逃避处罚的白人梦，不去交通法规学习班，只支付罚款，或碰碰运气设法让法官相信警车计速器（或雷达测速仪）出了一些技术问题。利用系统的漏洞，这个美好的愿望即将实现。

### 13.5.1 骗局

虽然我不建议你使用这种方法逃避罚单（有句话说的好，请勿轻易尝试），但这仍然是一个很好的社会工程学案例。

我们就叫这个交通违规者保罗?杜里（Paul Durea）好了。

第一步

“霍伦贝克区，洛杉矶警察局（LAPD）。”

“你好，我想和传票管理员谈话。”

“我就是。”

“好的，我是米查姆和塔尔波特的代理律师，我需要在法庭上传唤一名警官。”

“没问题，你要传唤谁？”

“肯德尔警官是你们区的吗？”

“他的编号是？”

“21349。”

“是的，你什么时候需要他？”

“下个月的某个时候，我还需要传唤其他几个证人才能确定开庭时间，肯德尔警官下个月有哪些安排？”

“让我来看看……20 号到 30 号是他的假期，他将在 8 号和 16 号参加培训。”

“谢谢，我需要的就是这些，开庭日期定下来我会再打给你的。”

地方法院，办事员前台

保罗：“我想要确定一下这张交通告票的开庭日期。”

办事员：“好的，我可以帮你安排在下个月的 26 号。”

“好，我想要安排一次传唤。”

“你想为交通告票传唤某个人？”

“是的。”

“好吧，我们可以把传唤设在明天上午或者下午，你想设在什么时候？”

“下午。”

“传唤设在明天下午 1:30，在第六法庭。”

“谢谢，我会来的。”

地方法院，第六法庭

日期：星期四，下午 1:45

办事员：“杜里先生，请靠近长椅。”

法官：“杜里先生，你了解你的权利了吗？”

保罗：“是的，法官大人。”

法官：“你愿意参加交通法规学习班的培训吗？你的案子将在你成功完成 8 小时的课程后取消，我查看了你的档案，你目前符合标准。”

保罗：“不，法官大人。我恳请审判此案。还有一件事，法官大人，我要出国一段时间，只在 8 号和 9 号有空，能不能把我的案子的审判放在其中一天？我明天就要到欧洲进行商务旅行，我将在四周后回来。”

法官：“非常好，审判设在六月八号，上午 8:30，第四法庭。”

保罗：“谢谢你，法官大人。”

地方法院，第四法庭

八号那一天，保罗很早就到了法院。当法官进来的时候，办事员给了他一张未出庭的警官列表，法官召集了所有被告，包括保罗，然后告诉他们他们的案子被取消了。

### 13.5.2 过程分析

当警官开罚单的时候，他会把他的名字和他的证件号码写在上面（或者其它可以联系他的私人号码），找到他工作的地方简直是小菜一碟。只要打个电话到号码服务台，查询一下写在传票上的执法机构名（公路巡逻局、县警察局、或者其它），事情就成功了一半，接着和那个机构取得联系，他们能提供给呼叫者传票管理员的电话号码。

执法部门的官员经常被法院传唤出庭作证：这是他们的职责之一。当检察官或辩护律师需要一名警官出庭作证时，如果他知道系统是怎样运转的，他就会首先确认这名警官是否有时间出庭。这很容易办到：只要打个电话给那里的传票管理员就可以了。

在谈话中，律师通常会询问那名警官在某月某日是否时间，为了实现这个骗局，保罗稍微变通了一下：他用一个似是而非的理由获知了那名警官无法出庭的时间。

当保罗第一次到法院去的时候，他为什么不直接告诉法院办事员他想安排在哪一天？答案很简单——我个人认为，大多数地方的交通法院办事员不允许让公众成员选择开庭日期，如果办事员提出的日期当事人无法接受，她会提供一个折中的选择，但是她会做出很大的让步。另一方面，想要获得额外的传讯时间的人可能会更走运一些，保罗知道他可以申请传讯，并且法官通常会为传讯安排指定的日期。他请求在那名警官参加培训的那一天开庭，要知道在这种情况下，警员培训比出庭作证要重要得多。

米特尼克语录

人类的思想是一种神奇的产物，比如人们在脑海里设计骗局得到他们要想的东西或者脱离险境。你可以在公共与私营部门中利用同样的创造力与想像力保护信息与计算机系统的安全。所以，各位，当你们制定你们公司的安全策略的时候——要打破常规去思考问题。

在交通法院，如果传唤的警官没有出现——案子就会被取消，没有罚款，不用去交通学校，没有分数，最棒的是，不会留下任何交通肇事的记录！

我猜会有一些警务人员、法院办事员、检察官和类似的人读到这个故事会摇摇头，因为他们知道这种骗局是可行的，但他们只是摇摇头而已，我敢打赌不会有任何改变。就像电影《通天神偷》（1992 年）中科斯莫说的那样，“一切只和零与一有关”——意思是，最终，所有的东西都将归结为信息。

只要执法机构愿意把一名警官的日程表提供给任何一个打电话来的人，人们躲避交通罚单的能力就会一直存在下去。聪明的社会工程师可以利用它来获取你不想让他们知道的信息，在你的公司或机构的程序中有类似的缺口吗？

## 13.6 萨曼塔的报复

萨曼塔?格雷森生气了。

她一直在为她的大学商学位而努力，为此她还申请了一大笔助学贷款，因为她总是听到别人说，大学学位能让你成就一番事业，大学学位能让你赚到很多很多的钱。然后她毕业了，却发现自己连一份合适的工作都找不到。

收到蓝贝克制造公司的聘用协议着实让她高兴了好一阵子，虽然这份秘书工作对她而言实在是大材小用，但卡特莱特先生说他们很欣赏她，并承诺在下一个非行政职位空缺时将她纳入候选人中。

两个月后，她听说卡特莱特先生的一个产品采购经理离职了，那天晚上她很久都没有睡，想象着自己在五楼办公室出席会议并参与公司决策的样子。

第二天一大早她就遇上了卡特莱特先生，他说他们觉得在她胜任这一职位之前，她还需要学习更多的行业知识，然后他们从公司外面雇用了一个外行人，一个比她差多了的外行人。

她很快就明白了：这家公司有很多女职员，但她们清一色的都是秘书，他们不会给她一份经理工作，永远也不会。

### 13.6.1 报复

她花了差不多一个星期才想好怎样报复他们。大概一个月前的产品发布会上，有一家商业杂志的记者想要采访她，几周后那个人打来电话说，希望她能提供一些 Cobra 273 的未公开信息，作为回报，他会送花给她，并且如果这些信息很有吸引力，他会专门从芝加哥跑来约她吃饭。

她每天会有一段时间待在乔汉森先生的办公室里，所以当年轻的乔汉森先生登录公司网络的时候，她站在后面看得一清二楚（有时候这也称为肩窥），他输入的密码是“marty63”。

她的计划已经开始实施了。她记得有一份备忘录是在她来公司后不久分发的，她在其中找到了一份复印件并仿照原始版本打印了一份新的，内容如下：

TO：C. 比尔顿，IT 部

FROM：L. 卡特莱特，开发部

马丁?乔汉森将转到我部门的专业研究小组工作，因此我授权他访问开发组使用的服务器，乔汉森先生的安全配置将更新为产品开发者权限。

路易斯?卡特莱特

术语

肩窥：通过监视用户输入，窃取密码或其它用户信息的行为。

当大部分人都出去吃午餐的时候，她把卡特莱特先生的签名从最初的备忘录上剪切下来，粘贴到她的版本上面，并在四周涂上修正液。她把成果复印了一份，然后再复印了一份复印件，你几乎看不到签名四周的痕迹。最后她在卡特莱特先生办公室附近的传真机上把它发送了出去。

三天后，等到所有人都离开了公司，她走进乔汉森的办公室，尝试用的他的用户名和密码（marry63）登录网络，结果成功了。

只用了几分钟她就找到了 Cobra 273 的产品规格文件并将其下载到了 Zip 磁盘上。

当她在凉爽的夜间像风一般走入停车场的时候，那张磁盘正平平安安地待在她的钱包里，等待着和那名记者的见面。

### 13.6.2 过程分析

一个不满的员工，一次文件搜寻与快速剪切粘贴-修正液操作，少量有创意的复印与一份传真，然后，瞧！——她得到了机密的商业产品技术规格书。

几天以后，一家商业杂志的新闻记者独家报导了一个热门新产品的技术规格书和产品销售计划，这些都在产品发布之前几个月出现在了该杂志的所有订阅者手中，竞争对手将有几个月的时间抢先开发同类产品并在他们的广告活动中做好准备影响 Cobra 273 的发售。

当然，这家杂志绝不会透漏他们的消息来源。

## 13.7 防范措施

当被请求任何有益于竞争对手的贵重、敏感或关键信息时，员工们必须了解通过来电显示验证外部人员的身份是不被允许的，必须要有一些其它的验证方法，比如与此人的主管联系，确认这些请求是合法的，用户已被授权接收这些信息。

各公司必须自行控制验证程序中安全与效率的平衡。哪些安全措施应当被优先考虑？员工们会不会抵制这些安全措施？甚至绕过它们以完成他们的工作任务？员工们了解为什么安全对公司和他们自己都如此重要吗？这些问题的回答将帮助建立基于企业文化和商业需求的安全策略。

大部分人难免会认为这些安全措施妨碍到了他们的工作，连绕过它们都是在浪费时间。可以通过宣传和教育，鼓励员工们把安全工作当成他们的日常职责。

尽管不能用来电显示验证外部呼叫者的身份，但是另一种叫做自动号码识别（ANI）的服务却可以。当一家公司开通了免付费电话（由公司支付呼入费用）时，这种服务可以准确地识别呼叫者。与来电显示不同的是，电话公司交换机不会接受客户发送过来的呼叫号码，ANI 传输的号码是分配给呼叫用户的付费号码。

另外，一些调制解调器厂商把来电显示功能添加到了他们的产品里，为保护企业网络而设定了只接受指定电话号码的远程访问。调制解调器的来电显示功能可以在安全级别较低的环境下作为身份验证的手段，但是，众所周知，伪造来电显示对于计算机入侵者而言并不是一件难事，因此在安全级别较高的情况下不能据此判断呼叫者的身份或位置。

在身份盗窃的案例中，管理员在企业电话系统上为入侵者创建了一个语音信箱，为了防止此类事件的发生，企业应当规定所有的电话系统、语音信箱和所有的企业目录（不管是印刷的还是在线的）在被使用时必须提出书面请求，形式固定，员工经理应当在这份请求上签字，然后交语音信箱管理员核实。

企业安全策略应当规定，在创建新的计算机账户或增加账户权限时，必须向系统管理员或他（或她）的指定负责人核实该请求，可以在纸质或在线公司目录上找到相应的电话号码。如果你们公司使用经过数字签名的安全电子邮件，这种折中的验证方法也可以接受。

记住，每一个员工（不管他是否能访问公司的计算机系统）都有被社会工程师利用的可能性。每个人都必须接受安全知识培训。所有的行政助理、接待员、电话接线员和安全警卫都必须要熟知各类社会工程学攻击（大多数都是针对他们的），这样他们才能更好地防范这些攻击。