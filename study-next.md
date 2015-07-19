#  接下来学习什么？

如果你已经完全读完了这本书并且也实践着编写了很多程序，那么你一定已经能够非常熟练自如地使用 Python 了。你可能也已经编写了一些 Python 程序来尝试练习各种 Python 技能和特性。如果你还没有那样做的话，那么你一定要快点去实践。现在的问题是“接下来学习什么？”。

我会建议你先解决这样一个问题：创建你自己的命令行 *地址簿* 程序。在这个程序中，你可以添加、修改、删除和搜索你的联系人（朋友、家人和同事等等）以及它们的信息（诸如电子邮件地址和/或电话号码）。这些详细信息应该被保存下来以便以后提取。

思考一下我们到目前为止所学的各种东西的话，你会觉得这个问题其实相当简单。如果你仍然希望知道该从何处入手的话，那么这里也有一个提示。

**提示（其实你不应该阅读这个提示）** 创建一个类来表示一个人的信息。使用字典储存每个人的对象，把他们的名字作为键。使用 cPickle 模块永久地把这些对象储存在你的硬盘上。使用字典内建的方法添加、删除和修改人员信息。

一旦你完成了这个程序，你就可以说是一个 Python 程序员了。现在，请立即寄一封信给我感谢我为你提供了这本优秀的教材吧。是否告知我，如你所愿，但是我确实希望你能够告诉我。

这里有一些继续你的 Python 之路的方法：

## 图形软件

使用 Python 的 GUI 库——你需要使用这些库来用 Python 语言创建你自己的图形程序。使用 GUI 库和它们的 Python 绑定，你可以创建你自己的 IrfanView、Kuickshow 软件或者任何别的类似的东西。绑定让你能够使用 Python 语言编写程序，而使用的库本身是用 C、C++或者别的语言编写的。

有许多可供选择的使用 Python 的 GUI：

- PyQt 这是 Qt 工具包的 Python 绑定。Qt 工具包是构建 KDE 的基石。Qt，特别是配合 Qt Designer 和出色的 Qt 文档之后，它极其易用并且功能非常强大。你可以在 Linux 下免费使用它，但是如果你在 Windows 下使用它需要付费。使用 PyQt，你可以在 Linux/Unix 上开发免费的（GPL 约定的）软件，而开发具产权的软件则需要付费。一个很好的 PyQt 资源是《[使用 Python 语言的 GUI 编程：Qt 版》](http://www.opendocs.org/pyqt/)请查阅[官方主页](http://www.riverbankcomputing.co.uk/pyqt/index.php)以获取更多详情。

- PyGTK 这是 GTK+工具包的 Python 绑定。GTK+工具包是构建 GNOME 的基石。GTK+在使用上有很多怪癖的地方，不过一旦你习惯了，你可以非常快速地开发 GUI 应用程序。Glade 图形界面设计器是必不可少的，而文档还有待改善。GTK+在 Linux 上工作得很好，而它的 Windows 接口还不完整。你可以使用 GTK+开发免费和具有产权的软件。请查阅[官方主页](http://www.pygtk.org/)以获取更多详情。

- wxPython 这是 wxWidgets 工具包的 Python 绑定。wxPython 有与它相关的学习方法。它的可移植性极佳，可以在 Linux、Windows、Mac 甚至嵌入式平台上运行。有很多 wxPython 的 IDE，其中包括 GUI 设计器以及如 [SPE（Santi's Python Editor）](http://spe.pycs.net/)和 [wxGlade](http://wxglade.sourceforge.net/) 那样的 GUI 开发器。你可以使用 wxPython 开发免费和具有产权的软件。请查阅[官方主页](http://www.pygtk.org/)以获取更多详情。
 
- TkInter 这是现存最老的 GUI 工具包之一。如果你使用过 IDLE，它就是一个 TkInter 程序。在 [PythonWare.org](http://www.pythonware.com/library/tkinter/introduction/index.htm) 上的 TkInter 文档是十分透彻的。TkInter 具备可移植性，可以在 Linux/Unix 和 Windows 下工作。重要的是，TkInter 是标准 Python 发行版的一部分。

- 要获取更多选择，请参阅 [Python.org 上的 GUI 编程 wiki 页](http://www.python.org/cgi-bin/moinmoin/GuiProgramming)。
     
### GUI 工具概括

不幸的是，并没有单一的标准 Python GUI 工具。我建议你根据你的情况在上述工具中选择一个。首要考虑的因素是你是否愿意为 GUI 工具付费。其次考虑的是你是想让你的程序运行在 Linux 下、Windows 下还是两者都要。第三个考虑因素根据你是 Linux 下的 KDE 用户还是 GNOME 用户而定。

> **未来的章节**  
我打算为本书编写一或两个关于 GUI 编程的章节。我可能会选择 wxPython 作为工具包。如果你想要表达你对这个主题的意见，请加入 [byte-of-python 邮件列表](http://lists.ibiblio.org/mailman/listinfo/byte-of-python)。在这个邮件列表中，读者会与我讨论如何改进本书。

## 探索更多内容

- **Python 标准库**是一个丰富的库，在大多数时候，你可以在这个库中找到你所需的东西。这被称为 Python 的“功能齐全”理念。我强烈建议你在开始开发大型 Python 程序之前浏览一下 [Python 标准文档](http://docs.python.org/)。

- [Python.org](http://www.python.org/)——Python 编程语言的官方主页。你可以在上面找到 Python 语言和解释器的最新版本。另外还有各种邮件列表活跃地讨论 Python 的各方面内容。

- comp.lang.python 是讨论 Python 语言的世界性新闻组。你可以把你的疑惑和询问贴在这个新闻组上。可以使用 [Google 群](http://groups.google.com/groups?hl=en&lr=&ie=UTF-8&group=comp.lang.python)在线访问这个新闻组，或加入作为新闻组镜像的[邮件列表](http://mail.python.org/mailman/listinfo/python-list)。

- [《Python 实用大全》](http://aspn.activestate.com/ASPN/Python/Cookbook/)是一个极有价值的秘诀和技巧集合，它帮助你解决某些使用 Python 的问题。这是每个 Python 用户必读的一本书。

- 《[迷人的 Python》](http://gnosis.cx/publish/tech_index_cp.html)是 David Mertz 编著的一系列优秀的 Python 相关文章。

- [《深入理解 Python》](http://www.diveintopython.org/)是给有经验的 Python 程序员的一本很优秀的书。如果你已经完整地阅读了本书，那么我强烈建议你接下来阅读《深入理解 Python》。它覆盖了包括 XML 处理、单元测试和功能性编程在内的广泛的主题。

- [Jython](http://www.jython.org/) 是用 Java 语言实现的 Python 解释器。这意味着你可以用 Python 语言编写程序而同时使用 Java 库！Jython 是一个稳定成熟的软件。如果你也是一个 Java 程序员，我强烈建议你尝试一下 Jython。

- [IronPython](http://www.ironpython.com/) 是用 C#语言实现的 Python 解释器，可以运行在.NET、Mono 和 DotGNU 平台上。这意味着你可以用 Python 语言编写程序而使用.NET 库以及其他由这三种平台提供的库！IronPython 还只是一个前期 alpha 测试软件，现在还只适合用来进行试验。Jim Hugunin，IronPython 的开发者，已经加入了微软公司，将在将来全力开发一个完整版本的 IronPython。

- [Lython](http://www.caddr.com/code/lython/) 是 Python 语言的 Lisp 前段。它类似于普通的 Lisp 语言，会被直接编译为 Python 字节码，这意味着它能与我们普通的 Python 代码协同工作。

- 另外还有很多很多的 Python 资源。其中比较有趣的有 [Daily Python-URL](http://www.pythonware.com/daily/)!，它使你保持与 Python 的最新进展同步。另外还有 [Vaults of Parnassus](http://www.vex.net/parnassus/)、[ONLamp.com Python DevCenter](http://www.onlamp.com/python/)、[dirtSimple.org](http://dirtsimple.org/)、[Python Notes](http://pythonnotes.blogspot.com/) 等等。



## 概括

现在，我们已经来到了本书的末尾，但是就如那句名言，这只是 *开始的结束* ！你现在是一个满怀渴望的 Python 用户，毫无疑问你准备用 Python 解决许多问题。你可以使你的计算机自动地完成许多先前无法想象的工作或者编写你自己的游戏，以及更多别的什么东西。所以，请出发吧！


## A. 自由/开放源码软件（FLOSS）

FLOSS 基于社区的概念，而它本身基于共享，特别是知识共享的概念。FLOSS 可以免费使用、修改和再发行。

如果你已经读了本书，那么你一定熟悉 FLOSS，因为你一直在使用 **Python**！

如果你想要了解更多的 FLOSS，你可以探索下面这个列表中的软件。我列出了一些最著名的 FLOSS 以及那些可以跨平台（即在 Linux、Windows 等）工作的 FLOSS。这样你无需马上切换到 Linux 就可以尝试使用这些软件了， *尽管你最终一定会转到 Linux 上的* 。

- **Linux** 这是一个正在慢慢被世界接纳的 FLOSS 操作系统！它最初由 Linus Torvalds 在学生时候开发。现在，它已经可以与微软 Windows 相匹敌。最新的 2.6 版本核心，无论从速度、稳定性还是扩展性角度来说，都是一个巨大的突破。【[Linux 核心](http://www.kernel.org/)】

- **Knoppix** 这是一个仅仅在 CD 上运行的 Linux 发行版！它不需要安装——你只需要重新启动你的计算机，把 CD 放入光驱，就可以开始使用一个完全的 Linux 发行版了！你可以使用所有的随标准 Linux 发行版发行的 FLOSS，如运行 Python 程序、编译 C 程序、看电影等等。然后再次重启你的计算机，取出 CD，就可以使用你现有的操作系统了，就好像什么都没有发生过一样。【[Knoppix](http://www.knopper.net/)】

- **Fedora** 这是一个由社区开发维护的发行版，由 Red Hat 公司赞助。它是最流行的 Linux 发行版之一。它包含 Linux 核心、KDE、GNOME 和 XFCE 桌面以及众多的 FLOSS，而所有这些都易于安装、易于使用。

  如果你担心你是一个完全的 Linux 生手，那么我推荐你尝试 **Mandrake Linux**。最新发布 Mandrake 10.1 确实很棒。【[Fedora Linux](http://fedora.redhat.com/)、[Mandrake Linux](http://www.mozilla.org/products/thunderbird)】

- **OpenOffice.org** 这是一个优秀的办公套件，它基于 Sun Microsystems 的 StarOffice 软件。OpenOffice 由文本编写器、演讲辅助、电子表格和绘图组件等等组成。它甚至可以方便地打开和编辑微软 Word 和 PowerPoint 文件。它可以在几乎所有平台上运行。即将推出的 OpenOffice 2.0 有一些重大的改进。【OpenOffice】

- **Mozilla Firefox** 这是被认为可以在未来几年击败 Internet Explorer（仅按照市场份额计算）的下一代网络浏览器。它极快，它的一些合理的、令人印象深刻的特性广受好评。它的扩展理念允许在它上面添加各种功能。

  它的姐妹产品 Thunderbird 是一个优秀的电子邮件客户端，使阅读电子邮件变得十分快捷。【Mozilla Firefox、Mozilla Thunderbird】

- **Mono** 这是一个微软.NET 平台的开源实现。它使我们可以在 Linux、Windows、FreeBSD、Mac OS 和许多其他平台上创建和运行.NET程序。Mono 执行 CLI 和 C#的 ECMA 标准，这个标准已经由微软、英特尔和惠普提交称为一个开放标准。这也是迈向 ISO 标准的一步。

  目前，Mono 包含一个完整的 C#主控制台（它本身也由 C#编写！）、一个具备完整特性的 ASP.NET 实现、许多数据库 ADO.NET 提供器另外还有每天不断改善和增加的新特性。【[Mono](http://www.mono-project.com/)、[ECMA](http://www.ecma-international.org/)、[Microsoft .NET](http://www.microsoft.com/net)】

- **Apache** 网络服务器 这是最流行的开源网络服务器。事实上，它是地球上最流行的网络服务器！它运行着几乎 60％的网站。对——Apache 处理的网站比它所有的竞争对手（包括微软 IIS）之和还要多。【[Apache](http://www.apache.org/)】

- **MySQL** 这是一个极其流行的开源数据库服务器。它以它的快速最为著名。在它的最新版本中又添加了更多的特性。【[MySQL](http://www.mysql.com/)】

- **MPlayer** 这是一个视频播放器，可以播放 DivX、MP3、Ogg、VCD、DVD……谁说开源软件就不能具有趣味呢？【[MPlayer](http://www.mplayerhq.hu/)】

- **Movix** 这是一个 Linux 发行版，它基于 Knoppix 仅仅在 CD 上运行用来播放电影！你可以创建 Movix 的 CD。它们是可启动的 CD，当你重启计算机的时候，放入 CD，电影就会自己开始播放！使用 Movix 观看电影，你甚至不需要硬盘。【[Movix](http://movix.sourceforge.net/)】

上面这个列表只是希望给你一个大概的印象——还有很多别的优秀 FLOSS，比如 Perl 语言、PHP 语言、Drupal 网站内容管理系统、PostgreSQL 数据库服务器、TORCS 赛车游戏、KDevelop IDE、Anjuta IDE、Xine——电影播放器、VIM 编辑器、Quanta+编辑器、XMMS 音频播放器、GIMP 图像编辑程序……这个列表可以一直继续下去。

访问下述网站以获取更多 FLOSS 信息：

- [SourceForge](http://www.sourceforge.net/)

- [FreshMeat](http://www.freshmeat.net/)

- [KDE](http://www.kde.org/)

- [GNOME](http://www.gnome.org/)

要获知 FLOSS 世界的最新进展，请访问下述网站：

- [OSNews](http://www.osnews.com/)

- [LinuxToday](http://www.linuxtoday.com/)

- [NewsForge](http://www.newsforge.com/)

- [SwaroopCH's blog](http://www.swaroopch.info/blog)

那么，现在就出发去探索广博、免费、开放的 FLOSS 世界了吧！

## B. 关于本书

### 后记

我在编写本书时使用的几乎所有软件都是 免费开放源码的软件 。在编写本书的第一个草稿的时候，我使用的是 Red Hat 9.0 Linux，而现在第六次改写的时候，使用的是 Fedora Core 3 Linux。

最初，我使用 KWord 编写本书（在前言的[本书的由来](http://woodpecker.org.cn/abyteofpython_cn/chinese/pr01s02.html)中已经介绍了）。后来，我开始使用 DocBook XML 和 Kate，但是我发现这样太乏味。所以，我开始使用 OpenOffice，它对格式的控制以及生成 PDF 的能力是很棒的。但是它生成的 HTML 过于庞大。最后，我发现了 XEmacs，于是我又开始重新使用 DocBook XML 来编写本书，并且那时我打算把这个模式作为将来长期的方案。在这个最新的第六次重写时，我决定使用 Quanta+ 来编辑。

我使用了标准的 XSL 样式表，它随 Fedora Core 3 Linux 附带。另外，我也使用了标准的默认字体。我编写了一个 CSS 文件来为 HTML 页增加颜色和样式。同时，我还用 Python 语言编写了一个粗劣的词汇分析器，它自动为书中所有的程序进行语法加亮。

### 关于作者

Swaroop C. H. 在 Yahoo!驻印度班加罗尔的办事处工作，他十分热爱他的工作。他目前在技术领域的兴趣有：包括 Linux、DotGNU、Qt 和 MySQL 在内的 FLOSS、Python 和 C#编程语言。另外他在业余时间编写一些如本书这样的教材和其他软件，以及编写他的网上日记。他的其他爱好有咖啡、Robert Ludlum 的小说、远足和政治等。

如果你有兴趣了解他的更多故事，可以在 [www.swaroopch.info](http://www.swaroopch.info/) 上查看他的网上日记。

### 关于译者

沈洁元 目前是上海交通大学无线通信研究所的一名硕士研究生。他现在的研究领域主要在多载波 CDMA 系统的同步、信道估计、多用户检测等方面。Python 语言（和 Numeric 库）是他目前在进行仿真和其他科研工作时使用的主要编程语言。在业余时间，他乐衷于各种 FLOSS，如 FreeBSD 操作系统、PyGTK 等等。电影、F1 赛车和网球也是他的兴趣爱好。

### 关于简体中文译本

在半年多前开始学习使用 Python 编程语言。正如 Swaroop 在本书中所说的那样，它很快就成为“我最喜欢的编程语言”。目前我的几乎所有编程工作都使用 Python。从我的切身体会来说，Python 最大的特点就是易懂、易用、高效率。我相信，如果你已经学完了本书，并且尝试着编写了一些程序后，你一定会有相同的感受。

Swaroop C. H.的这本书是我学习 Python 时的第一本教材。它简单明晰，可以在最短的时间内把你领进 Python 的世界。它不是很长，但是覆盖了几乎所有重要的 Python 知识。在第一次读本书的时候，我就深切的感到这是给 Python 初学者的一本极佳教材，应该是每一位 Python 初学者的第一本教材。

我利用业余时间翻译了这本教材的简体中文译本。一方面是为了感谢 Swaroop 给我们带来了那么好的一本教材，同时也是为了把本书介绍给更多的中国读者，希望让 Python 在中国更加普及。如果读了本书之后，你开始将 Python 应用于你的工作学习，这将是我和 Swaroop 以及其他 Python 用户的荣幸。如果你在学习和使用 Python 的过程中，遇到任何问题，你一定要试试使用 Python 的[邮件列表资源](http://mail.python.org/mailman/listinfo)。你一定会得到世界各地的 Python 高手的热情帮助。

本书的英文原名为《A Byte of Python》。经过与 Swaroop 的探讨，在翻译时，我把书名定为《简明  Python 教程》，以充分体现本书区别于其他 Python 教材的鲜明特色。在翻译这本简体中文译本时，我力求准确清晰。在原书中个别不甚清晰的地方，都与作者进行讨论后再行翻译。另外，在这本简体中文译本中，我还为书中所有的程序例子配上了源代码，并且在书后附上了中英对照的[术语表](http://woodpecker.org.cn/abyteofpython_cn/chinese/apcs02.html)，以便读者以后继续学习其他 Python 英文资料。

本译本作为原书的派生作品，依照[创作公用约定（署名-非派生作品-非商业用途）](http://www.creativecommons.cn/licenses/by-nd-nc/1.0/)发布。简单地说，你只要署上我的名字，就可以免费复制、分发和展示本译本。未得到我的允许，你禁止把本译本用于商业目的，也不能再在本译本的基础上修改、派生新的作品。

如果你对本书和译本有任何批评和建议，十分欢迎你与我联系：orion_val@163.com。

## C. 修订记录

### 时间表

本文档在 2005 年 1 月 13 日 4 点 02 分生成。

**修订记录**

1.20 版	2005 年 1 月 13 日  
使用 FC3 上的 Quanta+的完全重写。做了许多修正和更新。添加了许多新的例子。重写了我的 DocBook 设置。  
1.15 版	2004 年 3 月 28 日  
少量修订。  
1.12 版	2004 年 3 月 16 日  
添加修正了一些内容。  
1.10 版	2004 年 3 月 9 日  
感谢我的热情读者的帮助，我对更多的笔误做了修改。  
1.00 版	2004 年 3 月 8 日  
在从读者处获得了大量反馈和建议之后，我对本书的内容做了重要的修订，并且改正了一些笔误。  
0.99 版	2004 年 2 月 22 日  
增加了模块一章。增加了对可变数目函数参数的详细介绍。  
0.98 版	2004 年 2 月 16 日  
编写了一个 Python 脚本和 CSS 样式表来改善 XHTML 的输出效果。其中包括一个功能还很拙劣的词汇分析器，用来自动地为程序做类似于 VIM 地语法加亮。  
0.97 版	2004 年 2 月 13 日  
（再次）使用 DocBook XML 完全重写。本书改进了许多——更加有条理和易读。    
0.93 版	2004 年 1 月 25 日  
增加了关于 IDLE 的介绍以及更多 Windows®相关的话题  。
0.92 版	2004 年 1 月 5 日  
修改了几个例子。  
0.91 版	2003 年 12 月 30 日  
修正了排版错误。改进了许多章节的内容。  
0.90 版	2003 年 12 月 18 日  
增加了 2 章。使用 OpenOffice 格式修订。  
0.60 版	2003 年 11 月 21 日  
完全地重写和扩展。  
0.20 版	2003 年 11 月 20 日  
修改了一些排版错误和其他错误。  
0.15 版	2003 年 11 月 20 日  
改用 DocBook XML。  
0.10 版	2003 年 11 月 14 日  
最初使用 KWord 编写的草稿。  

### 术语表

<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{font-family:Arial, sans-serif;font-size:14px;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
.tg th{font-family:Arial, sans-serif;font-size:14px;font-weight:normal;padding:10px 5px;border-style:solid;border-width:1px;overflow:hidden;word-break:normal;}
</style>
<table class="tg">
  <tr>
    <th class="tg-031e">argument</th>
    <th class="tg-031e">实参</th>
  </tr>
  <tr>
    <td class="tg-031e">attribute</td>
    <td class="tg-031e">属性</td>
  </tr>
  <tr>
    <td class="tg-031e">base class</td>
    <td class="tg-031e">基本类</td>
  </tr>
  <tr>
    <td class="tg-031e">block</td>
    <td class="tg-031e">块</td>
  </tr>
  <tr>
    <td class="tg-031e">character</td>
    <td class="tg-031e">字符</td>
  </tr>
  <tr>
    <td class="tg-031e">class</td>
    <td class="tg-031e">类</td>
  </tr>
  <tr>
    <td class="tg-031e">comment</td>
    <td class="tg-031e">注释</td>
  </tr>
  <tr>
    <td class="tg-031e">complex number</td>
    <td class="tg-031e">复数</td>
  </tr>
  <tr>
    <td class="tg-031e">derived class</td>
    <td class="tg-031e">导出类</td>
  </tr>
  <tr>
    <td class="tg-031e">dictionary</td>
    <td class="tg-031e">字典</td>
  </tr>
  <tr>
    <td class="tg-031e">escape sequence</td>
    <td class="tg-031e">转义符</td>
  </tr>
  <tr>
    <td class="tg-031e">exception</td>
    <td class="tg-031e">异常</td>
  </tr>
  <tr>
    <td class="tg-031e">expression</td>
    <td class="tg-031e">表达式</td>
  </tr>
  <tr>
    <td class="tg-031e">field</td>
    <td class="tg-031e">域</td>
  </tr>
  <tr>
    <td class="tg-031e">float</td>
    <td class="tg-031e">浮点数</td>
  </tr>
  <tr>
    <td class="tg-031e">function</td>
    <td class="tg-031e">函数</td>
  </tr>
  <tr>
    <td class="tg-031e">identifier</td>
    <td class="tg-031e">标识符</td>
  </tr>
  <tr>
    <td class="tg-031e">indentation</td>
    <td class="tg-031e">缩进</td>
  </tr>
  <tr>
    <td class="tg-031e">indexing</td>
    <td class="tg-031e">索引</td>
  </tr>
  <tr>
    <td class="tg-031e">instance</td>
    <td class="tg-031e">实例</td>
  </tr>
  <tr>
    <td class="tg-031e">integer</td>
    <td class="tg-031e">整数</td>
  </tr>
  <tr>
    <td class="tg-031e">list</td>
    <td class="tg-031e">列表</td>
  </tr>
  <tr>
    <td class="tg-031e">list comprehension</td>
    <td class="tg-031e">列表综合</td>
  </tr>
  <tr>
    <td class="tg-031e">literal constant</td>
    <td class="tg-031e">字面意义上的常量</td>
  </tr>
  <tr>
    <td class="tg-031e">logical line</td>
    <td class="tg-031e">逻辑行</td>
  </tr>
  <tr>
    <td class="tg-031e">long integer</td>
    <td class="tg-031e">长整数</td>
  </tr>
  <tr>
    <td class="tg-031e">method</td>
    <td class="tg-031e">方法</td>
  </tr>
  <tr>
    <td class="tg-031e">module</td>
    <td class="tg-031e">模块</td>
  </tr>
  <tr>
    <td class="tg-031e">namespace</td>
    <td class="tg-031e">名称空间</td>
  </tr>
  <tr>
    <td class="tg-031e">object</td>
    <td class="tg-031e">对象</td>
  </tr>
  <tr>
    <td class="tg-031e">operand</td>
    <td class="tg-031e">操作数</td>
  </tr>
  <tr>
    <td class="tg-031e">operator</td>
    <td class="tg-031e">运算符</td>
  </tr>
  <tr>
    <td class="tg-031e">parameter</td>
    <td class="tg-031e">形参</td>
  </tr>
  <tr>
    <td class="tg-031e">pickle</td>
    <td class="tg-031e">储存器</td>
  </tr>
  <tr>
    <td class="tg-031e">physical line</td>
    <td class="tg-031e">物理行</td>
  </tr>
  <tr>
    <td class="tg-031e">sequence</td>
    <td class="tg-031e">序列</td>
  </tr>
  <tr>
    <td class="tg-031e">shebang line</td>
    <td class="tg-031e">组织行</td>
  </tr>
  <tr>
    <td class="tg-031e">slicing</td>
    <td class="tg-031e">切片</td>
  </tr>
  <tr>
    <td class="tg-031e">statement</td>
    <td class="tg-031e">语句</td>
  </tr>
  <tr>
    <td class="tg-031e">string</td>
    <td class="tg-031e">字符串</td>
  </tr>
  <tr>
    <td class="tg-031e">subclass</td>
    <td class="tg-031e">子类</td>
  </tr>
  <tr>
    <td class="tg-031e">superclass</td>
    <td class="tg-031e">超类</td>
  </tr>
  <tr>
    <td class="tg-031e">tuple</td>
    <td class="tg-031e">元组</td>
  </tr>
  <tr>
    <td class="tg-031e">type</td>
    <td class="tg-031e">类型</td>
  </tr>
  <tr>
    <td class="tg-031e">variable</td>
    <td class="tg-031e">变量</td>
  </tr>
</table>