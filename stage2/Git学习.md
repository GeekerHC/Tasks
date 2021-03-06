# Git学习

[TOC]

## Git简介及基本语法

Git是由Linus为Linux社区创建的分布式版本控制系统。因其优秀的分布式结构和免费为许多程序员们使用。其历史老生常谈，在此不再赘述。  

在学习具体的知识前，我们可以对Git的结构进行简单的了解，以便于解决许多在操作中令人迷惑的点（如添加文件需要2步：git add与git commit）。

![Git结构]（https://img-blog.csdn.net/20130519213551181）

Git中有许多特别的语法，在学习过程中有许多令人迷惑的代码，同时许多教程里并没有进行介绍，下面是一些学习过程中必要的语法和命令（按学习过程排序），其中，（括号及其里面的内容）这个整体需要被编辑者替换成所需内容。

> **mkdir (repository) ** *创建仓库*（允许套娃但不建议）

>**cd （repository）** *跳转*

> **pwd** *查看当前目录*  

> **git status** *监控仓库内状态

> **git init** *把这个目录变成Git可以管理的仓库（如果没有看到.git文件夹，可用ls-sh可以看见）*  

> **git add (文件名.文件格式)** *把文件添加到仓库暂存区中*

> **git commit -m"（备注）"** *把仓库暂存区的所有修改提交到分支*

> **git remote add origin (SSH密钥)** *把本地仓库提交到Github的现有远端（origin）仓库上*

> **git remote remove origin** *把远程仓库删除*

> **git push -u origin (分支)** *把本地仓库的内容推送到远程*

.0

## Git的使用

### 创建仓库

1. mkdir (仓库名1)  *创建仓库*

2. cd （仓库名1）  *跳转到仓库1中* 

3. （略）pwd *显示当前目录*

4. git init *把这个目录变成Git可以管理的仓库*

5. git add (文件名.文件格式)  *把文件1”文件名“放入该仓库暂存区中*

   git add . *把所有的文件都放入该仓库暂存区中*

6. git commit -m"（备注）" *把文件1从仓库暂存区存到分支中*



### 上传到Github

1. git remote add origin (SSH密钥) *把本地仓库1提交到Github的现有远端（origin）仓库上*

2. git push -u origin (分支名) *把本地仓库的内容推送到远程仓库上*

## 其他

### 暂存区的存在

在解释上传文件到Git本地管理时需要先“add”后“commit”这一问题之前，我们可以先对Git的结构进行了解。Git在本地数据管理时，可以大致分为2个区：

- 工作区（Working Directory）*可能不在Git的层次内*

  是我们直接操作的地方，肉眼可见，他的存在与Git无关。

- 暂存区（Stage）

  数据、文件暂时存放的地方，可以使工作区和版本库进行有效沟通。

- 版本库（Commit History）

  存放已经提交的文件，可以从其中push到Github的远程仓库中。

看似多余的一步，实际上暂存区（Stage）可以给Git一个大放异彩的Stage。我参考前人的经验，发现Stage对下列问题的解决有独特的解决方法：

- 修改了4个文件，在不放弃任何修改的情况下，其中一个文件不想提交，如何操作？（没add : git add 已经add: git reset --soft ）
- -修改到一半的文件，突然间不需要或者放弃修改了，怎么恢复未修改前文件？ (git checkout)
- 代码写一半，被打断去做其他功能开发，未完成代码保存？(git stash)
- 代码写一半，发现忘记切换分支了？(git stash & git checkout)
- 代码需要回滚了？（git reset）
- 等等
  ————————————————
  版权声明：本文为CSDN博主「DRPrincess」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
  原文链接：https://blog.csdn.net/qq_32452623/article/details/78417609

### 版本回退

我们都知道Git是**版本控制**系统，了解了Git的命名和结构，我们就不难理解版本回退了。版本回退是有关版本库的。“git commit”多次后我们可以使用版本回退来读取前几次上传的文件，这样可以提高我们工作时的容错率。

## 总结

学习Git的过程就是学习一个有序系统的过程，如何在非图形界面进行操作实属首次，那么第一件事就是大致了解该系统的层级，了解如何进行简单操作，尝试去做。在尝试的时候可能会出现许许多多的问题，但是我们可以在懂得之后进行复原工作（甚至可以重开，因为我就是这么做的）。你要走的路必然是前人走过的，如何快速地吸收经验并且利用起来才是学习的过程。许多渠道都可以进行学习，CSDN、同学们、学长都可以进行求教。因此，世上无难事，只要肯攀登。在短短的几天内，我们可能无法非常熟练地掌握Git，但是我们可以收获解决从未涉及的非图形界面的操作、自学能力以及对Git的大致认识，在不久的以后操作的时候可以回忆起Git有哪些功能，并且也可以非常沉着地应对报错等问题。同时Github也是一个Git的配套网站，远端的存在对分布式版本控制系统的重要性不言而喻。据我了解，国外许多大学的计算机系学生都在使用Github提交作业，在学习过程而不是等到工作时接触Github本身就是一种非常有意思的事情，因此我们也不得不承认国内外教学的差距，那么使我们打开格局的方法就是多接触新事物和新方法，只有这样才能成为一名优秀的Geeker。



## 报错的问题

- error：remote origin already exists

  **解决办法：**

  - **情况一**，你很清楚你的origin库是正确的，那么改用“git push”

  - **情况二**，你不清楚你的origin库是否正确，那么就使用“git remote remove origin”删除该库，然后再“给git remote add origin”添加该库。我们可以发现add和remove这两条语句十分对称，因此我们可以合理推断“git remote （） origin”语句可以实现对远端仓库的控制。



- ！[rejected]

  error:failed to push some refs to'github.com:xxxx/xxxx.git'

  **问题说明：**

  *因为对git操作过于没有条理，导致我反复删除了本地库和远端库，这使得许多本可避免的问题大量出现，这是其中之一。解决方案可能与版本库冲突有关。*

  **尝试：**

  - **第一步**（来源：CSDN），既然push存在问题，那么我们pull一下再push（CSDN上对版本冲突的普遍答案），然而问题并未解决，同时出现‘fatal:refusing to merge unrelated histories’(严重：拒绝合并不相关的历史)；当尝试再次上传时，仍然出现原来报错的情况。然后git给了我许多hint（线索），但收效甚微。

  - **第二步**，我使用‘git remote -v’检查是否和远程库绑定。git显示：‘origin  git@xxxxxx/xxxx (fetch)
    origin  git@xxxxxx/xxxx.git (push）’说明我确实绑定了远端库,我再使用‘git remote add origin git@xxxxxx/xxxx.git’，它显示‘error:remote origin already exists.’,这说明远端库也确实存在，所以如何处理这个问题呢？
  - **第三步**（来源：顾越），使用强制推送指令：‘git push --force origin (分支名)’，结果非常快速地解决了问题。但当我审视我的Github时，我发现我的各类文件夹最后保存的日期为‘2 days ago’（11月13日）而不是今天（11月15日）。与刚创建的README.md的‘2 minutes ago’相比，着实有点蹊跷。

