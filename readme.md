#### `golang moudle 学习`
升级golang版本至1.12版本

```
export  GO111MODULE = on
```





go命令维护一个go.sum的文件,其中包含特定模块版本内容的预期加密哈希

`go.sum` 不需要收到维护

`require github.com/astaxie/beego v1.11.1` 比如这一句话
* `require`关键字是引用
* 紧接着后面是包的名字
* 最后是版本

* download    download modules to local cache(从本地缓存下载modules)
* edit        edit go.mod from tools or scripts()
* graph       print module requirement graph(打印模块需要的图)
* init        initialize new module in current directory(在当前目录初始化一个新的moudle)
* tidy        add missing and remove unused modules(新增丢失的moudle,删除未用的moudle)
* vendor      make vendored copy of dependencies(制作一个依赖项的副本)
* verify      verify dependencies have expected content(校验依赖)
* why         explain why packages or modules are needed


Q1:依赖的包下载到哪里了?
A1:`$GOPATH/pkg/mod`

Q2:依赖包的版本如何控制?
A2:require 库名 @版本号  

Q3:可以把依赖放到$GOPATH/src下
A3:

Q4:项目如果不在$GOPATH/src下,引用自己怎么办
A4:模块名+路径

Q5:如果想把go.mod依赖的文件下载到vendor目录下
A5:go mod vendor



[参考go mod 链接](https://zhuanlan.zhihu.com/p/60703832)

