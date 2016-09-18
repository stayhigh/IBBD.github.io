# IBBD Golang编码风格

- 满足`go fmt`之外，还需要遵守一定的内部风格，原则上以golang的源码风格为准，见[文档](https://github.com/golang/go)
- [golang配置文件风格](/golang/golang-env-config.md)
- 所谓的代码风格，通常是以保证可维护性和可测试性为目的的。

## 变量

- 变量命名总体要遵守语义明确的原则，避免无意义的单词。
- 尽量避免使用拼音命名，除非确实难以翻译。
- `常量`和`普通变量`：和变量的命名一样，统一为驼峰命名法，通常不使用下划线。如果首字母大写，则该变量在引用时，能别外部使用；否则，只能在package内部使用。
- `结构体内的字段`：采用和普通变量一样的驼峰命名方式，首字母大小写区分是否全局。
- `循环变量`：对于短循环的循环变量，可能使用像`i`，`j`，`k`，`v`等之类的单字母变量（这是习惯用法，通常不应该命名为其他的字母，例如abc等）。
- `type新类型`：采用和普通变量一样的方式。


## 函数

- `命名`：采用驼峰命名法，首字母是否大小写来区分是否全局有效。
- `长度`：一个函数通常不宜太长，超过50行的应该是少数，超过100行的更是少数的少数。
- 函数是在整个package内部有效的，如果模块聚合不合理，很容易出现找不到在哪里定义的问题。函数名应该是跟文件名有某种联系的（功能的内聚），这个比较难判断。


## 文件与目录

- 文件名的命名采用小写字母和下划线的形式。例如`hello_world.go`
- 目录名的命名采用小写字母和连接符`-`，例如`hello-world`

## 包名命名

- 类似变量的命名方式，驼峰命名方式，首字母小写。
- 如果对应的目录名为`hello-world`，则对应的包名应该是`helloWorld`

