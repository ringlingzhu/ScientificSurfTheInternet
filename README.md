# 科学上网

系统 centos 6 一键安装shadowsocks   https://teddysun.com/357.html （安装完启动成功，仍然不能访问，考虑防火墙问题，我这里清理了防火墙 iptables -F）

支持多密码：改shadowsocks.json文件，去掉port和password，改为 port_password ，格式如下：
{
 "server":"my_server_ip"，
 "local_address": "127.0.0.1",
 "local_port":1080,
  "port_password": {
     "8381": "foobar1",
     "8382": "foobar2",
     "8383": "foobar3",
     "8384": "foobar4"
 },
 "timeout":300,
 "method":"aes-256-cfb",
 "fast_open": false
}
