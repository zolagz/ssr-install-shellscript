Ubuntu 配置 v2ray 

下载
https://github.com/Qv2ray/Qv2ray
![](https://tva1.sinaimg.cn/large/008i3skNgy1gwmsvyprhyj311e0podiy.jpg)
下载后，放在/opt/qv2ray/目录下

```
执行以下命令：

sudo chmod +x ./Qv2ray-v2.7.0-linux-x64.AppImage

输入以下命令(非root用户执行)：

./Qv2ray-v2.7.0-linux-x64.AppImage

```



### 配置链接服务器

执行后会出现主界面，点击导入

![](https://tva1.sinaimg.cn/large/008i3skNgy1gwmt0d3lzhj30yd0u00wb.jpg)

![](https://tva1.sinaimg.cn/large/008i3skNgy1gwmt1d5ln9j30qe0pc75z.jpg)

![](https://tva1.sinaimg.cn/large/008i3skNgy1gwmt4cz3aqj311f0u078w.jpg)



https://github.com/qv2ray/vcore
![](https://tva1.sinaimg.cn/large/008i3skNgy1gwmsx6kg35j30m803ldfy.jpg)
下载 ： v2ray-linux-64.zip 
然后解压到/home/user/.config/v2ray下面



![](https://tva1.sinaimg.cn/large/008i3skNgy1gwmt5ffklfj311f0u041x.jpg)

![](https://tva1.sinaimg.cn/large/008i3skNgy1gwmt6ndsj3j311c0u0wi9.jpg)

配置本机网络代理为手动：
临时使用：
![](https://tva1.sinaimg.cn/large/008i3skNgy1gwmtkapeuej30zz0u0gns.jpg)

推荐： Chrome 扩展插件：SwitchySharp



-------------------

# ssr-install-shellscript
one click to install ssr/ss
# 使用说明见: 
[Vien Blog](https://viencoding.com/article/122)


## 一键安装

将以下命令复制到你已连接的服务器命令行中，然后就是一步一步下一步

```
bash <(curl -s -L https://git.io/v2ray.sh)
```

选择1，按回车

```
 1. 安装
 2. 卸载
请选择 [1-2]:1
```

用默认的tcp就行，直接回车

```
请选择 V2Ray 传输协议 [1-32]
  1. TCP
  2. TCP_HTTP
  3. WebSocket
  4. WebSocket + TLS
  5. HTTP/2
  6. mKCP
  7. mKCP_utp
  8. mKCP_srtp
  9. mKCP_wechat-video
 10. mKCP_dtls
 11. mKCP_wireguard
 12. QUIC
 13. QUIC_utp
 14. QUIC_srtp
 15. QUIC_wechat-video
 16. QUIC_dtls
 17. QUIC_wireguard
 18. TCP_dynamicPort
 19. TCP_HTTP_dynamicPort
 20. WebSocket_dynamicPort
 21. mKCP_dynamicPort
 22. mKCP_utp_dynamicPort
 23. mKCP_srtp_dynamicPort
 24. mKCP_wechat-video_dynamicPort
 25. mKCP_dtls_dynamicPort
 26. mKCP_wireguard_dynamicPort
 27. QUIC_dynamicPort
 28. QUIC_utp_dynamicPort
 29. QUIC_srtp_dynamicPort
 30. QUIC_wechat-video_dynamicPort
 31. QUIC_dtls_dynamicPort
 32. QUIC_wireguard_dynamicPort
备注1: 含有 [dynamicPort] 的即启用动态端口..
备注2: [utp | srtp | wechat-video | dtls | wireguard] 分别伪装成 [BT下载 | 视频通话 | 微信视频通话 | DTLS 1.2 数据包 | WireGuard 数据包]
(默认协议: TCP):
```

端口随便写一个，范围1025到65535，也可以选择默认，直接回车

```
请输入 V2Ray 端口 [1-65535]
(默认端口: 47283):
```

这个也不知道真影响假影响，姑且相信他，使用默认，直接回车

```
是否开启广告拦截(会影响性能) [Y/N]
(默认 [N]):
```

是不是顺便把ss服务也装了，这个就随便你了，我感觉用了v2ray也没必要再搭ss，毕竟s's很容易被封，所以保持默认，回车

```
是否配置 Shadowsocks [Y/N]
(默认 [N]):
```

会让你确认一下信息，确认无误，按回车

```
---------- 安装信息 -------------
 V2Ray 传输协议 = TCP
 V2Ray 端口 = 47283
 是否配置 Shadowsocks = 未配置
---------- END -------------
按 Enter 回车键 继续....或按 Ctrl + C 取消.
```

然后，就是等...

如果中间出现这些图片，就回车就好了。

![file](https://viencoding.com/storage/20190925/L6BMGOgSxvHNJDSob9OxMyatt39KEQ6TKUJw8nd7.png)

![file](https://viencoding.com/storage/20190925/1J7gUZaCzL2W0ujhIOU1uGc40IWxb1Px4poJ0zDE.png)

安装完成，最后会提示你连接配置信息：

```
---------- V2Ray 配置信息 -------------
 地址 (Address) = 152.89.208.146
 端口 (Port) = 47283
 用户ID (User ID / UUID) = ed0b4117-0f5a-41e9-a732-96bdaf343d23
 额外ID (Alter Id) = 233
 传输协议 (Network) = tcp
 伪装类型 (header type) = none
---------- END -------------
```

也可以通过命令`v2ray url` 和 `v2ray qr` 获取v2ray url和v2ray QRCode

```
root@ONEVPS190911085532:~# v2ray url
---------- V2Ray vmess URL / V2RayNG v0.4.1+ / V2RayN v2.1+ / 仅适合部分客户端 -------------
vmess://ewoidiI6ICIyIiwKInBzIjogIjIzM3YyLmNvbV8xNTIuODkuMjA4LjE0NiIsCiJhZGQiOiAiMTUyLjg5LjIwOC4xNDYiLAoicG9ydCI6ICI0NzI4MyIsCiJpZCI6ICJlZDBiNDExNy0wZjVhLTQxZTktYTczMi05NmJkYWYzNDNkMjMiLAoiYWlkIjogIjIzMyIsCiJuZXQiOiAidGNwIiwKInR5cGUiOiAibm9uZSIsCiJob3N0IjogIiIsCiJwYXRoIjogIiIsCiJ0bHMiOiAiIgp9Cg==
root@ONEVPS190911085532:~# v2ray qr
---------- V2Ray 二维码链接 适用于 V2RayNG v0.4.1+ / Kitsunebi -------------
https://233boy.github.io/tools/qr.html#vmess://ewoidiI6ICIyIiwKInBzIjogIjIzM3YyLmNvbV8xNTIuODkuMjA4LjE0NiIsCiJhZGQiOiAiMTUyLjg5LjIwOC4xNDYiLAoicG9ydCI6ICI0NzI4MyIsCiJpZCI6ICJlZDBiNDExNy0wZjVhLTQxZTktYTczMi05NmJkYWYzNDNkMjMiLAoiYWlkIjogIjIzMyIsCiJuZXQiOiAidGNwIiwKInR5cGUiOiAibm9uZSIsCiJob3N0IjogIiIsCiJwYXRoIjogIiIsCiJ0bHMiOiAiIgp9Cg==
 友情提醒: 请务必核对扫码结果 (V2RayNG 除外)
```

## 客户端配置

- windows: `https://github.com/v2ray/v2ray-core/releases` 然后选择 v2ray-windows-64.zip 下载，如果你的系统是 32 位的那就选择 v2ray-windows-32.zip。 下载完成，解压。 打开解压出来的文件夹 (例如 v2ray-xxxx-windows-64，xxxx为版本号)
- mac os: `https://github.com/Cenmrev/V2RayX/releases`
- ios: `https://free.shadowrocket.online`
- Android: `https://www.geekersq.cc/v2ray/v2rayNG_v0.6.19.apk`

下载一个v2ray的软件，我以Mac上的软件为例：

![file](https://viencoding.com/storage/20190925/SrBCOOytIXDHMc0dfYMvEDPuNGzv3Weba66Vnplq.png)

复制粘贴到对应位置，点击OK

![file](https://viencoding.com/storage/20190925/llohdrUwA2eOjLVIj7o5X6NcJtur8UBu03vnsqFn.png)

选择刚刚配置的服务

![file](https://viencoding.com/storage/20190925/Vf1W1rVRpMW9D5njIbImOTgPhiVqvEWupgxW2iCP.png)

然后load core就是开启

![file](https://viencoding.com/storage/20190925/KzPIKjdJEwk8aKrqQFRvG0jBuAwHDhOIK5OuGB9R.png)


**viencoding.com版权所有，允许转载，但转载请注明出处和原文链接: https://viencoding.com/article/207**
