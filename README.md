﻿# 北京邮电大学本科学士学位论文模板（本科毕业设计模板）
* 作者：Caspar Zhang    <casparant@gmail.com>
* 修改：Bing Hsu        <hello@antinucleon.com>
* 修改：Guohua Wu       <ghmeta@163.com>
* 修改：Qiang Sheng     <sqyx008@outlook.com>

# 主要修改
- 加入外文译文和原文板块（4/24）
- 将附录合并于主文件（4/24）
- 将封面、诚信声明改为PDF导入（4/24）
- 修正了参考文献中“et al”和“等”的样式问题（4/24）
- 修正正文行间距为1.2倍（4/24）
- 修正“定义”类型的编号方法（修正后同图表编号形式）（4/28）
- 新增并调校“代码”框格式，附示例（指导手册无要求，根据实际需求编入）（4/29）
- 为便于阅读学习，重编示例文本（4/29）
- 全面按照指导手册要求顺序，插入任务书、成绩评定表、开题报告、中期检查表的PDF（4/29）
- 修正原示例中使用\ref引用公式的错误，已改为\eqref（4/29）
- 修正英文学位论文引用形式的BUG（4/29）
- 示例文本中新增“列表”示例（5/2）
- 迁移示例文本中大部分\usepackages至.sty文件中（5/2）
- 将任务书文档（task.*）更新至新版本（5/8）
- 启用AutoFakeBold以应对Windows自带黑体无style=Bold的情况（5/8）（感谢<a href="https://github.com/RicardoMing">RicardoMing</a>）
- 修正引用中“@article”类型的格式问题（5/9）
- 对照Word版本设置正文行间距（Word版的1.2倍）和目录行间距（20磅）至目测一致（5/13）

# 系统需求
- Windows

    建议直接安装TeX Live（其中已包含需要的XeLaTeX和BibTeX），同时安装TeXworks（安装过程中有勾选框，选中即可）。你也可以使用“TeX Live + 自己喜爱的编辑器 + 扩展”的方式，如使用**TeX Live + Visual Studio Code + LaTeX workshop**或**TeX Live + Atom + language-latex + latex + pdf-view**。
    
    传送门：https://www.tug.org/texlive/    （流量不多的同学可以到BYRBT去下载）

- Mac OS 

    建议直接安装MacTeX，编辑器可以使用MacTeX自带的TeXshop，也可以使用TeXpad等其它选择

    传送门：http://www.tug.org/mactex/    （流量不多的同学可以到BYRBT去下载）

    （感谢<a href="https://github.com/MrAdonis">Li Jiarong</a>提供）

# 如何使用
编辑以下文件

- main.cfg: 包含了论文中需要填写的项目，比如论文名称等。论文的致谢部分也放在了这里

- abstract.cfg: 包含了论文的中英文摘要

- main.tex: 论文的主体、附录、外文译文

- bib.ref: 论文的参考文献库

用素材填充以下文件夹

- pictures:将图片放入该文件夹

- docs：将封面（cover）、诚信声明（statement）、外文文献原文（translation）、任务书（task）、成绩评定表（scoreTable）、开题报告（openingReport）和中期检查表（interimReport）的PDF放入该文件夹。为了保持清晰度，请在从Word输出PDF时尽可能选择**高质量**的设置（修正官方缺陷的封面及其他材料的word版已放入该文件夹，编辑并保存为PDF即可）

教务处官方相关模板请访问https://jwc.bupt.edu.cn/list/list.php?p=9_38_1

在TeXworks中编译main.tex即可，main.pdf即最终输出。

# 编译

在TeX Live环境下

先用XeLaTeX编译一遍；

再用BibTeX编译一遍；

再用XeLaTeX编译一遍。

（如果里面引用号码没有显示，就再XeLaTeX编译一遍。）

# 初始发布日期
2018/4/24

# FAQ

- **Q:LaTeX怎么这么麻烦？**

    A:使用LaTeX排版学术材料是极受欢迎的，优秀的国际会议和权威的学术杂志鲜见不接受LaTeX投稿的，相反，它们会主动提供符合自家排版要求的LaTeX模板，学者不需要再根据其要求大费周折。当然，它对新手不如word友好，因为其不具有“所见即所得”的特性。但是，“信息黄埔”的你们，应该对“看代码→写代码→编译→看结果”这一套十分熟悉，熟练后他会让你不再陷于反反复复调整格式的泥淖。

- **Q:用Word排版有那么不堪么？**

    A:微软的Word是一个优秀的文字处理软件，但是我们很多同学使用得非常肤浅，就好像你还能时常见到“用敲空格的方式把一个标题居中”的人。如果你不太懂自动生成目录，不太懂项目编号，不太懂文档内链接，不太懂上下标，不太懂Word的公式编辑器，不太会调整段落与缩进，不太会处理表格的边框长度和宽度，不太会设置页眉页脚，不太会分节分页，不太会对不同节设置不同页码格式，不太会用合适的方式排列图文……可以说，**你对Word排版的学习成本也是很高的**。

- **Q：为什么我在TeXworks中编译，到“Require XeLaTeX”处就不动了？**

    A:正如编译提示所言，它需要XeLaTeX。请注意编辑器左上角是否选择“XeLaTeX”，默认状态下是pdfLaTeX。

- **Q：LaTeX语句书写有误，导致编译卡在一半怎么办？**

    A:TeXworks中，本次编译可以通过在下方输入框敲击Enter以忽略错误完成，但有时错误无法忽略会导致本次输出PDF不成功。修正好错误后，到“文件”中选择“删除辅助文件”，然后再重新编译即可。
    
- **Q：我已经开始写毕设论文了，但该项目的一些样式文件做了更新，怎么办？**

    A:从上面的资料你已经知道需要编辑的文件有哪些，给它们备个份，然后```git pull ```一下，再把备份文件换回；或者直接全盘在另一文件夹编辑你的文档，把更新的配置文件复制过去覆盖即可。
 
- **Q:引用文献的BibTeX文件可以从哪里获取？**

    A:几乎任何学术文献库都会提供BibTeX格式的引用数据，你可以使用**JabRef**来管理和自动生成你引用文献的BibTeX。但在引用量不大的情况下，直接去学术搜索引擎和数据库（Google Scholar/IEEEXplore/ACM digital library/Springer Link/必应学术/百度学术）或学术组织官网（CVF）去复制也不麻烦。

# BTW
欢迎大家去顶在北邮人论坛推广本项目的帖子：https://bbs.byr.cn/#!article/Paper/30043

欢迎提出issue，更欢迎提pull request，**关于模板的问题请使用Issue功能提出，其它途径无法得到答复保证**。

欢迎广而告之，欢迎在word调格式被折磨时投奔初期有一点学习（模仿）成本的LaTeX模板

我不能保证一切都能过教务部门的关（虽然使用了Word的其它人也不能保证），不过我会在2018年使用这个模板提交论文，并在发现问题后及时更新

如果你愿意，不妨在致谢部分留下**本论文使用基于LaTeX的本科生毕业设计模板书写**，如果你愿意附上本GitHub的链接，那是再好不过了

希望能有北邮的开源组织来维护和模块化本科生毕设LaTeX模板

（当然更希望北邮的教务部门**锐意进取、大胆创新、敢为人先**地提供**官方**的毕设LaTeX模板）
