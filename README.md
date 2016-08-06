《Effective Go》中英双语版
===

`Effective Go` 作为 `GO` 语言的入门必读教程，值得每位初学者好好阅读一遍，编辑成书，方便阅读交流。

> 改版说明：2016.8.6

> 李笑来说过[一句话](http://xiaolai.li/2016/06/12/makecs-preface/)： 在中国，对绝大多数人来说，`English + Computer Skills = Freedom` 我非常的赞同。能在学习好一门编程语言（`Go`）的同时，还能加强英语学习，何乐而不为呢。所以我决定将本书改版成中英双语版，方便更多的人来学习。

> 特别感谢 [Golang](https://golang.org) 官网提供的英文版教程。感谢 [hellogcc](http://www.hellogcc.org) 提供的 [中文翻译版一](http://www.hellogcc.org/effective_go.html)，这是我之前制作中文版电子书所参考的资料，翻译的很用心。这里要更感谢 [Go 语言中文社区](https://go-zh.org/) 提供的 [中文翻译版二](https://go-zh.org/doc/effective_go.htm)，翻译的更贴切自然，故此双语版决定选择该版本。

### 参考

*参考官方英文版：[Effective Go 英文版](https://golang.org/doc/effective_go.html)*

~~*参考中文翻译版一：[Effective Go 中文版](http://www.hellogcc.org/effective_go.html)*~~

*参考中文翻译版二：[Effective Go 中文版](https://go-zh.org/doc/effective_go.htm)*

### Fork and Read

> **[Fork me on GitHub](https://github.com/bingoHuang/effective-go-zh-en)**

> **[Read me on Gitbook](https://www.gitbook.com/book/bingohuang/effective-go-zh-en/details)**

## 当前完成章节（持续更新）：

### 已完成：
0. [前言](README.md)
* [引言](01_Overview.md)
* [格式化](02_Formatting.md)

### 未完成：
* [注释](03_Commentary.md)
* [命名](04_Names.md)
* [分号](05_Semicolons.md)
* [控制结构](06_Control_structures.md)
* [函数](07_Functions.md)
* [数据](08_Data.md)
* [初始化](09_Initialization.md)
* [方法](10_Methods.md)
* [接口和其他类型](11_Interfaces_and_other_types.md)
* [空白标识符](12_The_blank_identifier.md)
* [内嵌](13_Embedding.md)
* [并发](14_Concurrency.md)
* [错误](15_Errors.md)
* [一个Web服务器](16_A_web_server.md)

## *Effective Go* - 《实效 GO 编程》

### Introduction

Go is a new language. Although it borrows ideas from existing languages, it has unusual properties that make effective Go programs different in character from programs written in its relatives. A straightforward translation of a C++ or Java program into Go is unlikely to produce a satisfactory result—Java programs are written in Java, not Go. On the other hand, thinking about the problem from a Go perspective could produce a successful but quite different program. In other words, to write Go well, it's important to understand its properties and idioms. It's also important to know the established conventions for programming in Go, such as naming, formatting, program construction, and so on, so that programs you write will be easy for other Go programmers to understand.

This document gives tips for writing clear, idiomatic Go code. It augments the [language specification](https://go-zh.org/ref/spec), [the Tour of Go](https://tour.golang.org/), and [How to Write Go Code](https://go-zh.org/doc/code.html), all of which you should read first.


### 引言

Go 是一门全新的语言。尽管它从既有的语言中借鉴了许多理念，但其与众不同的特性， 使得使用Go编程在本质上就不同于其它语言。将现有的C++或Java程序直译为Go 程序并不能令人满意——毕竟Java程序是用Java编写的，而不是Go。 另一方面，若从Go的角度去分析问题，你就能编写出同样可行但大不相同的程序。 换句话说，要想将Go程序写得好，就必须理解其特性和风格。了解命名、格式化、 程序结构等既定规则也同样重要，这样你编写的程序才能更容易被其他程序员所理解。

本文档就如何编写清晰、地道的Go代码提供了一些技巧。它是对[语言规范](https://go-zh.org/ref/spec)、 [Go语言之旅](https://tour.golang.org/)以及[如何使用Go编程](https://go-zh.org/doc/code.html)的补充说明，因此我们建议您先阅读这些文档。

## License
除特别注明外， 本页内容均采用知识共享-署名（CC-BY）3.0协议授权，代码采用BSD协议授权。
