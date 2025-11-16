# TryHackMe: [Networking Core Protocols] Write-up

**Completed:** [2025.11.16]
**Difficulty:** Easy
## Task 4: HTTP(S): Accessing the Web

**Question:** Use telnet to access the file flag.html on MACHINE_IP. What is the hidden flag?
用 telnet 访问文件 flag.html MACHINE_IP。 什么是隐藏旗帜？
**Answer:** THM{TELNET-HTTP}

**How to solve:**
1. 用telnet远程登陆虚拟机ip:telnet .... 80(HTTP是80/8080，HTTPs是443/8443）
2. GET / flag.html_HTTP/1.1
3. HOST: 虚拟机地址

## Learned Concepts
- 如何用telnet查看网页信息
- HTTP默认监听端口80

## Task 5: FTP
**Question:** Using the FTP client ftp on the AttackBox, access the FTP server at 10.201.55.246 and retrieve flag.txt. What is the flag found?
通过 AttackBox 上的 FTP 客户端 ftp，访问 10.201.55.246 的 FTP 服务器并获取 flag.txt。发现的旗帜是什么？
**Answer:** THM{FAST-FTP}

**How to solve:**
1. 首先登录：ftp .....
2. 用ls列出文件列表
3. get flag.txt - （一定要有后面的—否则看不了，而且没有的话只能是标准文件下载）

## Learned Concepts
- 如何用ftp查看文档内容
- 切换为文档模式：type ASCII。
- 匿名登陆：name:anonymous
- FTP默认监听TCP端口21

## Tools Used
- `attracker`
## Task 6: SMTP: Sending Email  SMTP:发送电子邮件
## Learned Concepts
- HELO/EHLO 临时发起会话 如:HELO client.thm
- MAIL FROM 指定发件人邮箱
- RCPT TO 指定收件人的邮箱地址
- DATA 表明要发送的内容
- . 单独一行表示邮件内容结束
- SMTP 服务器默认监听 TCP 端口 25
- 比如：HELO client.thm --表明身份，我是client
-      MAIL FROM <a@.com> --设定发件人为a@.com>
-      RCPT TO <B@.COM> --设定收件人为B@.com>
-      DATA  --开始输入邮件内容
##Task 7:POP3接收邮件
##Question:**Looking at the traffic exchange, what is the name of the POP3 server running on the remote server?
查看流量交换，运行在远程服务器上的 POP3 服务器叫什么名字？
Dovecot   []中是服务器支持的拓展，ubuntu左侧是POP3的名字

## Learned Concepts
-POP3监听端口110
-USER <..> -- 识别用户
-PASS <password> --提供密码
-STAT  --请求消息总数和总大小
-LIST --列出所有消息和大小
-RETR <m_n> --检索指定消息
-DELE <message_number> --删除信息
-QUIT --退出
## Task 8: IMAP: Synchronizing Email同步邮件
**Question:** What IMAP command retrieves the fourth email message?
哪个 IMAP 命令可以检索第四封邮件？
**Answer:** FETCH 4 body[]
**How to solve:**
1. 首先登录：ftp .....
2. 用ls列出文件列表
3. get flag.txt - （一定要有后面的—否则看不了，而且没有的话只能是标准文件下载）

## Learned Concepts
-监听端口143
-LOGIN <username> <password> 登录
-SELECT <mailbox> 选择用于使用的邮箱文件夹
-MOVE <1> <2>将指定消息1移动到邮箱2
-FETCH <message_number> <date_item_num> 获取消息编号为3的 后面的<>有常用指令：body[]获取整个邮件（头部和正文） body[HEADER]只获取头部 body[TEXT]（只有正文不包括头部）
-COPY <> <>将一个消息复制到另一个邮箱里
-LOGOUT 登出


-Summary
telnet   23
DNS      53
http     80
https    43
FTP      21
SMTP     25
POP3     110
IMAP     143

只有DNS是有UDP协议，其他都是TCP协议
