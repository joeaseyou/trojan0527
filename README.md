Cloudflare-workers/pages代理脚本
支持workers部署，实现vless+ws+tls、trojan+ws+tls、vless+ws、trojan+ws代理节点

支持pages部署，实现vless+ws+tls、trojan+ws+tls代理节点

一：CF Vless节点可自定义内容
可修改Vless_workers_pages文件下的_worker.js文件
1、UUID必须自定义（第7行）

2、如果无法访问CF类网站或者ChatGPT，说明ProxyIP失效，可更换ProxyIP，自定义（第9行）

3、伪装网页目前留空，显示为400 Bad Request界面，可自定义（第10行）

也可在CF-workers/pages界面中使用变量设置，注：变量设置结果将覆盖本地修改结果
变量作用	变量名称	变量值要求	变量默认值
1、必要的uuid	uuid	符合uuid规定格式	万人骑uuid：77a571fb-4fd2-4b37-8596-1b7d9728bb5c
2、能上CF类网站	proxyip	ipv4地址、域名、[ipv6地址]	proxyip域名：cdn.xn--b6gac.eu.org
二：CF Trojan节点可自定义内容
可修改Trojan_workers_pages文件下的_worker.js文件
1、密码必须自定义（第4行）

2、如果无法访问CF类网站或者ChatGPT，说明ProxyIP失效，可更换ProxyIP，自定义（第5行）

3、伪装网页目前留空，显示为400 Bad Request界面，可自定义（第6行）

也可CF-workers/pages界面中使用变量设置，注：变量设置结果将覆盖本地修改结果
变量作用	变量名称	变量值要求	变量默认值
1、必要的密码	pswd	任意字符号	万人骑密码：trojan
2、能上CF类网站	proxyip	ipv4地址、域名、[ipv6地址]	proxyip域名：cdn.xn--b6gac.eu.org
