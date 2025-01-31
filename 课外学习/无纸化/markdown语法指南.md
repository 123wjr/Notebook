# 标题
># 123
>## 123
>### 123

# 段落
段落和段落之间要隔一行.

就像这样.
分割线
三条横线 (或更多的横线) 表示分割线.

---

就像这样.





# 加粗, 斜体和删除线
做笔记的时候, 我们常常会有这样的要求, "加粗, 斜体和删除线", 作为笔记的

>**重点加粗**
>
>*斜体*
>
>~~删除线~~
>Markdown Preview Enhanced 拓展功能:
>
>==高亮==

# 快捷键:

选中文本之后, 按下 Ctrl + B 可以给选中文本加粗.

同理 Ctrl + I 可以让选中文本变为斜体.

# 列表
列表是记笔记时非常基本的元素, 在 Markdown 中, 可以用很方便的格式书写列表:

>* 无序列表
>  * 嵌套无序列表
>  * 嵌套无序列表
>* 无序列表
>* 无序列表
>
>1. 有序列表 1
>   1. 嵌套有序列表 1
>   2. 嵌套有序列表 2
>2. 有序列表 2
>3. 有序列表 3

Markdown Preview Enhanced 拓展功能:

任务列表:

- [x] 已经完成的事 1
- [x] 已经完成的事 2
- [x] 已经完成的事 3
- [ ] 仍未完成的事 4
- [ ] 仍未完成的事 5

# 快捷键:

要进行缩进 (书写嵌套列表), 你可以使用 VS Code 的快捷键 Ctrl + [ 和 Ctrl + ].

这个快捷键可以将代码向左或向右进行缩进!

# 引用和代码
引用文本:

> 引用别人说的话
> 就这样写
> By. OrangeX4

这是 `行内代码` 语法.

代码块语法:

`````` python
print("Hello, World!")
``````

Markdown Preview Enhanced 拓展功能:

代码行数的显示:

`````` javascript {.line-numbers}
function add(x, y) {
  return x + y
}
``````

# 超链接和图片

你可以用下面的语法插入超链接和图片:

[超链接名称](链接地址)

![图片提示语](图片地址)

例如, 可以使用网址和图床:

[OrangeX4's Blog](https://orangex4.cool/)

![OrangeX's Avatar](https://orangex4.cool/images/icons/profile.jpg)

也可以在本地用相对地址:

[Other](other.md)

![OrangeX's Avatar](images/profile.jpg)

# 剪贴板图片插入
看了上面的插入图片语法, 也许你会觉得, 好麻烦啊.

我就插入一张图片, 居然还要把图片上传到网上. 或者把图片保存到本地, 还要移动图片, 命名什么的.

就不能像 Word 那样, 直接剪贴板粘贴图片吗?

万能的 VS Code 当然可以做到类似的事!

其实, 使用你已经安装了的 Paste Image 插件就行.

不过在使用之前, 你要做一点小调整:

按下 Ctrl + , 打开设置窗口, 输入 Paste Image Path 并搜索, 将框内的文本改成 ${currentFileDir}/images.

注意标题是 Paste Image: Path, 不要弄错了!

设置好之后, 你就可以使用剪贴板粘贴功能了!

按下快捷键 Ctrl + Alt + V,

就能把图片自动保存到当前目录下, 并以正确的格式粘贴到当前的 Markdown 文件中.

# 表格
你可以很方便地在做笔记的时候加入表格:

>表格:
>
>| 表头 | 表头 |
>| ---- | ---- |
>| 内容 | 内容 |
>| 内容 | 内容 |

Markdown Preview Enhanced 拓展功能:

>拓展语法:
>
>| 表头 | 表头 |
>| ---- | ---- |
>| 内容 | 内容 |
>| >    | 内容 |
>
>| 表头 | 表头 |
>| ---- | ---- |
>| 内容 | 内容 |
>| ^    | 内容 |

## 快捷键:

自动表格对齐: Shift + Alt + F

# 注释
注释不会被渲染出来.

你可以随手做点草稿, 如果还想保留着, 但是不显示, 就可以按下快捷键 Ctrl + \ 将当前行注释 / 反注释.

注释:

<!-- 你看不见我 -->

<!-- 多行注释
就像这样 -->
有一点很重要的就是, VS Code 会在你每次修改代码之后, 重新渲染一遍.

如果有很多很多的数学公式, 渲染会很慢, 这时候有两个建议:

分成多个文件, 避免单文件过大!
将你暂时不看的部分注释掉, 加快渲染速度!

# 数学公式支持
Markdown 的数学公式吸纳了大部分的 Latex 语法, 你可以以一种简单的方式在 VS Code 中书写数学公式.

>行内公式: 
>
>单位圆 $x^2+y^2=1$
>
>公式块:
>
>$$
>\begin{cases}
>x=\rho\cos\theta \\
>y=\rho\sin\theta \\
>\end{cases}
>$$

VS Code 有着非常便捷好用的自动补全功能, 只需要简单地打出你想打的内容的几个字母 (乱序也行), 再使用 ↑ ↓ 进行选择, 最后按下回车就可以打出你想要的内容.

再使用 HyperSnips 插件, 就能够写得飞快.

还有, 不要在公式内使用中文, 除非是 \text{中文} (但是也不推荐)

1. 上标和下标
        上标 $x^2 + y^{12} = 1$
        上标 $x_1 + y_{12} = 1$
        xsr  =>  x^{2}
        xtp  =>  x^{...}
        x1  =>  x_1
        xii  =>  x_i
        xsb  =>  x_{...}
2. 分式
    较小的行内行分数 $\frac{1}{2}$
    展示型的分式 $\displaystyle\frac{x+1}{x-1}$
    其中 \displaystyle 用于将行内展示转为块状展示.

    HyperSnips 自动扩展：
        1/  =>  \frac{1}{...}
        (1 + 2)/  =>  \frac{(1+2)}{...}
        //  =>  \frac{...}{...}
3. 根式
    开平方 $\sqrt{2}$

    开 $n$ 次方 $\sqrt[n]{2}$

    HyperSnips 自动扩展：

        hsq  =>  \sqrt{...}
4. 空格
    数学公式中的 空格和换行 都会在编译时 被忽略，想要实现「空格」的效果，需要用特别的命令。
        紧贴 $a\!b$
        没有空格 $ab$
        小空格 $a\,b$
        中等空格 $a\;b$
        大空格 $a\ b$
        quad 空格 $a\quad b$
        两个 quad 空格 $a\qquad b$
5. 累加, 累乘和积分
    累加 $\sum_{k=1}^n\frac{1}{k}  \quad  \displaystyle\sum_{k=1}^n\frac{1}{k}$

    累乘 $\prod_{k=1}^n\frac{1}{k}  \quad  \displaystyle\prod_{k=1}^n\frac{1}{k}$

    积分 $\displaystyle \int_0^1x{\rm d}x  \quad  \iint_{D_{xy}}  \quad  \iiint_{\Omega_{xyz}}$

    HyperSnips 自动扩展：

        sum  =>  \sum_{...}
        prod  =>  \prod_{<n=1>}^{<\infty>} ...
        int  =>  \int
        dint  =>  \int_{<-\infty>}^{<\infty>} ... \mathrm{d}x
    Tips：按下 Tab 键可以跳转光标。
6. 括号修饰
    用 \left 和 \right 可以让括号适配内部大小

    圆括号 $\displaystyle \left(\sum_{k=1}^{n}\frac{1}{k} \right)^2$

    方括号 $\displaystyle \left[\sum_{k=1}^{n}\frac{1}{k} \right]^2$

    花括号 $\displaystyle \left\{\sum_{k=1}^{n}\frac{1}{k} \right\}^2$

    尖括号 $\displaystyle \left\langle\sum_{k=1}^{n}\frac{1}{k} \right\rangle^2$

    HyperSnips 自动扩展：

        @(  =>  \left( ... \right)
        @[  =>  \left[ ... \right]
        @{  =>  \left\{ ... \right\}
        @<  =>  \left< ... \right>
        set  =>  \{ ... \}
7. 多行算式对齐
    居中:

    $$
    \begin{aligned}
    y &=(x+5)^2-(x+1)^2 \\
    &=(x^2+10x+25)-(x^2+2x+1) \\
    &=8x+24 \\
    \end{aligned}
    $$

    左对齐:

    $
    \begin{aligned}
    y &=(x+5)^2-(x+1)^2 \\
    &=(x^2+10x+25)-(x^2+2x+1) \\
    &=8x+24 \\
    \end{aligned}
    $

    HyperSnips 自动扩展：

        ali  =>
        \begin{aligned}
        ... \\
        \end{aligned}
    如果你安装了 Better Markdown & Latex Shortcuts 插件，你还可以按下 Shift + Ctrl + Alt + C 可以将行公式转为 aligned 环境。
8. 方程组
    $$
    \begin{cases}
    k_{11}x_1+k_{12}x_2+\cdots+k_{1n}x_n=b_1 \\
    k_{21}x_1+k_{22}x_2+\cdots+k_{2n}x_n=b_2 \\
    \cdots \\
    k_{n1}x_1+k_{n2}x_2+\cdots+k_{nn}x_n=b_n \\
    \end{cases}
    $$

    HyperSnips 自动扩展：

        case  =>
        \begin{cases}
        ... \\
        \end{cases}
9. 矩阵
矩阵:

    $$
    \begin{pmatrix}
    1 & 1 & \cdots & 1 \\
    1 & 1 & \cdots & 1 \\
    \vdots & \vdots & \ddots & \vdots \\
    1 & 1 & \cdots & 1 \\
    \end{pmatrix}

    \quad

    \begin{bmatrix}
    1 & 1 & \cdots & 1 \\
    1 & 1 & \cdots & 1 \\
    \vdots & \vdots & \ddots & \vdots \\
    1 & 1 & \cdots & 1 \\
    \end{bmatrix}
    $$ 

    行列式: 

    $$
    \begin{vmatrix}
    1 & 1 & \cdots & 1 \\
    1 & 1 & \cdots & 1 \\
    \vdots & \vdots & \ddots & \vdots \\
    1 & 1 & \cdots & 1 \\
    \end{vmatrix}
    $$

    HyperSnips 自动扩展：

        bmat2  =>  \begin{bmatrix} ... & ... \\ ... & ... \\\end{bmatrix}

        vec2  =>  \begin{pmatrix} ... \\ ... \\\end{pmatrix}
        tips：按下 Tab 键可以切换到下一个位置。
10. 特殊符号
    ![](${currentFileDir}/images/20230726132700.png)
    更多特殊符号可以 上网查询

    可以搜索 "Latex 符号表"

    HyperSnips 自动扩展：

        alpha  =>  \alpha
        Sigma  =>  \Sigma
11. 公式编号与引用
        $$
        x+2 \tag{1.2}
        $$

        $$
        \begin{equation}
        x^n+y^n=z^n
        \end{equation}
        $$

        由公式 $(1.2)$ 可得到结论
12. 零碎的重要语法
        点乘 $\cdot$, 叉乘 $\times$, 异或 $\otimes$, 直和 $\oplus$, 加减 $\pm$, 复合 $\circ$.
        小于等于 $\leq$, 大于等于 $\geq$, 不等 $\neq$, 恒等 $\equiv$, 约等 $\approx$, 等价 $\cong$, 相似 $\sim$, 相似等于 $\simeq$, 点等 $\doteq$.
        逻辑与 $\land$, 逻辑或 $\lor$, 逻辑非 $\lnot$, 蕴涵 $\to$, 等价 $\leftrightarrow$.
        因为 $\because$, 所以 $\therefore$, 存在 $\exist$, 任意 $\forall$.
        左小箭头 $\leftarrow$, 右小箭头 $\rightarrow$, 左大箭头 $\Leftarrow$, 右大箭头 $\Rightarrow$, 右长箭头 $\xrightarrow[fgh]{abcde}$.
        属于 $\in$, 包含于 $\subset$, 真包含于 $\subseteq$, 交 $\cap$, 并 $\cup$, 空集 $\empty$
        短向量 $\vec{x}$, 长向量 $\overrightarrow{AB}$, 上横线 $\overline{p}$.
        无限 $\infty$, 极限 $\lim$, 微分 ${\rm d}$, 偏导 $\partial$, 点求导 $\dot{y}$, 点二阶导 $\ddot{y}$, 变化量 $\Delta$, 梯度 $\nabla$.
        横省略 $\cdots$, 竖省略 $\vdots$, 斜省略 $\ddots$.
        常见函数 $\sin$, $\cos$, $\tan$, $\arcsin$, $\arccos$, $\arctan$, $\ln$, $\log$, $\exp$.
    
    HyperSnips 自动扩展：
    
        **  =>  \cdot
        xx  =>  \times
        otimes  =>  \otimes
        <=  =>  \le
        !=  =>  \neq
        ==  =>  \equiv
        ~~  =>  \thickapprox
        sim  =>  \sim
        land  =>  \land
        lor  =>  \lor
        bec  =>  \because
        thr  =>  \therefore
        EE  =>  \exists
        AA  =>  \forall
        inn  =>  \in
        sse  =>  \subseteq
        sqs  =>  \sqsubseteq
        cap  =>  \cap
        cup  =>  \cup
        empty  =>  \empty
        oo  =>  \infty
        lim  =>  \lim_{<n> \to <\infty>}
        dd  =>  \mathrm{d}
        part  =>  \frac{\partial <V>}{\partial <x>}
        Delta  =>  \Delta
        nabla  =>  \nabla
        ...  =>  \cdots
        sin  =>  \sin
        RR  =>  \mathbb{R}
        NN  =>   \mathbb{N}
        txt  =>  \text{...}
        xbar  =>  \bar{x}
        xhat  =>  \hat{x}
        xhvec  =>  \vec{x}
        xhdot  =>  \dot{x}
        Xbb  =>  \mathbb{X}
        Xbs  =>  \boldsymbol{X}
        Xbm  =>  \bm{X}
        Xbf  =>  \mathbf{X}
        Xsf  =>  \mathsf{X}
        Xcal  =>  \mathcal{X}
        Xfrak  =>  \mathfrak{X}
        Xrm  =>  \mathrm{X}
13. 输出为 PDF
我们在右侧预览栏邮件菜单, 选择 在浏览器中打开右键选择，打印，就能够输出为 PDF 了.
14. 类似 UltiSnips 的自动补全
    插件安装: HyperSnips for Math - Visual Studio Marketplace

    安装完成后, 按下快捷键 Ctrl + Shift + P, 输入命令 Open Snippets Directory, 就可以打开一个文件夹. 在该文件夹新建一个文件 markdown.hsnips, 并将 这个网址 里面的内容输入进去, 保存, 就可以使用了.

    例如, 你可以在数学环境中输入: (1+2)/, 它会自动变为 \frac{1+2}{}.

    你也可以创建自己的 Snippets, 按照格式, 发挥想象来写就好!

    先看个 普通例子:

        snippet RR "R" iAm
        \mathbb{R}
        endsnippet
    这是一个在数学环境中自动展开的 Snippet, 它有三个标示符 iAm, 分别代表 "在词语内部也会触发", "自动展开" 和 "数学环境".

    这个例子会在数学环境内, 自动将 RR 展开成为 \mathbb{R}, 代表 "实数".

    再看个 正则表达式 的例子:

        snippet `((\d+)|(\d*)(\\)?([A-Za-z]+)((\^|_)(\{\d+\}|\d))*)/` "Fraction no ()" Am
        \frac{``rv = m[1]``}{$1}$0
        endsnippet
    其中 rv = m[1] 是 JavaScript 代码, 表示将正则表达式的第一个组 m[1] 输出给 "返回值" rv, 然后输出出去.

    这是一个在数学环境中自动展开的 Snippet, 它有两个标示符 'Am', 分别代表 '自动展开' 和 '数学环境'. 用处是:

        1/    --->    \frac{1}{}
    相比于原来的 HyperSnips, 最大特点是, 它只会在数学环境 $...$, $$...$$, \(...\) 和 \[...\] 中自动展开!

    还有 ${VISUAL} 语法:

        snippet fr "frac" iAm
        \\frac{${1:${VISUAL}}}{$2}
        endsnippet
    这个语法会保存最近选中的内容, 然后替换掉 ${VISUAL} 部分.

    要开启在 markdown 下的 自动补全提示, 请使用 Shift + Ctrl + P 然后输入 open settings json 打开配置文件, 然后加入以下部分:

        "[markdown]": {
            "editor.quickSuggestions": true
        },
15. VS Code 快捷键
    快捷键是用 VS Code 记笔记的精髓之一, 每一个都非常重要!

    请务必认真记住这些快捷键!!!

    1. 原生快捷键
       1. 通用操作
        Ctrl + C, 复制当前文本
        Ctrl + V, 粘贴当前文本
        Ctrl + Z, 撤销
        Ctrl + Shift + Z, 反撤销
        Shift + Alt + F, 整理代码
        Ctrl + /, 将当前行注释 / 反注释, 当多行文本被选中时, 将多行文本注释
       2. 光标操作
        Ctrl + ← 将光标向左移动一个单词
        Ctrl + → 将光标向右移动一个单词
        Ctrl + Alt + ↑, 向上加入一个光标
        Ctrl + Alt + ↓, 向下加入一个光标
        Ctrl + Alt + U, 撤销上次光标操作
       3. 界面移动
        Ctrl + ↑ 向上移动当前界面
        Ctrl + → 向下移动当前界面
       4. 选中操作
        Shift + ← 向左选中 / 反选中一个字符(重要)
        Shift + → 向右选中 / 反选中一个字符(重要)
        Ctrl + Shift + ← 向左选中 / 反选中一个单词(重要)
        Ctrl + Shift + → 向右选中 / 反选中一个单词(重要)
        Ctrl + D当前有选中文本时, 将下一个与其相同的文本加入选中 (重要)
       5. 文本行操作
        Ctrl + C当前无选中文本时, 复制当前行
        Shift + Alt + ↑ 向上复制当前行, 当多行文本被选中时, 向上复制多行 (重要)
        Shift + Alt + ↓ 向下复制当前行, 当多行文本被选中时, 向下复制多行 (重要)
        Alt + ↑ 向上移动当前行, 当多行文本被选中时, 将当前多行文本向上移动 (重要)
        Alt + ↓ 向下移动当前行, 当多行文本被选中时, 将当前多行文本向下移动 (重要)

    2. 插件增加的快捷键
       1. Markdown 语法
        Ctrl + B当前有选中文本时, 将文本加粗
        Ctrl + I当前有选中文本时, 将文本变为斜体
        Ctrl + M 进入数学公式模式 (加入美元符)
       2. 图片粘贴
        Ctrl + Alt + V 粘贴剪贴板图片 (本地)
        Ctrl + Alt + V 粘贴剪贴板图片 (图床)
       3. 光标操作
        Ctrl + Alt + U 将多选光标变为单选
       4. 选中操作
        Shift + Alt + ← 向左复制当前选中文本 (重要)
        Shift + Alt + → 向右复制当前选中文本 (重要)
        Alt + ← 向左移动当前选中文本一个字符(重要)
        Alt + → 向右移动当前选中文本一个字符(重要)
        Ctrl + Alt + ← 向左移动当前选中文本一个单词(重要)
        Ctrl + Alt + → 向右移动当前选中文本一个单词(重要)
       5. 计算器功能
        Ctrl + Shift + Alt + E 计算当前选中表达式, 用等号连接并输出
        Ctrl + Shift + Alt + R 计算当前选中表达式, 并替换当前选中表达式
        Ctrl + Shift + Alt + D 定义当前选中表达式, 无输出

    3. 科学计算
        使用我开发的一个插件 Latex Markdown Calculator , 可以很方便地在 VS Code 中用 Latex 公式语法进行科学计算。
        即选中一段数学表达式, 按下一个快捷键就能帮你计算出结果, 一些简单的计算再也不用打开电脑自带的计算器和 Matlab~
        因为是基于 Python Sympy 的, 所以现在它已经有很多强大的功能了。
        比如说：符号运算, 求积分, 求微分, 基于矩阵的符号运算(如行列式, 点乘, 转置, 求逆等功能), 解方程...
        快捷键为 Shift + Ctrl + Alt + E, 详细内容请查看插件的说明文档.

# 云端存储
## 安装 Git
    你可以前往 官网 下载 Git, 有 Windows 版本, 也有 Mac 版本和 Linux 版本.

    如果你网速不佳, 也可以去 腾讯软件中心 下载.

    安装过程中, 基本上一直点 Next 就好.

    安装好了之后, 按下 Win 键, 输入 cmd, 回车, 便出现了命令行.

    输入

        git
    命令, 回车, 若输出如图显示, Git 就安装成功了.
## 版本控制
    我们使用 Git 来实现版本控制, 或者是笔记保存效果.

    每次你更改了笔记, 在传到云端之前, 都要进行一次笔记保存 Commit.
## 上传到 GitHub
GitHub 是世界上最大的代码托管平台, 你当然也可以把你的笔记托管在 GitHub 上.

你可以看我的这篇 GitHub 简易指南, 加深对 GitHub 的理解.

要上 GitHub, 你可能需要一点小技巧, 这我就不教你了.

不然你也可以选择国内的 Gitee 或者国内能访问的 GitLab.

看完这篇指南之后, 你大概就知道怎么把笔记托管到云端了, 而且, 完全免费噢.

(虽然可能麻烦了点)
## 上传云端
如果你设置好了 GitHub, 需要上传到云端了, 你可以 Git Push 上去.
## 在线浏览
如果你把你的笔记上传到了云端, 你就可以随时随地地查看你的笔记, 并且可以很方便地分享给别人.

比如, 你要看我的笔记, 可以访问这个链接:

https://notes.orangex4.cool/?git=gitlab

如果你把你的笔记上传到了 GitHub, 想要查看, 你可以用这个网址:

https://notes.orangex4.cool/

并且仿照这个格式:

https://notes.orangex4.cool/?git=github&github=typoverflow/note

大概格式是:

https://notes.orangex4.cool/?git=github&github=用户名/笔记仓库

你就有了这种效果的笔记!