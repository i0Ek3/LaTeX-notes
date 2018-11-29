# 如何使用LaTex

> 如果你还不知道LaTex，请自行了解。

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
    - []()
    - []()
    - []()
    - []()
    - []()



## 基本语法

这里的基本语法几乎都是以`\begin{}`开始，以`\end{}`结束。示例中的代码可以直接拷贝到LaTex编辑器中运行查看效果。

### 文档开始

用`\begin{documen}`和`\end{document}`来表示文档的开始和结束。

    \begin{document}

    Hello LaTex!

    \end{document}

### 列表

- 无序

用`\begin{itemize}`和`\end{itemize}`来添加无序列表。

    \begin{itemize}
    \item First line.
    \item Second line.
    \end{itemize}

- 有序

用`\begin{enumerate}`和`\end{enumerate}`来添加有序列表。

    \begin{enumerate}
    \item First line.
    \item Second line.
    \end{enumerate}

### 段落

用`\section`表示一个部分，用`\prograph`表示一个段落，用`\subsection`和`\subprograph`表示子部分与子段落。

    \section{}
    One Section

    \paragraph{}
    This is my first time to use LaTex, I like it so much! This is my first time to use LaTex, I like it so much!
    This is my first time to use LaTex, I like it so much! This is my first time to use LaTex, I like it so much!
    This is my first time to use LaTex, I like it so much! This is my first time to use LaTex, I like it so much!

    \subsection{}
    Subsection One

    \subparagraph{}
    This is my first time to use LaTex, I like it so much!


### 目录

用`\tableofcontents`和上述段落中的内容可以很容易的创建一个目录。

    \tableofcontents
    \section{Section 1}
    This is section one
    \subsection{Subsection subtitle}
    This is subsection one


### 创建新的一页

用`\newpage`来创建新的一页。

### 脚注

用`\footnote` + `\label` + `\ref`来表示脚注。

    This is my first time to use LaTex\footnote{\label{myfootnote}Hello LaTex}.
    I am referring to myself \ref{myfootnote}.

### 换行

用`\newline`来换行。

### 包

用`\usepackage`来导入包。

### 表格

用`\begin{table}`和`\end{table}`来表示表格环境。

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

用`\usepackage{graphicx}`和`\begin{figure}`和`\end{figure}`来添加图像。
    
    \usepackage{graphicx}

    \begin{figure}
        \includegraphics[width=\linewidth]{filename.jpg}
        \caption{What?}
        \label{fig:whateverlabel}
    \end{figure}

### 插入代码

用`\begin{verbatim}`和`\end{verbatim}`来插入代码。或者使用`listings`包来插入代码。

    \begin{verbatim}

    #include <iostream>

    int main()
    {
        std::cout << "Hello LaTex!" << std::endl;
        return 0;
    }

    \end{verbatim}

### 分割文件

用`\input{second_file}`来分割较长的文件内容。

    % original
    This is my first time to use LaTex. 
    This is my second time to use LaTex.

    % after split
    This is my first time to use LaTex. 
    \input{second_file}




