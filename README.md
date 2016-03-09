`《Effective Go》` 作为 `GO` 语言的入门必读教程，值得每位初学者好好阅读一遍，编辑成书，方便阅读交流。

*参考官方版：[Effective Go](https://golang.org/doc/effective_go.html)*

*参考翻译版：[Effective Go](http://www.hellogcc.org/effective_go.html)*

**[Fork me on GitHub](https://github.com/bingoHuang/effective-go-cn-gitbook)**

## 当前完成章节（持续更新）：

### 已完成章节：
0. [前言](README.md)
* [简介](01_Overview.md)
* [格式](02_Formatting.md)
* [注释](03_Commentary.md)

### 未完成章节：
* [命名](04_Names.md)
* [分号](05_Semicolons.md)
* [控制](06_Control_structures.md)
* [函数](07_Functions.md)
* [数据](08_Data.md)
* [初始](09_Initialization.md)
* [方法](10_Methods.md)
* [接口](11_Interfaces_and_other_types.md)
* [空符](12_The_blank_identifier.md)
* [内嵌](13_Embedding.md)
* [并发](14_Concurrency.md)
* [错误](15_Errors.md)
* [服务](16_A_web_server.md)

## 简介
`Go` 是一个新的语言。虽然是借鉴了现有的语言，但是它独有的特性可以使得高效的 Go 程序，与其它语言编写的程序相比，大不相同。直接将 C++ 或者 Java 程序转换为 Go 程序，是不可能产生令人满意的结果—— Java 程序是使用 Java 编写的，而不是 Go。另一方面，从 Go 的角度考虑问题则会产生成功的、而且大不相同的程序。换句话说，想要编写好的 Go 程序，理解它的特性和风格是非常重要的。了解 Go 语言编程中已有的约定也非常重要，例如命名、格式、程序结构等等。这会使得其他Go程序员容易理解你编写的程序。

该文档对如何编写清晰，符合语言规范的 Go 代码，给出了一些建议。你应该先阅读 [language specification](http://localhost:6060/ref/spec)，[Tour of Go](http://tour.golang.org/) 和 [How to Write Go Code](http://localhost:6060/doc/code.html)，然后将该文档作为扩展阅读。
