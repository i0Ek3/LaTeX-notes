# 如何使用LaTeX

> 如果你还不知道 LaTeX，请自行了解。

**不断完善中....**


## 目录

- [基本语法](#基本语法)
    - [文档开始](#文档开始)
    - [列表](#列表)
    - [段落](#段落)
    - [目录](#目录)
    - [创建新的一页](#创建新的一页)
    - [脚注](#脚注)
    - [换行](#换行)
    - [包](#包)
    - [表格](#表格)
    - [添加图像](#添加图像)
    - [插入代码](#插入代码)
    - [分割文件](#分割文件)
    - [转义](#转义)
    - [数学公式](#数学公式)
    - [上下标](#上下标)
    - [根号与分式](#根号与分式)
    - [运算符](#运算符)
    - [定界符](#定界符)
    - [省略号](#省略号)
    - [矩阵](#矩阵)
    - [分段函数](#分段函数)
    - [页边距](#页边距)
    - [页眉页脚](#页眉页脚)
    - [首行缩进](#首行缩进)
    - [段间距](#段间距)
    - [行间距](#行间距)



## 基本语法

这里的基本语法几乎都是以 `\begin{}` 开始，以 `\end{}` 结束。示例中的代码可以直接拷贝到 LaTeX 编辑器中运行查看效果。

### 文档开始

用 `\begin{documen}` 和 `\end{document}` 来表示文档的开始和结束。

    \begin{document}

    Hello LaTeX!

    \end{document}

### 列表

- 无序

用 `\begin{itemize}` 和 `\end{itemize}` 来添加无序列表。

    \begin{itemize}
    \item First line.
    \item Second line.
    \end{itemize}

- 有序

用 `\begin{enumerate}` 和 `\end{enumerate}` 来添加有序列表。

    \begin{enumerate}
    \item First line.
    \item Second line.
    \end{enumerate}

### 段落

用 `\section` 表示一个部分，用 `\prograph` 表示一个段落，用 `\subsection` 和 `\subprograph` 表示子部分与子段落。

    \section{}
    One Section

    \paragraph{}
    This is my first time to use LaTeX, I like it so much! This is my first time to use LaTeX, I like it so much!
    This is my first time to use LaTeX, I like it so much! This is my first time to use LaTeX, I like it so much!
    This is my first time to use LaTeX, I like it so much! This is my first time to use LaTeX, I like it so much!

    \subsection{}
    Subsection One

    \subparagraph{}
    This is my first time to use LaTeX, I like it so much!


### 目录

用 `\tableofcontents` 和上述段落中的内容可以很容易的创建一个目录。

    \tableofcontents
    \section{Section 1}
    This is section one
    \subsection{Subsection subtitle}
    This is subsection one


### 创建新的一页

用 `\newpage` 来创建新的一页。

### 脚注

用 `\footnote` + `\label` + `\ref` 来表示脚注。

    This is my first time to use LaTeX\footnote{\label{myfootnote}Hello LaTeX}.
    I am referring to myself \ref{myfootnote}.

### 换行

用 `\newline` 来换行。

### 包

用 `\usepackage` 来导入包。

### 表格

用 `\begin{table}` 和 `\end{table}` 来表示表格环境。

    \begin{table}[h!]
        \centering
        \caption{Cation for the table}.
        \label{tab:table1}
        \begin{tabular}{l|c||r}
            1 & 2 & 3\\
            \hline
            a & b & c\\
        \end{tabular}
    \end{table}

### 添加图像

用 `\usepackage{graphicx}` 和 `\begin{figure}` 和 `\end{figure}` 来添加图像。
    
    \usepackage{graphicx}

    \begin{figure}
        \includegraphics[width=\linewidth]{filename.jpg}
        \caption{What?}
        \label{fig:whateverlabel}
    \end{figure}

### 插入代码

用 `\begin{verbatim}` 和 `\end{verbatim}` 来插入代码。或者使用 `listings` 包来插入代码。

    \begin{verbatim}

    #include <iostream>

    int main()
    {
        std::cout << "Hello LaTeX!" << std::endl;
        return 0;
    }

    \end{verbatim}

### 分割文件

用 `\input{second_file}` 来分割较长的文件内容。

    % original
    This is my first time to use LaTeX. 
    This is my second time to use LaTeX.

    % after split
    This is my first time to use LaTeX. 
    \input{second_file}

### 转义

同编程中的情况类似，LaTeX中对特殊符号也需要用`\`转义。如：

    Such 20\% people.

### 数学公式

在 LaTeX 中，有两种数学模式，`行内模式(inline)`和`行间模式(display)`。

其中，使用 `$ ... $` 可以在行文中插入行内公式，使用 `\[ ... \]` 可以插入行间公式，并用 `equation` 来编号。

    \documentclass{article}
    \usepackage{amsmath}
    \begin{document}
    
    $E=mc^2$.
    \[ E=mc^2. \]

    \begin{equation}
    E=mc^2.
    \end{equation}
    \end{document}

### 上下标

使用`^`和`_`来标注上下标，可参考上面的例子。


### 根号与分式

根式用 `\sqrt{·}` 来表示，分式用 `\frac{·}{·}` 来表示（第一个参数为分子，第二个为分母）。

    \documentclass{article}
    \usepackage{amsmath}
    \begin{document}

    %行内
    $\sqrt{x}$, $\frac{1}{2}$.

    %行间
    \[ \sqrt{x}, \]
    \[ \frac{1}{2}. \]
    
    \end{document}

### 运算符

    \documentclass{article}
    \usepackage{amsmath}
    \begin{document}
    
    %基本运算符号
    \[ \pm\; \times \; \div\; \cdot\; \cap\; \cup\;
    \geq\; \leq\; \neq\; \approx \; \equiv \]
    
    %极限
    $ \sum_{i=1}^n i\quad \prod_{i=1}^n $
    $ \sum\limits _{i=1}^n i\quad \prod\limits _{i=1}^n $
    \[ \lim_{x\to0}x^2 \quad \int_a^b x^2 dx \]
    \[ \lim\nolimits _{x\to0}x^2\quad \int\nolimits_a^b x^2 dx \]
    
    %积分符号
    \[ \iint\quad \iiint\quad \iiiint\quad \idotsint \]
    
    
    \end{document}



### 定界符

就是各种括号。

    \documentclass{article}
    \usepackage{amsmath}
    \begin{document}
    
    \[ \Biggl(\biggl(\Bigl(\bigl((x)\bigr)\Bigr)\biggr)\Biggr) \]
    \[ \Biggl[\biggl[\Bigl[\bigl[[x]\bigr]\Bigr]\biggr]\Biggr] \]
    \[ \Biggl \{\biggl \{\Bigl \{\bigl \{\{x\}\bigr \}\Bigr \}\biggr \}\Biggr\} \]
    \[ \Biggl\langle\biggl\langle\Bigl\langle\bigl\langle\langle x
    \rangle\bigr\rangle\Bigr\rangle\biggr\rangle\Biggr\rangle \]
    \[ \Biggl\lvert\biggl\lvert\Bigl\lvert\bigl\lvert\lvert x
    \rvert\bigr\rvert\Bigr\rvert\biggr\rvert\Biggr\rvert \]
    \[ \Biggl\lVert\biggl\lVert\Bigl\lVert\bigl\lVert\lVert x
    \rVert\bigr\rVert\Bigr\rVert\biggr\rVert\Biggr\rVert \]
    
    \end{document}


### 省略号

    \documentclass{article}
    \usepackage{amsmath}
    \begin{document}
    
    \[ x_1,x_2,\dots ,x_n\quad 1,2,\cdots ,n\quad
    \vdots\quad \ddots \]
    
    \end{document}·


### 矩阵

    \documentclass{article}
    \usepackage{amsmath}
    \begin{document}
    
    \[ \begin{pmatrix} a&b\\c&d \end{pmatrix} \quad
    \begin{bmatrix} a&b\\c&d \end{bmatrix} \quad
    \begin{Bmatrix} a&b\\c&d \end{Bmatrix} \quad
    \begin{vmatrix} a&b\\c&d \end{vmatrix} \quad
    \begin{Vmatrix} a&b\\c&d \end{Vmatrix} \]
    
    \end{document}

### 分段函数

分段函数可以用cases次环境来实现。

    \documentclass{article}
    \usepackage{amsmath}
    \begin{document}
        
    \[ y= \begin{cases}
    -x,\quad x\leq 0 \\
    x,\quad x>0
    \end{cases} \]
        
    \end{document}
        
### 页边距

可以根据需要进行更该相应的数值。

    \usepackage{geometry}
    \geometry{papersize={20cm,15cm}}
    \geometry{left=1cm,right=2cm,top=3cm,bottom=4cm}


### 页眉页脚

    \documentclass{article}

    \usepackage{fancyhdr}
    \pagestyle{fancy}
    \lhead{\author}
    \chead{\date}
    \rhead{152xxxxxxxx}
    \lfoot{}
    \cfoot{\thepage}
    \rfoot{}
    \renewcommand{\headrulewidth}{0.4pt}
    \renewcommand{\headwidth}{\textwidth}
    \renewcommand{\footrulewidth}{0pt}
    
    \begin{document}   
    \end{document}


### 首行缩进

`\ccwd` 是当前字号下一个中文汉字的宽度。

    \setlength{\parindent}{\ccwd}

### 段间距

    \usepackage{setspace}
    \onehalfspacing %1.5倍

### 行间距

    \addtolength{\parskip}{.4em}















