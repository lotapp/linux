# linux

linux安全检查
Mail:liuquyong112@gmail.com

## 脚本说明

1. 将本目录所有文件都放入到一台自己的本地linux主机同一目录下
2. 将服务器IP、普通账号、普通账号密码、root密码依次按以下格式写入到hosts.txt中（注意“:”作为hosts.txt的分隔符）：
    - 192.168.1.81:user:123456:nothing
    - 192.168.1.10:user:123456:nothing
    - 192.168.1.11:user:123456:nothing
3. 执行sh login.sh,脚本将自动批量上传checklinux.sh到服务器/tmp目录下，并且自动执行和自动上传结果到本地linux主机上
4. 最后将服务器上传的脚本和结果自动删除

checkrulues: 部分判断逻辑,这里面目前仅有端口的判断逻辑,后期可以将进程、应用程序是否有漏洞等逻辑放在这里面进行安全检查,比较简单的判断逻辑直接在 buying_linuxcheck.sh 中可以实现

```shell
buying_linuxcheck.sh: 核心检查逻辑

del.exp: 删除远程服务器上的脚本与检查结果

get.exp: 获取远程服务器上安全检查的结果

hosts.txt:需要被检查的服务器列表

login.sh:一键进行登录检查,安全检查时只需要运行该脚本即可

put.exp:将安全检查脚本上传到远程服务器上

readme.txt:使用相关说明文档

sh.exp:在远程服务器上执行安全检查脚本
```

(注意：本脚本适用于linux系统)

## 目录

![toc](https://img2018.cnblogs.com/blog/1127869/201905/1127869-20190519081655539-153631561.jpg)
