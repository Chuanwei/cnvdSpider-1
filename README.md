# cnvdSpider v0.4(单线程无代理模式)
					本脚本用来自动化生成cnvd的漏洞报告
					
1安装
cd /项目根目录
pip install -r requirement

2使用教程
python main.py 
-w (要爬取的web应用程序漏洞的页数) 
-a (要爬取的app应用漏洞的页数) 
-s (要爬取的操作系统漏洞的页数) 
-d (要爬取的网络设备漏洞的页数)
-wl (要爬取的web应用程序漏洞的安全等级,默认为2) 
-al (要爬取的app应用程序漏洞的安全等级,默认为1) 
-sl (要爬取的操作系统漏洞的安全等级,默认为1)
-dl (要爬取的网络设备漏洞的安全等级,默认为1) 
-m  (设置爬取的方法,按时间爬取,或者按页数爬取默认按时间爬取,爬取天数为1周7天)
-ST  (设置按时间爬取的开始时间,格式如 -ST 2019-10-11)
-ET  (设置按时间爬取的结束时间,格式如 -ET 2019-10-21)

example:
python main.py (默认按时间爬取1周的漏洞,从七天前至今天)
python main.py -ST 2019-10-11 -ET 2019-10-21 -m time (按时间爬取从2019-10-11~2019-20-21的漏洞)
python main.py -w 5 -a 4 -s 3 -d 2 -m page(按页数爬取,爬取每个类型指定的页数) 

安全等级:
	[1~3]
	1：只爬取等级为高的漏洞
	2：只爬取等级为高和中的漏洞
	3：高中低的漏洞都爬取

生成的安全通告默认在项目根目录

tips:脚本使用单线程,没有使用代理池可能爬取速度会比较慢
如果有问题请发邮件到fengwei@aiosh.com或者联系@qq:2716508591


更新:
比v0.3多加了按时间爬取的功能
修复了wps表格宽度问题


