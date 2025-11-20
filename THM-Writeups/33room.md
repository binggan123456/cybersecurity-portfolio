Option  选择	Explanation  解释
-sL	List scan – list targets without scanning
列表扫描——无需扫描即可列出目标
Host Discovery  宿主发现	
-sn	Ping scan – host discovery only
Ping 扫描——仅主机发现
Port Scanning  端口扫描	
-sT	TCP connect scan – complete three-way handshake
TCP 连接扫描——完整的三方握手
-sS	TCP SYN – only first step of the three-way handshake
TCPSYN——三方握手的第一步
-sU	UDP Scan  UDP 扫描
-F	Fast mode – scans the 100 most common ports
快速模式——扫描100个最常见的端口
-p[range]	Specifies a range of port numbers – -p- scans all the ports
指定端口号范围——-p- 扫描所有端口
-Pn	Treat all hosts as online – scan hosts that appear to be down
把所有主机都当作在线——扫描看起来宕机的主机
Service Detection  服务检测	
-O	OS detection  作系统检测
-sV	Service version detection
服务版本检测
-A	OS detection, version detection, and other additions
作系统检测、版本检测及其他新增功能
Timing  定时	
-T<0-5>	Timing template – paranoid (0), sneaky (1), polite (2), normal (3), aggressive (4), and insane (5)
时机模板——偏执（0）、狡猾（1）、礼貌（2）、正常（3）、激进（4）、疯狂（5）
--min-parallelism <numprobes> and --max-parallelism <numprobes>
--最小并行度<numprobes> 和 --max-parallelism<numprobes>	Minimum and maximum number of parallel probes
最小和最大并行探针数量
--min-rate <number> and --max-rate <number>
--最小速率 <number> 和 --max-rate <number>	Minimum and maximum rate (packets/second)
最小和最高速率（数据包/秒）
--host-timeout	Maximum amount of time to wait for a target host
等待目标主机的最大时间
Real-time output  实时输出	
-v	Verbosity level – for example, -vv and -v4
冗长程度——例如，-vv 和 -v4
-d	Debugging level – for example -d and -d9
调试级别——例如 -d 和 -d9
Report  报告	
-oN <filename>	Normal output  正常输出
-oX <filename>	XML output  XML 输出
-oG <filename>	grep-able output
可复制输出
-oA <basename>	Output in all major formats
所有主要格式的输出
