# goproxy-php说明

本软件来源phuslu大神，仅使用其php模式。

任何软件都分为本地端与服务端

基于php，所以任何搭建了php语言的服务器/vps均可使用，只要将本站提供的goproxy.php放置于服务器目录，并设置本地端即可使用

# 服务端所用goproxy.php文本

有些支持git部署的服务器，可以直接输入git地址进行部署。

如果不支持git，可以将文本直接传到网站根目录

# 最终本地端调用方式
php.json文件中
修改URL地址：http://example.com/goproxy.php 或者 https://example.com/goproxy.php

若URL地址是https，则“SSLVerify”:true；若URL地址是http，则“SSLVerify”:flase。

httpproxy.json文件中

修改第三行： “Enabled”:false
修改”PHP”: 下面一行：

“Enabled”:true

“Address”: “127.0.0.1:8088”

最后设置代理服务器为http协议127.0.0.1:8088即可
