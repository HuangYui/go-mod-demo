GOPROXY

这个环境变量主要是用于设置 Go 模块代理（Go module proxy）,其作用是用于使 Go 在后续拉取模块版本时直接通过镜像站点来快速拉取。

GOPROXY 的默认值是：https://proxy.golang.org,direct

proxy.golang.org国内访问不了,需要设置国内的代理.

●  阿里云
https://mirrors.aliyun.com/goproxy/
●  七牛云
https://goproxy.cn,direct

如:

$ go env -w GOPROXY=https://goproxy.cn,direct

GOPROXY 的值是一个以英文逗号 “,” 分割的 Go 模块代理列表，允许设置多个模块代理，假设你不想使用，也可以将其设置为 “off” ，这将会禁止 Go 在后续操作中使用任何 Go 模块代理。

设置命令
```shell 
go env -w GOPROXY=https://goproxy.cn,https://mirrors.aliyun.com/goproxy/,https://goproxy.cn,direct
```


go使用的是github仓库的包,查询地址：
https://pkg.go.dev/

如何发布包到https://pkg.go.dev/

https://www.bilibili.com/read/cv21221484/