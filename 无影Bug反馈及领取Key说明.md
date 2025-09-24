

## 致谢

`无影 (TscanPlus)` 自 2023 年 12 月发布 v1.0 以来，受到了广大安全研究人员和技术爱好者的关注和支持。

在此，我们特别感谢各位师傅（来自 GitHub、知识星球、工具交流群等）提出的宝贵修改建议和诸多 Bug！

你们的支持与反馈是我不断优化和进步的动力。

## 反馈及奖励

自2024年7月发布v2.2版后，`无影 (TscanPlus)`上线Vip认证功能【目前Vip可解锁所有Poc和密码破解连接验证功能】，开启“**提交一个有效Bug，Bug修复后可获得一个Key**”模式。

**提交Bug的师傅在Bug修复后，在修复Bug后的发布版—`About页面`可看到致谢名单，凭致谢名单截图发送到邮箱 [xyguest@gmail.com](mailto:xyguest@gmail.com)，可获得Key一枚，并被拉进Bug反馈专用群。**

为了更好地完善和改进`无影 (TscanPlus)`，重新说明一下 Bug 反馈的方式：

1. **GitHub Issue**：在项目的 [GitHub Issue](https://github.com/TideSec/TscanPlus/issues) 页面提交 Bug 反馈和功能建议。
2. **知识星球**：加入[知识星球](https://wx.zsxq.com/group/15525258451582)也**可直接获得3个key且可无限重置**，同时开放了交流渠道，可随时发帖留言。
3. **电子邮箱**：如涉及敏感信息、视频等，也可发送至我的邮箱 [xyguest@gmail.com](mailto:xyguest@gmail.com)，不过邮箱查看可能不会太及时。
4. **工具交流群**：~~由于个人开发，精力有限，目前只开设了一个交流群，且目前已满。~~

上线Vip认证功能主要也是为了Poc搜集和使用能形成良性生态，自 2024年 7 月以来在Poc平台上提交的的Poc数量约为400+，针对有效Poc发放key约300+，提交Poc换Key的说明可查看这里：[POC提交及无影Key获取说明.md][url-poc-key] 

希望大家继续多提宝贵的建议和意见，共同打造更优秀的网络安全工具！感谢每一位使用和支持`无影 (TscanPlus)`的朋友！



## Bug反馈统计

【2025.10.01】无影(TscanPlus)自2023年12月上线来，截止目前共发布62个版本，**增加/升级65项功能，累计修复317个用户反馈的591个Bug**，反馈Bug统计数据如下。

为感谢大家一直以来对无影的支持，**提交已修复bug数量达5个(含5个)以上的用户可免费加入[“剑影安全实验室”知识星球](https://wx.zsxq.com/group/15525258451582)**，可根据榜单上的数量私聊我或发邮件 [xyguest@gmail.com](mailto:xyguest@gmail.com)。



<table style="width:100%; table-layout:fixed; border:1px solid black; border-collapse:collapse;">
  <tr>
    <td style="width:50%; border:1px solid black; vertical-align:top; padding:10px;">
      <b>无影更新及Bug反馈记录</b>
    </td>
    <td style="width:50%; border:1px solid black; vertical-align:top; padding:10px;">
      <b>Bug反馈统计数据及榜单</b>
    </td>
  </tr>
  <tr>
    <td style="width:50%; border:1px solid black; vertical-align:top; padding:10px;">
       <br>
<b> v3.0.0版 【2025.09.23】 
	1、增加Awvs扫描功能 @天明 <br>
	2、项目管理支持定时任务 @秋茶- <br>
	3、jwt编码支持多种密钥编码 @树先生  <br>
	4、jwt秘钥编码与jwt.io兼容 @秋茶- @mk4no1  <br>
	5、域名枚举数据右键增加密码破解 @笑傲江湖 <br>
	6、密码破解增加全局超时限制 @小白 <br>
	7、MongoDB密码破解资源占用高 @呱呱 <br>
	8、增强JS接口爬取与解析功能 @无先森 <br>
	9、密码破解RDP协议闪退 @0x1eeA @jo3ker <br>
	10、根据问卷调查重排功能模块顺序 <br>
<br>
<b> v2.9.9版 【2025.09.03】 </b>  <br>
	1、针对poc、js结果增加AI辅助分析功能 @呱呱 <br>
	2、密码破解增加docker未授权检测 @youxia5 <br>
	3、敏感目录字典更新 @无先森 <br>
	4、beianx备案查询cookie信息变更 @TAI <br>
	5、jwt密钥兼容base64url格式 @树先生 <br>
	6、SMTP爆破功能不兼容SSL协议 @nnasdlc <br>
	7、高级配置中目录打开有误 @秋茶- @Easonc8 <br>
	8、jwt密钥成功但校验失败 @小白 <br>
	9、编码转换增加Url全编码选项 @秋茶- <br>
	10、AES功能解密异常 @零乱 <br>
<br>
<b> v2.9.8版 【2025.08.21】 </b>  <br>
	1、风鸟cookie异常导致查询报错 @Seven @zzzhhha <br>
	2、密码破解的暂停功能无效 @菜鸟的菜 <br>
	3、筛选数据后选择所有行无效 @xj90512 <br>
	4、个别Poc检测存在误报漏报 @shuai32768 <br>
	5、代理池当前代理显示地区和延迟 @n0rth_404 <br>
	6、JsFinder部分规则存在误报 @雪山乘客 <br>
	7、JsFinder个别站点标题乱码 @小白 <br>
	8、JsFinder结果展示优化 @一根胡萝卜 <br>
	9、ICP备案信息批量查询功能优化 @缓归 <br>
	10、SSH服务爆破执行命令异常 @陌上花开 <br>
<br>
<b> v2.9.7版 【2025.08.20】 </b>  <br>
	1、增加项目中断后继续扫描功能  <br>
	2、信息搜集到资产探测到漏洞检测流程化 @zzzhhha <br>
	3、激活码认证时硬件信息读取异常 @孙吉国杰 <br>
	4、信息搜集联动web指纹时nuclei异常 @n0rth_404 <br>
	5、增加程序退出确认防止意外关闭 @faow <br>
	6、jwt校验根据算法进行密钥截断或补零 @xiaoliusec <br>
	7、主动指纹探测策略优化 @hellowchen <br>
	8、Svn破解支持GET和PROPFIND两种方式 @ZenkiH <br>
	9、空间测绘增加自定义延迟时间 @zzzhhha <br>
	10、编辑项目时信息搜集选项不保存 @zzzhhha <br>
<br>
<b> v2.9.6版 【2025.08.12】 </b>  <br>
	1、提权辅助的检索功能无效 @nn0nkey <br>
	2、信息搜集增加域名及ip归属地查询 @文欧 <br>
	3、信息搜集Cookie校验超时 @Yo皮蛋 <br>
	4、bypass开启大小写绕过闪退 @pemuse @A1 <br>
	5、全局配置增加自定义body设置 @秋茶- <br>
	6、jwt解析增加异常字符处理 @按时睡觉 <br>
	7、Web指纹的截图功能支持全局UA @Reluctantly <br>
	8、SSH破解时因空行导致结果异常 @树先生 <br>
	9、key过期提示优化 @zzzhhha <br>
	10、JsFinder爬虫策略优化 @小白 <br>
<br>
<b> v2.9.5版 【2025.07.28】 </b>  <br>
	1、信息搜集功能与项目管理集成 <br>
	2、优化jsfinder功能并支持自定义规则 @TFour123 @@qty567 <br>
	3、对资产可自定义标签并标记颜色 <br>
	4、增加jwt已知漏洞检测功能 @amoy6228 <br>
	5、优化目录枚举高并发导致闪退 @丶ty @雪山乘客 <br>
	6、密码破解多个账户时进度异常 @呱呱 <br>
	7、jwt爆破增加密钥多种编码选择 @z1603206931 <br>
	8、项目管理中卡在待执行状态 @b2522 <br>
	9、关闭端口指纹选项时端口数据不显示 @Backspace <br>
	10、信息收集页面切换项目闪退 @Y. <br>
<br>
<b> v2.9.4版 【2025.07.16】 </b>  <br>
	1、RDP密码爆破导致闪退 @ziyue0230 <br>
	2、杀软查询时	 @Wans <br>
	3、新建项目后项目列表刷新异常 @hello @momxSec <br>
	4、列表数据检索支持&和||运算符 @太霖 <br>
	5、资产测绘右键功能联动闪退 @弹弹弹 @Vain @太霖  <br>
	6、icp备案查询增加停止功能 @jiuyueyi <br>
	7、主动指纹结果较多时优化处理 @Crab <br>
	8、项目执行状态时禁止项目编辑 @b2522 <br>
	9、根据企业名进行信息搜集数据显示不完整 @X <br>
	10、域名枚举右键功能联动闪退 @xmqaq @J0k4r5 <br>
<br>
<b> v2.9.3版 【2025.07.10】 </b>  <br>
	1、达梦数据库密码破解联动Bug @KaerSAN <br>
	2、web探测超时时间过长 @菜鸟的菜 <br>
	3、poc联动检测时部分目标缺失 @小白 <br>
	4、ICMP存活探测模式时域名探测无效 @R <br>
	5、右键破解增加根据端口/服务自匹配 @酒零 <br>
	6、Telnet密码破解闪退 @呱呱 @洋丞 <br>
	7、密码破解增加JDWP、RMI未授权检测 @kio <br>
	8、资产分拣时大网段导致闪退 @KaerSAN <br>
	9、空间测绘时icon查询标签名相同 @fu221ng <br>
	10、资产测绘多个Key时可用验证失败 @15679768019 <br>
<br>
<b> v2.9.2版 【2025.07.01】 </b>  <br>
	1、增加达梦数据库密码破解  <br>
	2、增加ActiveMQ服务密码破解 <br>
	3、增加RabbitMQ服务密码破解 <br>
	4、增加RMI服务密码破解 <br>
	5、增加Kafka服务密码破解 <br>
	6、增加Neo4j服务密码破解 <br>
	7、增加Modbus、ADB未授权检测 <br>
	8、支持mongodb高版本未授权检测 @wuha <br>
	9、信息搜集模块增加导出和批量关闭 @秋茶- @. @youcs233 <br>
	10、密码字典可选择追加或覆盖模式 @鼎级FW @雾散 <br>
<br>
<b> v2.9.1版 【2025.06.23】 </b>  <br>
	1、空间测绘中某些tab无法彻底关闭 @jason9777598 <br>
	2、项目编辑中默认显示内置字典 @ZACsec <br>
	3、poc检测时目标url路径被截断 @Pyl0ad <br>
	4、poc检测查看数据包无post的body数据 @秋茶- <br>
	5、增加标题Slogan开关选项 @圣男 <br>
	6、信息搜集和资产测绘增加历史查询 @cf48rty0 <br>
	7、端口扫描增加防火墙检测选项 @贝贝 <br>
	8、端口扫描增加状态码筛选 @xiaridenuanfeng <br>
	9、40xbypass不支持socks5类型代理 @totooss <br>
	10、信息搜集cookie验证时代理无效 @小白 <br>
<br>
<b> v2.9.0版 【2025.06.16】 </b>  <br>
	1、正式上线信息搜集模块 <br>
	2、上线ICP备案信息批量查询功能 <br>
	3、支持多目标(域名/单位名/IP)批量查询 <br>
	4、集成爱站、Chinaz、风鸟、备案API等 <br>
	5、整合站点信息、备案信息、域名信息、企业信息 <br>
	6、整合端口、子域名、IP/域名反查、历史解析等数据 <br>
	7、集成分支机构、对外投资、软著、APP、小程序等查询 <br>
	8、支持信息搜集与端口扫描、web指纹等功能联动 <br>
	9、支持多tab页展示和本地数据库存储 <br>
	10、ICP备案批量查询支持API动态调配 <br>
	 <br><br>
<b> v2.8.4版 【2025.06.13】 </b>  <br>
	1、空间测绘API支持多个key轮询 @cf48rty0 <br>
	2、资产测绘增加“多查询条件“输入 @TFour123 <br>
	3、提权辅助功能增加完善CVE信息 @曾哥 <br>
	4、对所有表格数据增加检索功能 @小白 <br>
	5、增加手动更新功能 @菜鸟的菜 <br>
	6、信息搜集配置模块前端数据同步 @心海 <br>
	7、项目管理表格无法拖动 @Avalon @20812807 <br>
	8、密码破解功能无法单独勾选服务 @daryl888 <br>
	9、优化API有效性验证时扣积分较多问题 @cf48rty0 <br>
	10、FofaAPI的key验证可用性失效 @NewGtBoy <br>
<br>
<b> v2.8.3版 【2025.06.08】 </b>  <br>
	1、代理池增加免费代理爬取功能  <br>
	2、端口扫描时端口随机以规避IPS @呱呱 <br>
	3、密码破解功能在探测端口时闪退 @呱呱 <br>
	4、内置POC无法进行多线程扫描 @bupsdx <br>
	5、增加ICMP和PING两种存活探测选项 @瑶瑶 <br>
	6、扫描时提示“是否清除已有数据” @菜鸟的菜 <br>
	7、Snmp弱口令检测失败 @beauty @Mrship12138 <br>
	8、Snmp及SMB弱口令检测误报 @Backspace <br>
	9、编码转换模块增加滚动条 @fricka6768 <br>
	10、密码破解支持ip:port格式 @0xFF <br>
<br>
<b> v2.8.2版 【2025.05.30】 </b>  <br>
	1、网卡切换后无法切回Auto模式 @sonumb-z <br>
	2、功能联动Poc时控制第三方工具进程数 @榆关 <br>
	3、Poc列表显示异常，增加指纹Poc提示 @秋茶- <br>
	4、host碰撞的队列显示异常 @Pyl0ad @dafupp <br>
	5、webshell功能无法滚动显示 @echo-Shu <br>
	6、对ping检测进行优化完善 @je5442804 <br>
	7、限制空间测绘语法标签长度 @miki-java <br>
	8、RDP密码破解异常导致闪退 @je5442804 <br>
	9、空间测绘功能去除BinaryEdge @lzj242 <br>
	10、JsFinder导出html时数据缺失 @xxxx1a <br>
<br>
<b> v2.8.1版 【2025.05.16】 </b>  <br>
	1、jwt编码兼容数组型payload @root1010jk <br>
	2、RC4解码时Base64转换导致错误 @eleveni386 <br>
	3、资产测绘功能高级配置指定hearder无效 @RMAX2000 <br>
	4、TscanClient修复端口扫描指纹识别异常 @菜 <br>
	5、TscanClient支持IP:Port形式 @Backspace <br>
	6、445端口的smb和ms-ds服务区分 @XingHuoLiaoYuanBaby <br>
	7、增加HTTP响应包最大长度限制选项 @秋茶- <br>
	8、Poc查看数据包增加一键复制 @菜狗 <br>
	9、启发式扫描时IP排除不生效 @LiPaCai <br>
	10、资产分拣时对IP段自动解析 @行者无疆 <br>
<br>
<b> v2.8.0版 【2025.05.07】 </b>  <br>
	1、优化线程动态调整策略 @小白 <br>
	2、新增113个内置poc @浮生若梦 <br>
	3、导出数据支持xls和html两种 @Afrog <br>
	4、修改任务持续时间为1h2m3s格式 @菜 <br>
	5、JWT破解字典更新 @amoy6228 <br>
	6、Shodan自定义查询存在bug @Hem1ock <br>
	7、Poc结果直接显示PocUrl和状态码 @秋茶- <br>
	8、端口扫描时支持!port以便排除端口 @minghuinet <br>
	9、导出数据增加Url屏幕截图 @菜鸟的菜 <br>
	10、红队命令等数据UI展示不完整 @Yo皮蛋 <br>
<br>
<b> v2.7.9版 【2025.05.01】 </b>  <br>
	1、前端页面布局调整增加TitleBar <br>
	2、密码破解支持UDP协议探测 @beauty <br>
	3、多重验证的poc数据包显示异常 @热河 <br>
	4、多个任务可同时执行重新扫描 @朱瀚声 <br>
	5、Host碰撞中ip资产的启发式探测bug @Anthony <br>
	6、Key数据类型错误导致校验异常 @候鸟 <br>
	7、40xbypass功能优化及文件统一处理 @小白 <br>
	8、poc导出excel增加响应请求数据 @秋茶- <br>
	9、Client数据库部分数据未记录 @张朝 <br>
	10、导出路径不存在导致导出失败 @soevai <br>
<br>
<b> v2.7.8版 【2025.04.23】 </b>  <br>
	1、代理池增加无限轮询模式 @dtset001 @秋茶- <br>
	2、Smb密码破解异常导致闪退 @je5442804 <br>
	3、Mongodb密码破解存在误报 @DreAm <br>
	4、主程序内置部分红队配置文件 @Superhero-zero <br>
	5、GUI界面的输入框取消自动大写检查 @perlh <br>
	6、TP5指纹规则完善及指纹匹配优化 @xintianwen <br>
	7、Poc中toUpper规则完善 @zysanjing <br>
	8、对C段进行密码破解时出现闪退 @L-Serim @cf48rty0 <br>
	9、Client存活探测np存在bug  @小刘小刘开心加油 <br>
	10、Poc检测支持主动指纹 @秋茶- <br>
<br>
<b> v2.7.7版 【2025.04.17】 </b>  <br>
	1、支持ipv6扫描 @呱呱 @Dawn @이 소 <br>
	2、优化启发式扫描进度估算 @kylinsec <br>
	3、修改Client校验策略 @小白 <br>
	4、目录枚举针对403结果优化 @Yo皮蛋 <br>
	5、目录枚举增加waf检测选项 @秋茶- <br>
	6、密码生成内存占用较高 @:-) @lsota1 <br>
	7、端口探测线程优化 @kylinsec <br>
	8、资产测绘采集页数显示异常 @Tomorrow @按时睡觉 <br>
	9、创建项目时空间测绘根据配置选取 @山西哥谭小丑 <br>
	10、Url检测功能显示网页缩略图 @King <br>
<br>
<b> v2.7.6版 【2025.04.06】 </b>  <br>
	1、目录枚举模块bug修复及算法增强 @无先森 <br>
	2、jwt破解功能存在bug @秋分 <br>
	3、表格复选框增加全选和当前页 @n0rth_404 <br>
	4、代理池自动爬取存在bug @秋茶- @addnetghost <br>
	5、代理池校验时禁用自定义header @秋茶-  <br>
	6、域名枚举时未开poc但仍会poc检测 @bpfmili <br>
	7、端口扫描支持IP:PORT格式 @lant1s <br>
	8、go-webview2版本回退 @Zxc123456zxc @ZMinGood <br>
	9、thinkphp:5.0.20 POC完善 @RuoJi6 <br>
	10、客户端修改默认mod选项 @小白 <br>
<br>
<b> v2.7.5版 【2025.04.01】 </b>  <br>
	1、增加大网段启发式扫描 @xxsmile123 <br>
	2、优化UDP端口扫描精准度 @💪 <br>
	3、客户端进度条优化 @涅槃 <br>
	4、修复nocolor参数无颜色输出 @涅槃 <br>
	5、创建项目时异常提醒 @ZMinGood <br>
	6、IP归属查询增加解析主域名选项 @秋茶- <br>
	7、Redis连接验证功能bug @涅槃 <br>
	8、jwt功能个别token检验失败 @秋分 <br>
	9、端口探测线程优化 @kylinsec <br>
	10、hunter自定义查询语句报错 @秋茶- <br>
<br>
<b> v2.7.4版 【2025.03.21】 </b>  <br>
	1、内网代理验证存在Bug @P1rc4 @CSeroad <br>
	2、Client多个bug @秋茶- @小刘小刘开心加油  <br>
	3、Bypass功能Auth编码bug @Aliak15 <br>
	4、目录扫描字典更新及进度条bug @无先森 <br>
	5、WMI密码爆破报错 @秋茶- @魚丸 <br>
	6、Poc增加“指纹不匹配时不扫描”选项 @秋茶- <br>
	7、第三方代理api导入方案 @zlj <br>
	8、增加自定义端口选项 @weisir1 <br>
	9、增加部分自定义红队命令 @RuoJi6 <br>
	10、Virustotal接口限额调整 @gniuy <br>
<br>
<b> v2.7.3版 【2025.03.12】 </b>  <br>
	1、密码爆破功能闪退 @-A1ert @涅槃 @fuz2 <br>
	2、代理地址删除 @小刘小刘开心加油 <br>
	3、空间测绘0.zone查询异常 @无忧 <br>
	4、代理验证时内网代理提示无效 @CSeroad <br>
	5、单个目标时遇到waf提醒 @小白 <br>
	6、创建项目同时提示两次 @山西哥谭小丑 <br>
	7、IP扫描时对目标中的域名解析IP后去重 @按时睡觉 <br>
	8、SM2解密时ASN.1编码bug @岁月静好 <br>
	9、JWT破解存在Bug @pplayerr @joonk685 <br>
	10、客户端存在Xss漏洞 @gniuy <br>
<br>
<b> v2.7.2版 【2025.02.18】 </b>  <br>
	1、代理池增加根据关键词切换代理 @Dawn <br>
	2、增加MQTT端口破解功能 <br>
	3、部分poc看不到数据包 @按时睡觉  <br>
	4、部分key校验提示异常 @杨帆起航 <br>
	5、新建项目资产测绘可多个目标 @按时睡觉 <br>
	6、空间测绘增加采集页数参数 @按时睡觉 <br>
	7、创建项目时可只保存后执行 @xhmcc <br>
	8、RSA解密增加pkcs8私钥解析 @dactar123 <br>
	9、导出excel数据异常 @xhmcc <br>
	10、空间测绘0.zone查询异常 @xintianwen <br>
<br>
<b> v2.7.1版 【2025.01.23】 </b>  <br>
	1、增加导出项目所有数据到Excel <br>
	2、代理池增加自动破解功能  <br>
	3、Url探测增加网页截图功能 @づ听风看月 <br>
	4、敏感目录字典更新 @无先森 <br>
	5、导入资产目标过多时前端卡死 @笑傲江湖 <br>
	6、资产导出excel文件名过长报错 @秋茶- <br>
	7、清空项目管理时40xBypass未清空 @Yo皮蛋 <br>
	8、项目管理扫描功能与基本功能开关存在冲突 @VBPush  <br>
	9、自定义POC选择后无法保存生效 @。 <br>
	10、代理启动后即可显示当前代理ip @Dawn <br>
<br>
<b> v2.7.0版 【2025.01.18】 </b>  <br>
  	1、代理池可批量启用、禁用、删除等 @bupsdx  <br>
  	2、代理池显示当前代理IP及手工切换 @xiaoliusec @Dawn <br>
  	3、bypass线程异常导致闪退 @Dawn <br>
  	4、因map重新顺序导致Jwt编码异常 @披着羊皮的狼 <br>
  	5、Base64解码方式不同导致jwt解码异常 @L1ech0  <br>
  	6、POC联动时可选择使用内置+外置 @xhmcc <br>
  	7、目录枚举功能时间间隔选项无效 @จุ๊บ <br>
  	8、POC和密码破解右键增加单条删除 @xhmcc <br>
  	9、VNC和CS密码本去除花括号 @fuz2 <br>
  	10、xray配置错误导致秒结束 @秋茶- <br>
<br>
<b> v2.6.9版 【2025.01.10】 </b>  <br>
  	1、Zoomeye接口API升级到v2版 <br>
  	2、JsFinder功能和展示优化 @呱呱 <br>
  	3、资产分拣时主域名.do误报 @xhmcc <br>
  	4、配置Apikey和验证时提示相同 @cream-sec <br>
  	5、密码生成社工字典闪退 @goodplay @Xxinbbyy <br>
  	6、Poc初始化时会默认访问ceye @Cream <br>
  	7、代理地址自动添加和下拉可选 @小白 <br>
  	8、默认项目清理资产后有残留数据 @行者无疆 <br>
  	9、资产分拣功能完善和优化 @xhmcc @Dawn <br>
  	10、端口扫描增加过滤打印机选项 @kk <br>
<br>
<b> v2.6.8版 【2025.01.06】 </b>  <br>
  	1、部分web指纹优化完善 @涅槃 <br>
  	2、项目管理排序修改为倒序排序 @sutdent1 <br>
  	3、域名枚举web相关全局代理可用 @A 阿宏 <br>
  	4、jwt字典可以自定义修改 @LiChaser <br>
  	5、Poc检测增加时间间隔选项 @8201 <br>
  	6、密码猜解部分服务线程优化 @sqy <br>
  	7、目录枚举302跳转导致误报 @山西哥谭小丑 <br>
  	8、支持SMB空口令连接 @小胖 <br>
  	9、资产分拣增加过滤内网功能 @我的名字回不来了！！！ <br>
  	10、Poc搜索前端UI优化 @sonumb-z <br>
<br>
<b>v2.6.7版 【2024.12.25】</b>  <br>
  	1、各功能在使用代理前先验证可用性 @小白 <br>
  	2、端口扫描时代理功能异常 @King <br>
  	3、Url检测前后台数据同步bug @秋茶- <br>
  	4、增加失败url查看功能 @秋茶- <br>
  	5、修复代理池重复循环bug @づ听风看月 <br>
  	6、Fofa兼容不同权限用户 @Qq1111111111 <br>
 <br>
<b>v2.6.6版 【2024.12.22】</b>  <br>
  	1、空间测绘功能增加查询语法聚合  <br>
  	2、破解密码功能内置和自定义字典切换bug @秋茶- <br>
  	3、JSFINDER功能目标地址显示异常 @呱呱🥝 <br>
  	4、网卡选择不同页面间同步 @魚丸 <br>
  	5、Go版本导致的个别站点url探测异常 @山西哥谭小丑 <br>
  	6、个别内置Poc检测误报较高 @kio <br>
  	7、端口策略选择存在bug @1024548219 <br>
  	8、代理池数据异常和提示异常 @阿宏 <br>
  	9、密码破解"仅破解一个账号"选项无效 @charis3306 <br>
  	10、红队命令OS类型显示重复选项 @cream-sec <br>
 <br>
<b>v2.6.5版 【2024.12.18】  </b>	 <br>
	1、增加代理池管理功能  <br>
	2、支持http和socks的代理Listener功能 <br>
	3、支持单个和批量添加，支持身份认证功能 <br>
	4、可从fofa、hunter、quake等自动抓取代理 <br>
	5、可对代理进行批量有效性验证 <br>
	6、可手工设置代理验证网站和关键词 <br>
	7、支持5种代理场景，如轮询、次数、时长等 <br>
	8、失败累计3次的代理可自动删除 <br>
	9、没有可用代理时会自动关闭代理接口 <br>
	10、支持单个代理管理及导出功能 <br>
 <br>
<b>v2.6.4版 【2024.12.12】 </b>  <br>
	1、增加中英文语言切换功能 <br>
	2、硬件校验时兼容多种系统命令 @CyangN <br>
	3、Url包含特殊字符时报错闪退 @秋茶- @hunmeng123 <br>
	4、Config初始化完成时增加前端提示 @小白 <br>
	5、部分站点jsfinder爬取较慢 @山西哥谭小丑 <br>
	6、Memcache命令stats更正 @Derrrry @澍小夏 <br>
	7、qqwry文件下载后可直接加载 @qingchenhh  <br>
	8、“密码破解”增加IP有效性验证 @hkylin <br>
	9、Linux下版本升级无效 @Finback  <br>
	10、Jsfinder功能针对vue站点爬取进行优化 @零乱 <br>
 <br>
<b>v2.6.3版 【2024.12.04】 </b>  <br>
	1、高级配置-增加多网卡选择功能 @小刘小刘开心加油 <br>
	2、目录枚举时单目标支持路径级中断 @EatKfcV50 <br>
	3、密码破解功能支持记录上次服务选项 <br>
	4、目录枚举时默认请求头导致漏报 @づ听风看月 <br>
	5、高级配置-修复随机UA设置无效  <br>
 <br>
<b>v2.6.2版 【2024.11.26】 </b>  <br>
	1、空间测绘模块增加0.zone接口 @Niko <br>
	2、全局代理开启时空间测绘模块可代理 <br>
	3、配置文件更新时文件名包含中文导致异常 <br>
	4、目录扫描web超时设置无效 @chencicici @VBPush <br>
	5、资产测绘中ICP备案查询语法修订 @ysdxj  <br>
	6、JWT破解功能增加支持none算法 @nonu11  <br>
	7、资产测绘自定义语句转义问题 @qty567  <br>
	8、红队命令特殊字符显示异常 @sourcexu7  <br>
	9、POC检测导出Excel标题错行 @Derrrry <br>
	10、修复个别资产测绘引擎检索语句 <br>
	11、资产分拣功能增加对逗号分割的处理 @Derrrry <br>
	12、编解码模块增加key和iv的格式选择 @あくま <br>
 <br>
<b>v2.6.1版 【2024.11.21】</b>  <br>
	1、增加300多个xray和afrog自定义poc @rain <br>
	2、单ip有防护时可能存在误报 @忘年忘义振于无竟 @阿宏 <br>
	3、新建项目时保存任务选项为默认参数 @Evi10x01 <br>
	4、敏感目录字典更新 @无先森 <br>
	5、密码破解中的mssql协议问题 @一根胡萝卜 <br>
	6、SM2解密时可能闪退 @零乱 <br>
	7、资产分拣时增加内外网资产排序 @文欧 <br>
	8、js中部分敏感字符未匹配 @Evi10x01 <br>
	9、去除fofa的1000条限制 @Y. <br>
	10、导出目录设置无效 @秋分 <br>
 <br>
<b>v2.6版 【2024.10.18】</b>  <br>
	1、增加程序自动更新功能 <br>
	2、知识星球用户的key可无限续期 <br>
	3、密码破解结果增加连接功能 <br>
	3、单个Poc扫描时进度显示异常 @山西哥谭小丑  <br>
	4、JsFinder“仅展示本站”匹配主域名  @山西哥谭小丑 <br>
	6、目录枚举遇到waf时跳过检测 @呱呱🥝 <br>
	7、主动指纹识别后Url可直接跳转 @づ听风看月 <br>
	8、SM2加解密都需要公钥私钥 @omegazero01  <br>
	9、资产分拣中针对edu.cn的处理 @Niko <br>
	10、IP扫描增加超时时间设置 @小啸 <br>
	11、JsFinder数据量过多时前端卡顿 @山西哥谭小丑  <br>
	12、清除数据后目标资产仍存在 @圣男 <br>
	13、Default项目清空后资产仍在 @山西哥谭小丑 <br>
	14、主动指纹探测中路径拼接存在Bug @guyan <br>
	15、切换项目后扫描状态变为“继续” @李 <br>
	16、清除记录后前端数据有留存 @Wans <br>
	17、自动更新页面增加手动按钮 @づ听风看月 <br>
	18、目录枚举存活模式下POST无效 @1204554617 <br>
	19、Mac_Arm自动更新报错 @大反派 @老梁 @蜉蝣 <br>
	20、域名枚举增加自定义DNS选项 @无忧 <br>
	21、第三方poc工具自定义扫描参数 @FanerAce  <br>
	22、域名枚举功能增加banner排序 @狐狸 <br>
	23、空间测绘支持自定义语法 @张召 <br>
	24、目录枚举导出excel列内容交叉 @Acczdy <br>
	25、Quake空间测绘可自定义获取数据量 @xjp08 <br>
 <br>
<b>v2.5版 【2024.09.15】</b>  <br>
	1、重构端口扫描模块，效率提升2-3倍 <br>
	2、针对Linux增加配置文件备份功能  <br>
	3、资产分拣支持Ipv6 @. <br>
	4、全屏模式下数据显示适配 @菜 <br>
	5、修复Linux的Key认证问题 @Narcissus <br>
	6、Mac下程序图标美化 @大反派 <br>
	7、功能联动时Poc检测占用资源较高 @sutdent1 <br>
	8、识别不到指纹时端口不显示 @A1 <br>
	9、非默认端口时功能联动无效 @山西哥谭小丑 <br>
	10、Redis爆破成功显示未授权 @Black @山西哥谭小丑  <br>
	11、LDAP密码破解误报 @Aholic_sec <br>
	12、Poc检测目标带子目录问题 @零乱 <br>
	13、Socks5代理保存时自动小写 @restart <br>
	14、输出log路径不存在时报错 @哥斯拉Yvan <br>
	15、项目名称支持中文 @菜狗 <br>
	16、445端口指纹识别闪退 @魚丸 <br>
	17、Afrog扫描时进度异常 @T-T <br>
	18、增加端口扫描线程数提醒 @小啸 <br>
	19、MSSQL联动时无法触发弱口令破解 @李 <br>
	20、第三方Poc工具无法匹配poc时全扫 @Atirds <br>
 <br>
<b>v2.4版 【2024.09.01】</b>  <br>
	1、IP扫描大量目标时可能导致闪退 <br>
	2、增加webshell笔记功能 @chencicici  <br>
	3、各种webshell免杀马 @CSeroad  <br>
	4、目录枚举时状态码过滤bug @Azure <br>
	5、Poc列表显示问题 @Xxinbbyy @澍小夏  <br>
	6、Poc多次检索后数据异常 @Ashthes @TXC <br>
	7、Bypass功能UA、fuzz测试bug @45 <br>
	8、Quake空间测绘数据异常 @按时吃饭 <br>
	9、密码爆破内存占用优化 @yehao1991  <br>
	10、Twj秘钥爆破算法优化 @xxsmile123 <br>
	11、优化密码破解漏报问题 <br>
	12、3389密码破解闪退问题 @yehao1991 <br>
	13、优化主动指纹探测精准度 @文欧 <br>
	14、目录枚举页面相似度算法优化 <br>
	15、扫描结束时程序闪退 @j1dag @kkkyan @文欧 @按时吃饭 <br>
	16、资产分拣内网IP分类排序 @xxsmile123 <br>
	17、密码破解多个账户问题 @b2522  <br>
	18、杀软查询及敏感目录字典更新 <br>
	19、第三方poc工具线程数设置 @Cx330才 <br>
	20、右键查看数据包异常及编码Bug @魚丸 <br>
 <br>
<b>v2.3版 【2024.08.12】</b>  <br>
	1、升级Go+Wails框架版本 <br>
	2、增加程序日志功能 <br>
	3、根据系统资源占用动态调整线程数 @1337Player <br>
	4、密码破解可自定义字典	 <br>
	5、wmi服务密码爆破闪退  @按时吃饭 <br>
	6、敏感目录字典更新 @无先森  <br>
	7、程序代码加固 @Again @看我扭转万象 <br>
	8、杀软识别不全面bug  @Yo皮蛋 <br>
	9、杀软识别特殊字符报错 @づ听风看月 <br>
	10、前端部分列内容增加排序 @按时吃饭 @づ听风看月 <br>
	11、目录枚举添加标题和排序 <br>
	12、Ip库加载失败导致闪退 @guyan <br>
	13、第三方poc工具Stop后会继续扫描 @LittleMoonhub  <br>
	14、项目执行进度卡在url检测  @大反派 <br>
	15、密码破解进程优化 @Aholic_sec <br>
	16、针对Hunter增加自定义查询页码  @文欧 <br>
	17、优化空间探测的资产去重功能 <br>
	18、sm4解密时处理hex格式bug @. <br>
	19、4xxBypass增加查看数据包功能 @呱呱 <br>
	20、Bypass修复Stop功能 @菜 @MTY123-YF <br>
	21、Log日志太大导致闪退 @Y. <br>
	22、目录扫描导致DB文件过大 @Azure <br>
	23、使用vpn可能导致认证失败 @鼎级FW <br>
	24、下载命令自定义保存bug @Xxinbbyy <br>
	25、修改红队命令、下载命令保存格式 <br>
 <br>
<b>v2.2版 【2024.07.22】</b>  <br>
	1、增加Host碰撞功能 @Baal  <br>
	2、增加40xBypass检测功能  <br>
	3、增加Jwt破解和加解密功能 @yhy <br>
	4、增加Vip认证(可解锁所有Poc) <br>
	5、增加IP归属地查询功能 <br>
	6、增加指纹策略，可根据需求选择不同指纹库 <br>
	7、新目录下程序无法启动bug @T-T <br>
	8、Telnet蜜罐出现误报情况 @. <br>
	9、配置文件重置时会先自动备份 <br>
	10、Poc输出日志改为倒序 @魚丸 <br>
	11、查看Poc数据包调整到右键菜单 @wuha <br>
	12、增加一键Hash识别功能 @Scappy <br>
	13、JsFinder个别链接爬不出js @古心静典  <br>
	14、针对hunter可自定义API地址 @starscow <br>
	15、RDP爆破多线程误报问题 @ℍℤ <br>
	16、端口策略显示问题 @slack @. <br>
	17、红队命令模块能加编辑功能 @1 <br>
	18、资产分拣匹配国外域名 @倏尔 <br>
	19、目录字典不存在时扫描闪退 @Xxinbbyy <br>
	20、恢复扫描可能导致数据重复 @鼎级FW <br>
	21、针对Mac/Linx增加Ulimit设置 <br>
	22、新建项目时出现重复项目数据 @Evi10x01 @大反派 <br>
	23、目录扫描时对目录前缀"/"进行处理 @转身遇见 <br>
	24、Jwt破解及显示bug @cloud- @大反派 <br>
	25、qqwry库文件缺失提醒 @xxsmile123 <br>
	26、资产提取匹配xyz等域名 @肖肖乐  <br>
	27、poc闪退问题 @老梁 @望天 <br>
	28、poc检测存在误报  @J1wa @Hem1ock <br>
	29、目录扫描针对特殊站点的跳转bug @づ听风看月 <br>
	30、Key认证bug @SinkO @Xxinbbyy @朱瀚声 @이 소 <br>
 <br>
<b>v2.1版 【2024.07.01】</b>  <br>
	1、支持自定义被动指纹添加 @Dawn <br>
	2、程序中断或Stop后可恢复之前扫描 @鼎级FW @陳 @涅槃 <br>
	3、项目状态显示Bug @方糖 @望天 @DouLiYouTang31 <br>
	4、导出资产excel中高危标红 @zlj <br>
	5、可支持自定义的header @Azure @涅槃 <br>
	6、AES解密iv类型的自动化判断 @Wans <br>
	7、主动指纹部分情况存在误报  @鼎级FW <br>
	8、Windows移动程序目录导致无法启动 @Black <br>
	9、RDP密码破解存在闪退情况 @Black <br>
	10、高级配置中增加"导出文件后打开"选项 @鼎级FW <br>
	11、POC检测结果最后一行会被遮住  @魚丸 <br>
	12、Default项目可一键清空 @步行街 <br>
	13、调用外部Poc工具时线程优化 @0x4C79 <br>
	14、资产测绘查c段导出excel存在Bug @我该叫什么 <br>
	15、增加文本转\x \u \o等多种编码 @cloud- <br>
	16、修复WMI弱口令误报Bug  @涅槃 @步行街 <br>
	17、密码查询功能添加新密码Bug @fitzxxx <br>
	18、密码破解发现未授权时的处置  @💪      <br>
	19、空间测绘可批量探测url存活 @季風吹向大海คิดถึง <br>
	20、个别网站标题存在乱码情况 @ki10Moc <br>
 <br>
<b>v2.0版 【2024.06.16】（包含了部分v1.9.1版修复的bug</b>） <br>
	1、增加编解码功能，支持36种编解码、加解密、哈希等 <br>
	2、针对445端口增加MS17010检测  <br>
	3、Nuclei自定义poc智能匹配Bug @陈皮老四 <br>
	4、敏感目录字典更新 @无先森  <br>
	5、主动指纹探测的误报问题 @望天 @🇯 <br>
	6、Url探测检索及清除记录bug @零乱 <br>
	7、资产分拣的收缩模式和C段分拣 @鼎级FW @猫哥 <br>
	8、Poc检测增加漏洞等级标识 @放飞梦想จุ๊บ <br>
	9、Poc检测流程优化 @zlj <br>
	10、空间测绘标签页批量关闭 @季風吹向大海คิดถึง  <br>
	11、设置hunter最多查询页数5 @Evi10x01 <br>
	12、破解字典空口令bug @Darkid_98 <br>
	13、修复ip扫描端口策略 @-A1ert <br>
	14、Poc检索前端bug @魚丸 <br>
	15、空间测绘查询Tab混乱bug @澍小夏 @大反派 <br>
	16、端口指纹选项关闭时资产不显示 @张召 <br>
	17、联动密码破解时覆盖所有服务及提示Bug  @鼎级FW <br>
	18、pop3协议密码爆破bug  @Azure <br>
	19、端口扫描时Socks5代理问题 @张召 <br>
	20、调用nuclei和xray可使用代理扫描  @魚丸 <br>
 <br>
<b>v1.9版 【2024.05.28】</b>  <br>
	1、增加指纹探测规则8327条，总计51873条 <br>
	2、远程下载非核心配置文件缩减体积 <br>
	3、密码破解成功后进行指纹识别  <br>
	4、敏感目录字典更新 @无先森  <br>
	5、增加多个密探工具的目录字典 @kkbo <br>
	6、增加主动指纹探测并可自定义 @@huclilu <br>
	7、整合优化多个cms指纹 @Dawn @wlaq-su @ @RL <br>
	8、excel导出bug修复 @无先森 <br>
	9、web密码破解异常退出bug @鼎级FW <br>
	10、Mysql密码破解bug @xiaojj2021 <br>
	11、Tomcat破解异常 @ℍℤ @我的名字回不来了！！！ <br>
	12、SSH服务爆破异常 @哈哈 <br>
	13、网络测绘C段标签命名bug @澍小夏 <br>
	14、集成xray2.0外置Poc并智能匹配 @kio <br>
	15、配置选项中的UA设置 @yuwan-jpg  <br>
	16、文件导入时兼容CRLF @烧烤老师傅 <br>
	17、poc检测模块可右键复制PocUrl @六六 <br>
	18、密码字典自动更新及一键更新bug @鼎级FW <br>
	19、路由器telnet爆破bug  @. <br>
	20、Oracle爆破异常 @我的名字回不来了！！！ <br>
	21、测绘资产-目录扫描时暂停出现闪退 @Azure <br>
	22、Url扫描支持web无协议扫描 <br>
	23、只选外置poc时的队列问题  @hunmeng123 <br>
	24、空间测绘支持批量检索 @辞忧 <br>
	25、社工字典生成优化 @ymbzd <br>
 <br>
<b>v1.8版 【2024.05.01】</b>  <br>
	1、密码破解功能完善及多线程优化 <br>
	2、资产较多时的前端响应优化 <br>
	3、多个敏感目录字典更新 @无先森 <br>
	4、内置多个目录字典并自动释放到目录 @无先森 <br>
	5、资产分拣功能优化及bug修复  @xxsmile123 <br>
	6、增加RTSP端口破解功能 @づ听风看月 @hunmeng123   <br>
	7、反弹shell和cs上线IP保存 @Evi10x01 <br>
	8、项目漏洞详情展示 @WasteMaterial @Evi10x01 <br>
	9、Hunter查询接口优化 @鼎级FW <br>
	10、Quake查询接口优化 @lwjdsgz <br>
	11、空间测绘增加icp备案查询 @Evi10x01 <br>
	12、密码破解联动功能Bug修复 @Evi10x01 @鼎级FW <br>
	13、端口扫描可根据服务进行爆破  @jisanlong <br>
	14、自定义Poc显示bug @Phonk <br>
	15、url探测存在卡顿情况 @rkabyss <br>
	16、结果日志输出bug @季風吹向大海คิดถึง  <br>
	17、任务联动时地址栏显示Bug  <br>
	18、密码破解闪退bug修复 @鼎级FW <br>
	19、密码破解支持协议://IP:Port格式 <br>
	20、爆破功能自定义字典bug @wvykey <br>
 <br>
<b>v1.7版 【2024.04.16】</b>  <br>
	1、Poc检测可直接调用Nuclei、Xray、Afrog @J1wa @无先森    <br>
	2、增加自定义poc功能  <br>
	3、在高级选项中增加自定义主题模式 <br>
	4、IP扫描时会先探测是否存在防火墙  <br>
	5、增加资产分拣功能 @xxsmile123 <br>
	6、优化更新账号和密码字典 @那个少年 <br>
	7、优化自定义账号密码功能 @DeEpinGh0st <br>
	8、自定义配置目录、导出目录等 @づ听风看月 @蜉蝣 <br>
	9、修复项目管理若干Bug  @无先森 @Evi10x01 <br>
	10、敏感目录字典更新 @无先森 <br>
	11、Fofa自定义api地址 @Tian @季風吹向大海คิดถึง  <br>
	12、项管理添加进度状态展示 <br>
	13、UrlFinder功能优化完善及bug修复 @A1 <br>
	14、强化Url敏感信息检索功能 @xxsmile123 <br>
	15、密码破解功能优化完善 @步行街 @endin9 @Y. <br>
	16、Banner标红资产自动排序 @Evi10x01 <br>
	17、部分指纹精确度优化 @Black @倏尔 @高歌 <br>
	18、目录扫描自定义字典bug @Evi10x01 <br>
	19、项目任务中的目录枚举功能优化 @鼎级FW <br>
	20、项目任务自定义字典功能优化  <br>
 <br>
<b>v1.6版 【2024.03.25】</b>  <br>
	1、增加项目管理流程，增强各功能模块联动 <br>
	2、使用数据库可对所有功能和数据进行增删改查 <br>
	3、添加js爬取功能及js敏感信息匹配 @onewinner  @无先森 <br>
	4、敏感目录字典更新 @无先森 <br>
	5、配置代理增加前端校验 @WangGang <br>
	6、目录枚举Ext及3xx跳转优化 @无先森 @转身遇见 <br>
	7、网络空探导出所有tab到一个excel @Evi10x01 <br>
	8、优化代理设置模块，完善校验和提示 @一口蛋黄苏 <br>
	9、密码破解端口修改只能输一位 @nuanfeng1yue @💪 @零乱 @清风拂杨柳 <br>
	10、端口扫描增加只探测存活选项 @Wans @Black <br>
	11、poc检测增加Log模块  <br>
	12、URL探测联动功能bug  @Evi10x01	 <br>
	13、IP端口扫描时闪退问题 @xxsmile123 @Thron_bird <br>
	14、空间测绘添加body、证书、ICON检索  @Tian <br>
	15、空间测绘右键添加继续查询标题、ip、域名等  @Tian <br>
	16、生成字典枚举模式闪退 @咕噜咕噜 <br>
 <br>
<b>v1.5版 【2024.03.01】</b>  <br>
	1、目录枚举超链接bug @无先森 @Google_Hacking <br>
	2、扫描目标过多时，点击终止后会继续扫描 @行者无疆 <br>
	3、增加一键检测ApiKey可用性功能 @Dawn <br>
	4、枚举模式生成字典会异常退出  @无先森 <br>
	5、大量数据时前端会有卡顿 @零乱 @Mr.Right @impdx <br>
	6、指纹识别中hostname乱码问题 @hunmeng123 @2gggggg <br>
	7、AV识别数据库更新 @pei <br>
	8、网络空间测绘增加url跳转及优化  @づ听风看月 @80576560 <br>
	9、Mac深色Url超链接样式优化 @下完雪🍁 <br>
	10、FofaApi接口权限bug @Bains @💪 <br>
	11、多次查询时Tab数据可能覆盖 @J1wa <br>
	12、导出excel时报错 @Huck-Lim  <br>
	13、空间测绘VT平台数据回传问题 @Evi10x01 <br>
	14、密码破解log无法清除 @sq565163 <br>
	15、个别网站标题乱码问题 @Dawn <br>
	16、支持自定义添加红队命令 @Lelylsj  <br>
	17、支持自定义设备密码  @Sharlong-Wen <br>
	18、优化端口、URL的检索功能 @xxxxl🐾 <br>
	19、配置文件版本号同步 @づ听风看月 <br>
	20、配置cookie未生效 @bupsdx <br>
 <br>
<b>v1.4版 【2024.02.18】</b>  <br>
	1、增加网络空间探测功能模块，内置9种常见空间探测API <br>
	2、目录枚举功能进行字典优化和重分类 @无先森  <br>
	3、消息窗口不消失 @J1wa  @Hhhnee <br>
	4、空间探测平台api接口协助 @Grit <br>
	5、增加目录枚举递归限制，默认3层 @Google_Hacking <br>
	6、目录枚举过滤指定长度、关键字，自定义后缀  @无先森 <br>
 <br>
<b>v1.3版 【2024.01.22】</b>  <br>
	1、增加密码生成功能，内置三种生成模式 <br>
	2、增加设备弱口令查询功能，内置1.1万条记录 <br>
	3、新增分页功能，并可跨页面进行多选 <br>
	4、目录扫描点击stop闪退 @转身遇见 @Google_Hacking <br>
	5、端口扫描兼容域名，及进度NaN的问题 @无先森   <br>
	6、精简优化扫描端口及超链接bug @xxxxl🐾 <br>
	7、自定义字典换行编码问题  @无先森 <br>
	8、域名泛解析问题 @无先森 <br>
	9、导出excel多一列及乱序bug @一起看雪 @南 <br>
	10、密码破解任务无法停止 @冰點  @T-T <br>
 <br>
<b>v1.2版 【2024.01.10】</b>  <br>
	1、增加子域名枚举、接口查询功能 <br>
	2、针对非web服务的指纹识别进行优化 <br>
	3、增加导出excel功能，完善更多右键功能 <br>
	4、实时保存数据到result.txt文件 <br>
	5、增加批量多选功能 @Dawn  @piaolingshusheng <br>
	6、修复目录枚举闪退 @Google_Hacking @Bains @LC <br>
	7、自定义密码框输入Bug @이 소 <br>
	8、导入字典数据显示错误 @转身遇见 <br>
	9、增加目录扫描递归选项 @onewinner  @T-T <br>
	10、扫描时的进度和存活数量问题  @💪  @龙猫爱吃鱼 <br>
	11、增加排序及相关过滤功能  @xg <br>
	12、大量Url时的闪退Bug @rtfghd @无先森 <br>
 <br>
<b>v1.1版 【2023.12.27】</b>  <br>
	1、新增加java命令编码，解决部分按钮无效 @Dawn  <br>
	2、修复windows ping扫描cmd窗口 @遥遥 @hunmeng123 <br>
	3、修复B段扫描时卡死情况 @Mr.Right <br>
	4、目录枚举同长度出现3次以上不再显示 @Bains  <br>
	5、自定义poc异常退出问题 @qtz777 @转身遇见 <br>
	6、修复路径字典错误、编码错误、前端校验错误 @遥遥 @TXC <br>
	7、重构目录枚举实现方式，效率提高10倍  <br>
	8、IP扫描和指纹识别同步进行  <br>
	9、Ip扫描、Url扫描增加状态栏 <br>
	10、密码破解时自定义字典无效问题	 <br>
 <br>
<b>v1.0版 【2023.12.21】 实现局部/全局、多类代理功能，正式版发布 </b><br>
<b>v0.9版 【2023.12.19】 实现各功能之间的任务联动及右键菜单联动</b>  </b><br>
<b>v0.8版 【2023.12.15】 增加版本更新检查、有效期校验、配置文件读写等</b>  <br>
<b>v0.7版 【2023.12.12】 辅助功能杀软查询、提权辅助完成 <br>
<b>v0.6版 【2023.12.10】 反弹shell、CS上线、下载命令、红队命令完成 </b><br>
<b>v0.5版 【2023.12.08】 目录枚举及Fuzz模式实现</b>  <br>
<b>v0.4版 【2023.11.29】 弱口令破解模块功能实现 </b><br>
<b>v0.3版 【2023.11.18】 Poc检测及Poc指纹匹配功能实现 </b><br>
<b>v0.2版 【2023.11.01】 Url扫描及web指纹精简功能实现 </b><br>
<b>v0.1版 【2023.10.23】 Ip及端口扫描、服务识别功能实现 </b><br>
<b>v0.0版 【2023.10.10】 TscanPlus架构选择及功能初步规划 </b><br>
    </td>
    <td style="width:50%; border:1px solid black; vertical-align:top; padding:10px;">
      <br><b>截至【2025.10.01】数据：</b>
<br><br>
<b>@秋茶-: 28个 </b><br><br>
<b>@无先森: 26个 </b><br><br>
<b>@小白: 15个 </b><br><br>
<b>@鼎级FW: 14个 </b><br><br>
<b>@Evi10x01: 14个 </b><br><br>
<b>@呱呱: 13个 </b><br><br>
<b>@Dawn: 12个 </b><br><br>
<b>@づ听风看月: 12个 </b><br><br>
<b>@山西哥谭小丑: 11个 </b><br><br>
<b>@xxsmile123: 8个 </b><br><br>
<b>@涅槃: 8个 </b><br><br>
<b>@魚丸: 8个 </b><br><br>
<b>@零乱: 7个 </b><br><br>
<b>@zzzhhha: 6个 </b><br><br>
<b>@菜鸟的菜: 6个 </b><br><br>
<b>@按时睡觉: 6个 </b><br><br>
<b>@.: 6个 </b><br><br>
<b>@xhmcc: 6个 </b><br><br>
<b>@大反派: 6个 </b><br><br>
<b>@文欧: 5个 </b><br><br>
<b>@Yo皮蛋: 5个 </b><br><br>
<b>@💪: 5个 </b><br><br>
<b>@Xxinbbyy: 5个 </b><br><br>
<b>@hunmeng123: 5个 </b><br><br>
<b>@Black: 5个 </b><br><br>
<b>@Azure: 5个 </b><br><br>
<b>@转身遇见: 5个 </b><br><br>
<b>@Y.: 4个 </b><br><br>
<b>@Wans: 4个 </b><br><br>
<b>@cf48rty0: 4个 </b><br><br>
<b>@菜: 4个 </b><br><br>
<b>@小刘小刘开心加油: 4个 </b><br><br>
<b>@澍小夏: 4个 </b><br><br>
<b>@T-T: 4个 </b><br><br>
<b>@按时吃饭: 4个 </b><br><br>
<b>@J1wa: 4个 </b><br><br>
<b>@季風吹向大海คิดถึง: 4个 </b><br><br>
<b>@Google_Hacking: 4个 </b><br><br>
<b>@雪山乘客: 3个 </b><br><br>
<b>@树先生: 3个 </b><br><br>
<b>@n0rth_404: 3个 </b><br><br>
<b>@A1: 3个 </b><br><br>
<b>@b2522: 3个 </b><br><br>
<b>@Backspace: 3个 </b><br><br>
<b>@kio: 3个 </b><br><br>
<b>@bupsdx: 3个 </b><br><br>
<b>@je5442804: 3个 </b><br><br>
<b>@行者无疆: 3个 </b><br><br>
<b>@이 소: 3个 </b><br><br>
<b>@kylinsec: 3个 </b><br><br>
<b>@秋分: 3个 </b><br><br>
<b>@CSeroad: 3个 </b><br><br>
<b>@zlj: 3个 </b><br><br>
<b>@我的名字回不来了！！！: 3个 </b><br><br>
<b>@Derrrry: 3个 </b><br><br>
<b>@张召: 3个 </b><br><br>
<b>@望天: 3个 </b><br><br>
<b>@步行街: 3个 </b><br><br>
<b>@Tian: 3个 </b><br><br>
<b>@Bains: 3个 </b><br><br>
<b>@Reluctantly: 2个 </b><br><br>
<b>@yhy: 2个 </b><br><br>
<b>@0x1eeA: 2个 </b><br><br>
<b>@笑傲江湖: 2个 </b><br><br>
<b>@一根胡萝卜: 2个 </b><br><br>
<b>@xiaoliusec: 2个 </b><br><br>
<b>@TFour123: 2个 </b><br><br>
<b>@amoy6228: 2个 </b><br><br>
<b>@太霖: 2个 </b><br><br>
<b>@KaerSAN: 2个 </b><br><br>
<b>@wuha: 2个 </b><br><br>
<b>@Pyl0ad: 2个 </b><br><br>
<b>@圣男: 2个 </b><br><br>
<b>@beauty: 2个 </b><br><br>
<b>@sonumb-z: 2个 </b><br><br>
<b>@Hem1ock: 2个 </b><br><br>
<b>@朱瀚声: 2个 </b><br><br>
<b>@xintianwen: 2个 </b><br><br>
<b>@King: 2个 </b><br><br>
<b>@ZMinGood: 2个 </b><br><br>
<b>@RuoJi6: 2个 </b><br><br>
<b>@gniuy: 2个 </b><br><br>
<b>@-A1ert: 2个 </b><br><br>
<b>@fuz2: 2个 </b><br><br>
<b>@无忧: 2个 </b><br><br>
<b>@VBPush: 2个 </b><br><br>
<b>@cream-sec: 2个 </b><br><br>
<b>@sutdent1: 2个 </b><br><br>
<b>@阿宏: 2个 </b><br><br>
<b>@Niko: 2个 </b><br><br>
<b>@chencicici: 2个 </b><br><br>
<b>@小啸: 2个 </b><br><br>
<b>@guyan: 2个 </b><br><br>
<b>@李: 2个 </b><br><br>
<b>@老梁: 2个 </b><br><br>
<b>@蜉蝣: 2个 </b><br><br>
<b>@Aholic_sec: 2个 </b><br><br>
<b>@TXC: 2个 </b><br><br>
<b>@yehao1991: 2个 </b><br><br>
<b>@ℍℤ: 2个 </b><br><br>
<b>@倏尔: 2个 </b><br><br>
<b>@cloud-: 2个 </b><br><br>
<b>@onewinner: 2个 </b><br><br>
<b>@Mr.Right: 2个 </b><br><br>
<b>@xxxxl🐾: 2个 </b><br><br>
<b>@遥遥: 2个 </b><br><br>
<b>@chlinfo404: 1个 </b><br><br>
<b>@天明: 1个 </b><br><br>
<b>@mk4no1: 1个 </b><br><br>
<b>@jo3ker: 1个 </b><br><br>
<b>@youxia5: 1个 </b><br><br>
<b>@TAI: 1个 </b><br><br>
<b>@nnasdlc: 1个 </b><br><br>
<b>@Easonc8: 1个 </b><br><br>
<b>@Seven: 1个 </b><br><br>
<b>@xj90512: 1个 </b><br><br>
<b>@shuai32768: 1个 </b><br><br>
<b>@缓归: 1个 </b><br><br>
<b>@陌上花开: 1个 </b><br><br>
<b>@孙吉国杰: 1个 </b><br><br>
<b>@faow: 1个 </b><br><br>
<b>@hellowchen: 1个 </b><br><br>
<b>@ZenkiH: 1个 </b><br><br>
<b>@nn0nkey: 1个 </b><br><br>
<b>@pemuse: 1个 </b><br><br>
<b>@@qty567: 1个 </b><br><br>
<b>@丶ty: 1个 </b><br><br>
<b>@z1603206931: 1个 </b><br><br>
<b>@ziyue0230: 1个 </b><br><br>
<b>@hello: 1个 </b><br><br>
<b>@momxSec: 1个 </b><br><br>
<b>@弹弹弹: 1个 </b><br><br>
<b>@Vain: 1个 </b><br><br>
<b>@jiuyueyi: 1个 </b><br><br>
<b>@Crab: 1个 </b><br><br>
<b>@X: 1个 </b><br><br>
<b>@xmqaq: 1个 </b><br><br>
<b>@J0k4r5: 1个 </b><br><br>
<b>@R: 1个 </b><br><br>
<b>@酒零: 1个 </b><br><br>
<b>@洋丞: 1个 </b><br><br>
<b>@fu221ng: 1个 </b><br><br>
<b>@15679768019: 1个 </b><br><br>
<b>@youcs233: 1个 </b><br><br>
<b>@雾散: 1个 </b><br><br>
<b>@jason9777598: 1个 </b><br><br>
<b>@ZACsec: 1个 </b><br><br>
<b>@贝贝: 1个 </b><br><br>
<b>@xiaridenuanfeng: 1个 </b><br><br>
<b>@totooss: 1个 </b><br><br>
<b>@曾哥: 1个 </b><br><br>
<b>@心海: 1个 </b><br><br>
<b>@Avalon: 1个 </b><br><br>
<b>@20812807: 1个 </b><br><br>
<b>@daryl888: 1个 </b><br><br>
<b>@NewGtBoy: 1个 </b><br><br>
<b>@瑶瑶: 1个 </b><br><br>
<b>@Mrship12138: 1个 </b><br><br>
<b>@fricka6768: 1个 </b><br><br>
<b>@0xFF: 1个 </b><br><br>
<b>@榆关: 1个 </b><br><br>
<b>@dafupp: 1个 </b><br><br>
<b>@echo-Shu: 1个 </b><br><br>
<b>@miki-java: 1个 </b><br><br>
<b>@lzj242: 1个 </b><br><br>
<b>@xxxx1a: 1个 </b><br><br>
<b>@root1010jk: 1个 </b><br><br>
<b>@eleveni386: 1个 </b><br><br>
<b>@RMAX2000: 1个 </b><br><br>
<b>@XingHuoLiaoYuanBaby: 1个 </b><br><br>
<b>@菜狗: 1个 </b><br><br>
<b>@LiPaCai: 1个 </b><br><br>
<b>@浮生若梦: 1个 </b><br><br>
<b>@Afrog: 1个 </b><br><br>
<b>@minghuinet: 1个 </b><br><br>
<b>@热河: 1个 </b><br><br>
<b>@Anthony: 1个 </b><br><br>
<b>@候鸟: 1个 </b><br><br>
<b>@张朝: 1个 </b><br><br>
<b>@soevai: 1个 </b><br><br>
<b>@dtset001: 1个 </b><br><br>
<b>@DreAm: 1个 </b><br><br>
<b>@Superhero-zero: 1个 </b><br><br>
<b>@perlh: 1个 </b><br><br>
<b>@zysanjing: 1个 </b><br><br>
<b>@L-Serim: 1个 </b><br><br>
<b>@:-): 1个 </b><br><br>
<b>@lsota1: 1个 </b><br><br>
<b>@Tomorrow: 1个 </b><br><br>
<b>@addnetghost: 1个 </b><br><br>
<b>@bpfmili: 1个 </b><br><br>
<b>@lant1s: 1个 </b><br><br>
<b>@Zxc123456zxc: 1个 </b><br><br>
<b>@P1rc4: 1个 </b><br><br>
<b>@Aliak15: 1个 </b><br><br>
<b>@weisir1: 1个 </b><br><br>
<b>@岁月静好: 1个 </b><br><br>
<b>@pplayerr: 1个 </b><br><br>
<b>@joonk685: 1个 </b><br><br>
<b>@杨帆起航: 1个 </b><br><br>
<b>@dactar123: 1个 </b><br><br>
<b>@。: 1个 </b><br><br>
<b>@披着羊皮的狼: 1个 </b><br><br>
<b>@L1ech0: 1个 </b><br><br>
<b>@จุ๊บ: 1个 </b><br><br>
<b>@goodplay: 1个 </b><br><br>
<b>@Cream: 1个 </b><br><br>
<b>@kk: 1个 </b><br><br>
<b>@A 阿宏: 1个 </b><br><br>
<b>@LiChaser: 1个 </b><br><br>
<b>@8201: 1个 </b><br><br>
<b>@sqy: 1个 </b><br><br>
<b>@小胖: 1个 </b><br><br>
<b>@Qq1111111111: 1个 </b><br><br>
<b>@1024548219: 1个 </b><br><br>
<b>@charis3306: 1个 </b><br><br>
<b>@CyangN: 1个 </b><br><br>
<b>@qingchenhh: 1个 </b><br><br>
<b>@hkylin: 1个 </b><br><br>
<b>@Finback: 1个 </b><br><br>
<b>@EatKfcV50: 1个 </b><br><br>
<b>@ysdxj: 1个 </b><br><br>
<b>@nonu11: 1个 </b><br><br>
<b>@qty567: 1个 </b><br><br>
<b>@sourcexu7: 1个 </b><br><br>
<b>@あくま: 1个 </b><br><br>
<b>@rain: 1个 </b><br><br>
<b>@忘年忘义振于无竟: 1个 </b><br><br>
<b>@omegazero01: 1个 </b><br><br>
<b>@1204554617: 1个 </b><br><br>
<b>@FanerAce: 1个 </b><br><br>
<b>@狐狸: 1个 </b><br><br>
<b>@Acczdy: 1个 </b><br><br>
<b>@xjp08: 1个 </b><br><br>
<b>@Narcissus: 1个 </b><br><br>
<b>@restart: 1个 </b><br><br>
<b>@哥斯拉Yvan: 1个 </b><br><br>
<b>@Student1: 1个 </b><br><br>
<b>@Atirds: 1个 </b><br><br>
<b>@Ashthes: 1个 </b><br><br>
<b>@45: 1个 </b><br><br>
<b>@j1dag: 1个 </b><br><br>
<b>@kkkyan: 1个 </b><br><br>
<b>@Cx330才: 1个 </b><br><br>
<b>@1337Player: 1个 </b><br><br>
<b>@Again: 1个 </b><br><br>
<b>@看我扭转万象: 1个 </b><br><br>
<b>@LittleMoonhub: 1个 </b><br><br>
<b>@MTY123-YF: 1个 </b><br><br>
<b>@Baal: 1个 </b><br><br>
<b>@Scappy: 1个 </b><br><br>
<b>@古心静典: 1个 </b><br><br>
<b>@starscow: 1个 </b><br><br>
<b>@slack: 1个 </b><br><br>
<b>@1: 1个 </b><br><br>
<b>@肖肖乐: 1个 </b><br><br>
<b>@SinkO: 1个 </b><br><br>
<b>@陳: 1个 </b><br><br>
<b>@方糖: 1个 </b><br><br>
<b>@DouLiYouTang31: 1个 </b><br><br>
<b>@0x4C79: 1个 </b><br><br>
<b>@我该叫什么: 1个 </b><br><br>
<b>@fitzxxx: 1个 </b><br><br>
<b>@ki10Moc: 1个 </b><br><br>
<b>@陈皮老四: 1个 </b><br><br>
<b>@J: 1个 </b><br><br>
<b>@猫哥: 1个 </b><br><br>
<b>@放飞梦想จุ๊บ: 1个 </b><br><br>
<b>@Darkid_98: 1个 </b><br><br>
<b>@kkbo: 1个 </b><br><br>
<b>@huclilu: 1个 </b><br><br>
<b>@wlaq-su: 1个 </b><br><br>
<b>@: 1个 </b><br><br>
<b>@RL: 1个 </b><br><br>
<b>@xiaojj2021: 1个 </b><br><br>
<b>@哈哈: 1个 </b><br><br>
<b>@yuwan-jpg: 1个 </b><br><br>
<b>@烧烤老师傅: 1个 </b><br><br>
<b>@六六: 1个 </b><br><br>
<b>@辞忧: 1个 </b><br><br>
<b>@ymbzd: 1个 </b><br><br>
<b>@WasteMaterial: 1个 </b><br><br>
<b>@lwjdsgz: 1个 </b><br><br>
<b>@jisanlong: 1个 </b><br><br>
<b>@Phonk: 1个 </b><br><br>
<b>@rkabyss: 1个 </b><br><br>
<b>@wvykey: 1个 </b><br><br>
<b>@那个少年: 1个 </b><br><br>
<b>@DeEpinGh0st: 1个 </b><br><br>
<b>@endin9: 1个 </b><br><br>
<b>@高歌: 1个 </b><br><br>
<b>@WangGang: 1个 </b><br><br>
<b>@一口蛋黄苏: 1个 </b><br><br>
<b>@nuanfeng1yue: 1个 </b><br><br>
<b>@清风拂杨柳: 1个 </b><br><br>
<b>@Thron_bird: 1个 </b><br><br>
<b>@咕噜咕噜: 1个 </b><br><br>
<b>@impdx: 1个 </b><br><br>
<b>@2gggggg: 1个 </b><br><br>
<b>@pei: 1个 </b><br><br>
<b>@80576560: 1个 </b><br><br>
<b>@下完雪🍁: 1个 </b><br><br>
<b>@Huck-Lim: 1个 </b><br><br>
<b>@sq565163: 1个 </b><br><br>
<b>@Lelylsj: 1个 </b><br><br>
<b>@Sharlong-Wen: 1个 </b><br><br>
<b>@Hhhnee: 1个 </b><br><br>
<b>@Grit: 1个 </b><br><br>
<b>@一起看雪: 1个 </b><br><br>
<b>@南: 1个 </b><br><br>
<b>@冰點: 1个 </b><br><br>
<b>@piaolingshusheng: 1个 </b><br><br>
<b>@LC: 1个 </b><br><br>
<b>@龙猫爱吃鱼: 1个 </b><br><br>
<b>@xg: 1个 </b><br><br> 
<b>@rtfghd: 1个 </b><br><br> 
<b>@qtz777: 1个 </b><br><br>
   </td>
  </tr>
</table>





[url-poc-key]: POC提交及无影Key获取说明.md

