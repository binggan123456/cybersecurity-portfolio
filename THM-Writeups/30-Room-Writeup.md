# TryHackMe: [Networking Secure Protocols] Write-up

**Completed:** [2025.11.17]
**Difficulty:** Easy

## Task 5: HTTPS

**Question:** How many packets did the TLS negotiation and establishment take in the Wireshark HTTPS screenshots above?
在上面 Wireshark 的 HTTPS 截图中，TLS 协商和建立接收了多少数据包？
**Answer:** 8

**How to solve:**
1. TCP是文件传输协议，TLS是加密协议，所以TLS协商和建立接受多少数据包要取决于TCP

## Learned Concepts
- 浏览器与HTTP交互指令：GET / HTTP/1.1
-
# TryHackMe: [房间名称] Write-up

**Completed:** [完成日期]
**Difficulty:** Easy

## Task 4: SMTPS, POP3S, and IMAPS  SMTPS、POP3S 和 IMAPS

**Question:** If you capture network traffic, in which of the following protocols can you extract login credentials: SMTPS, POP3S, or IMAP?
如果你捕获网络流量，可以通过以下哪种协议提取登录凭证：SMTPS、POP3S，还是 IMAP？
**Answer:** `IMAP


## Learned Concepts
- 加上s后更加安全，而IMAP没有s，属于不安全的一种，可以用来提取
