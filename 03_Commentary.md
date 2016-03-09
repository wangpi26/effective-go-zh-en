## 注释
Go提供了C风格的块注释/\* \*/和C++风格的行注释//。通常为行注释；块注释大多数作为程序包的注释，但也可以用于一个表达式中，或者用来注释掉一大片代码。

程序—同时又是网络服务器—godoc，用来处理Go源文件，抽取有关程序包内容的文档。在顶层声明之前出现，并且中间没有换行的注释，会随着声明一起被抽取，作为该项的解释性文本。这些注释的本质和风格决定了godoc所产生文档的质量。

每个程序包都应该有一个包注释，一个位于package子句之前的块注释。对于有多个文件的程序包，包注释只需要出现在一个文件中，任何一个文件都可以。包注释应该用来介绍该程序包，并且提供与整个程序包相关的信息。它将会首先出现在godoc页面上，并会建立后续的详细文档。

```
/*
Package regexp implements a simple library for regular expressions.

The syntax of the regular expressions accepted is:

    regexp:
        concatenation { '|' concatenation }
    concatenation:
        { closure }
    closure:
        term [ '*' | '+' | '?' ]
    term:
        '^'
        '$'
        '.'
        character
        '[' [ '^' ] character-ranges ']'
        '(' regexp ')'
*/
package regexp
```

如果程序包很简单，则包注释可以非常简短。

```
// Package path implements utility routines for
// manipulating slash-separated filename paths.
```
注释不需要额外的格式，例如星号横幅。生成的输出甚至可能会不按照固定宽度的字体进行展现，所以不要依靠用空格进行对齐—godoc，就像gofmt，会处理这些事情。注释是不作解析的普通文本，所以HTML和其它注解，例如_this_，将会逐字的被复制。对于缩进的文本，godoc确实会进行调整，来按照固定宽度的字体进行显示，这适合于程序片段。[fmt package](http://golang.org/pkg/fmt/)的包注释使用了这种方式来获得良好的效果。

根据上下文，godoc甚至可能不会重新格式化注释，所以要确保它们看起来非常直接：使用正确的拼写，标点，以及语句结构，将较长的行进行折叠，等等。

在程序包里面，任何直接位于顶层声明之前的注释，都会作为该声明的文档注释。程序中每一个被导出的（大写的）名字，都应该有一个文档注释。

文档注释作为完整的语句可以工作的最好，可以允许各种自动化的展现。第一条语句应该为一条概括语句，并且使用被声明的名字作为开头。

```
// Compile parses a regular expression and returns, if successful, a Regexp
// object that can be used to match against text.
func Compile(str string) (regexp *Regexp, err error) {
```
如果都是使用名字来起始一个注释，那么就可以通过grep来处理godoc的输出。设想你正在查找正规表达式的解析函数，但是不记得名字“Compile”了，那么，你运行了命令

```
$ godoc regexp | grep parse
```

如果程序包中所有的文档注释都起始于"This function..."，那么grep将无法帮助你想起这个名字。但是，因为程序包是使用名字来起始每个文档注释，所以你将会看到类似这样的信息，这将使你想起你要查找的单词。

```
$ godoc regexp | grep parse
    Compile parses a regular expression and returns, if successful, a Regexp
    parsed. It simplifies safe initialization of global variables holding
    cannot be parsed. It simplifies safe initialization of global variables
$
```

Go的声明语法允许对声明进行组合。单个的文档注释可以用来介绍一组相关的常量或者变量。由于展现的是整个声明，这样的注释通常非常肤浅。

```
// Error codes returned by failures to parse an expression.
var (
    ErrInternal      = errors.New("regexp: internal error")
    ErrUnmatchedLpar = errors.New("regexp: unmatched '('")
    ErrUnmatchedRpar = errors.New("regexp: unmatched ')'")
    ...
)
```
