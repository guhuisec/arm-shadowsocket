# arm-shadowsocket
本人只是把python2和shadowsocks一起打包成可以在arm下运行的的shadowsocket,目前运行到arm系统版本如下：

```
Processor       : ARMv7 Processor rev 0 (v7l)
```


通过此方法可以很轻松在arm里面运行python和shadowsocket，本人还在这里面集成了busybox
当然了，大家有什么建议可以在建议里面提，
下面是列出的包的目录：
drwxr-xr-x@ 16 yx  staff      512  9 21 11:15 bin
-rw-r--r--@  1 yx  staff  1132724  9 20 13:11 busybox
-rw-r--r--@  1 yx  staff      139  9 21 11:22 config.json
drwxr-xr-x@  3 yx  staff       96  6 20  2018 include
drwxr-xr-x@  5 yx  staff      160  6 20  2018 lib
drwxr-xr-x@  3 yx  staff       96  6 20  2018 share
drwxr-xr-x@  6 yx  staff      192  6 20  2018 ssl

bin目录是python，ssl是openssl arm版本，需要配置到环境，不然运行shadowsocket会提示找不到加密库。
config.json
{
	"server":"本机外网ip",
		"server_port":81,
		"local_port":3111,
		"password":"fuckyou",
		"timeout":600,
		"method":"aes-256-cfb"
}
你需要修改server为本机外网ip就行

把bin目录和lib目录添加到环境变量和环境库中后，当然还有ssl也配置好，就可以在arm中运行了。


