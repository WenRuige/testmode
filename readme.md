#### `golang moudle`
升级golang版本至1.12版本

```
export  GO111MODULE = on
```





go命令维护一个go.sum的文件,其中包含特定模块版本内容的预期加密哈希

go.sum 不需要收到维护


download    download modules to local cache(从本地缓存下载modules)
edit        edit go.mod from tools or scripts()
graph       print module requirement graph
init        initialize new module in current directory
tidy        add missing and remove unused modules
vendor      make vendored copy of dependencies
verify      verify dependencies have expected content
why         explain why packages or modules are needed


Q1:依赖的包下载到哪里了?
A1:`$GOPATH/pkg/mod`

Q2:依赖包的版本如何控制?
A2:require 库名 @版本号  

Q3:可以把依赖放到$GOPATH/src下
A3:

Q4:项目如果不在$GOPATH/src下,引用自己怎么办
A4:模块名+路径



[参考go mod 链接](https://zhuanlan.zhihu.com/p/60703832)

