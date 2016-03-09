## 简介
Go 是一个新的语言。虽然是借鉴了现有的语言，但是它独有的特性可以使得高效的 Go 程序，与其它语言编写的程序相比，大不相同。直接将 C++ 或者 Java 程序转换为 Go 程序，是不可能产生令人满意的结果—— Java 程序是使用 Java 编写的，而不是 Go。另一方面，从 Go 的角度考虑问题则会产生成功的、而且大不相同的程序。换句话说，想要编写好的 Go 程序，理解它的特性和风格是非常重要的。了解 Go 语言编程中已有的约定也非常重要，例如命名、格式、程序结构等等。这会使得其他Go程序员容易理解你编写的程序。

该文档对如何编写清晰，符合语言规范的 Go 代码，给出了一些建议。你应该先阅读 [language specification](https://golang.org/ref/spec)，[Tour of Go](http://tour.golang.org/) 和 [How to Write Go Code](https://golang.org/doc/code.html)，然后将该文档作为扩展阅读。

### 例子
[Go package sources](https://golang.org/src/) 旨在不仅作为核心库来使用，而且还可以作为如何使用语言的例子。此外，许多程序包都包含了可以在[golang.org](http://golang.org/) 网站上独立执行的例子，例如[这一个](http://golang.org/pkg/strings/#example_Map)（如果需要，点击单词"Example"来打开）。如果你对如何处理一个问题，或者如何进行实现有疑问，那么库中的文档，代码和例子可以提供答案，概念和背景。
