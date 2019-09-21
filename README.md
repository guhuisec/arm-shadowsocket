# arm-shadowsocket
本人只是把python2和shadowsocks一起打包成可以在arm下运行的的shadowsocket,目前运行到arm系统版本如下：

```
Processor       : ARMv7 Processor rev 0 (v7l)
```


通过此方法可以很轻松在arm里面运行python和shadowsocket
当然了，大家有什么建议可以在建议里面提，
下面是列出的包的目录：
```
arm_py_ss.tar.gz
busybox	
config.json	
outssl.tar.gz
```
###arm_py_ss是python并且集成了shadowsocket，
###outssl是openssl arm版本，需要配置到环境，不然运行shadowsocket会提示找不到加密库。
###config.json是shadowsocket到配置文件内容如下：
```
{
	"server":"本机外网ip",
		"server_port":81,
		"local_port":3111,
		"password":"fuckyou",
		"timeout":600,
		"method":"aes-256-cfb"
}
```
###本人还在这里面集成了busybox


把bin目录和lib目录添加到环境变量和环境库中后，当然还有ssl也配置好，就可以在arm中运行了。


