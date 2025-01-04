

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

【2025.01.01】无影(TscanPlus)自2023年12月上线来，截止目前共发布25个版本，**增加/升级45项功能，累计修复192个用户反馈的376个Bug**，反馈Bug统计数据如下。

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
      <br><b>截至【2025.01.01】数据：</b>
<br><br>
<b>@无先森: 21个 <br><br></b>
<b>@Evi10x01: 14个 <br><br></b>
<b>@鼎级FW: 13个 <br><br></b>
<b>@づ听风看月: 11个 <br><br></b>
<b>@山西哥谭小丑: 9个 <br><br></b>
<b>@魚丸: 7个 <br><br></b>
<b>@零乱: 6个 <br><br></b>
<b>@大反派: 6个 <br><br></b>
<b>@xxsmile123: 6个 <br><br></b>
<b>@Dawn: 6个 <br><br></b>
<b>@hunmeng123: 5个 <br><br></b>
<b>@.: 5个 <br><br></b>
<b>@Black: 5个 <br><br></b>
<b>@Azure: 5个 <br><br></b>
<b>@转身遇见: 5个 <br><br></b>
<b>@涅槃: 4个 <br><br></b>
<b>@秋茶-: 4个 <br><br></b>
<b>@澍小夏: 4个 <br><br></b>
<b>@文欧: 4个 <br><br></b>
<b>@T-T: 4个 <br><br></b>
<b>@Xxinbbyy: 4个 <br><br></b>
<b>@按时吃饭: 4个 <br><br></b>
<b>@J1wa: 4个 <br><br></b>
<b>@💪: 4个 <br><br></b>
<b>@季風吹向大海คิดถึง: 4个 <br><br></b>
<b>@Google_Hacking: 4个 <br><br></b>
<b>@小白: 3个 <br><br></b>
<b>@Derrrry: 3个 <br><br></b>
<b>@Y.: 3个 <br><br></b>
<b>@Wans: 3个 <br><br></b>
<b>@张召: 3个 <br><br></b>
<b>@望天: 3个 <br><br></b>
<b>@步行街: 3个 <br><br></b>
<b>@Tian: 3个 <br><br></b>
<b>@Bains: 3个 <br><br></b>
<b>@呱呱🥝: 2个 <br><br></b>
<b>@kio: 2个 <br><br></b>
<b>@阿宏: 2个 <br><br></b>
<b>@Niko: 2个 <br><br></b>
<b>@chencicici: 2个 <br><br></b>
<b>@小啸: 2个 <br><br></b>
<b>@guyan: 2个 <br><br></b>
<b>@李: 2个 <br><br></b>
<b>@老梁: 2个 <br><br></b>
<b>@蜉蝣: 2个 <br><br></b>
<b>@菜: 2个 <br><br></b>
<b>@A1: 2个 <br><br></b>
<b>@Aholic_sec: 2个 <br><br></b>
<b>@TXC: 2个 <br><br></b>
<b>@yehao1991: 2个 <br><br></b>
<b>@ℍℤ: 2个 <br><br></b>
<b>@倏尔: 2个 <br><br></b>
<b>@cloud-: 2个 <br><br></b>
<b>@이 소: 2个 <br><br></b>
<b>@zlj: 2个 <br><br></b>
<b>@: 2个 <br><br></b>
<b>@我的名字回不来了！！！: 2个 <br><br></b>
<b>@onewinner: 2个 <br><br></b>
<b>@Mr.Right: 2个 <br><br></b>
<b>@xxxxl🐾: 2个 <br><br></b>
<b>@遥遥: 2个 <br><br></b>
<b>@A 阿宏: 1个 <br><br></b>
<b>@8201: 1个 <br><br></b>
<b>@sqy: 1个 <br><br></b>
<b>@小胖: 1个 <br><br></b>
<b>@King: 1个 <br><br></b>
<b>@Qq1111111111: 1个 <br><br></b>
<b>@1024548219: 1个 <br><br></b>
<b>@charis3306: 1个 <br><br></b>
<b>@cream-sec: 1个 <br><br></b>
<b>@CyangN: 1个 <br><br></b>
<b>@qingchenhh: 1个 <br><br></b>
<b>@hkylin: 1个 <br><br></b>
<b>@Finback: 1个 <br><br></b>
<b>@小刘小刘开心加油: 1个 <br><br></b>
<b>@EatKfcV50: 1个 <br><br></b>
<b>@VBPush: 1个 <br><br></b>
<b>@ysdxj: 1个 <br><br></b>
<b>@nonu11: 1个 <br><br></b>
<b>@qty567: 1个 <br><br></b>
<b>@sourcexu7: 1个 <br><br></b>
<b>@あくま: 1个 <br><br></b>
<b>@rain: 1个 <br><br></b>
<b>@忘年忘义振于无竟: 1个 <br><br></b>
<b>@一根胡萝卜: 1个 <br><br></b>
<b>@秋分: 1个 <br><br></b>
<b>@omegazero01: 1个 <br><br></b>
<b>@圣男: 1个 <br><br></b>
<b>@1204554617: 1个 <br><br></b>
<b>@无忧: 1个 <br><br></b>
<b>@FanerAce: 1个 <br><br></b>
<b>@狐狸: 1个 <br><br></b>
<b>@Acczdy: 1个 <br><br></b>
<b>@xjp08: 1个 <br><br></b>
<b>@Narcissus: 1个 <br><br></b>
<b>@sutdent1: 1个 <br><br></b>
<b>@restart: 1个 <br><br></b>
<b>@哥斯拉Yvan: 1个 <br><br></b>
<b>@菜狗: 1个 <br><br></b>
<b>@Atirds: 1个 <br><br></b>
<b>@CSeroad: 1个 <br><br></b>
<b>@Ashthes: 1个 <br><br></b>
<b>@45: 1个 <br><br></b>
<b>@j1dag: 1个 <br><br></b>
<b>@kkkyan: 1个 <br><br></b>
<b>@b2522: 1个 <br><br></b>
<b>@Cx330才: 1个 <br><br></b>
<b>@1337Player: 1个 <br><br></b>
<b>@Again: 1个 <br><br></b>
<b>@看我扭转万象: 1个 <br><br></b>
<b>@Yo皮蛋: 1个 <br><br></b>
<b>@LittleMoonhub: 1个 <br><br></b>
<b>@呱呱: 1个 <br><br></b>
<b>@MTY123-YF: 1个 <br><br></b>
<b>@Baal: 1个 <br><br></b>
<b>@yhy: 1个 <br><br></b>
<b>@wuha: 1个 <br><br></b>
<b>@Scappy: 1个 <br><br></b>
<b>@古心静典: 1个 <br><br></b>
<b>@starscow: 1个 <br><br></b>
<b>@slack: 1个 <br><br></b>
<b>@1: 1个 <br><br></b>
<b>@天明: 1个 <br><br></b>
<b>@肖肖乐: 1个 <br><br></b>
<b>@Hem1ock: 1个 <br><br></b>
<b>@SinkO: 1个 <br><br></b>
<b>@朱瀚声: 1个 <br><br></b>
<b>@陳: 1个 <br><br></b>
<b>@方糖: 1个 <br><br></b>
<b>@DouLiYouTang31: 1个 <br><br></b>
<b>@0x4C79: 1个 <br><br></b>
<b>@我该叫什么: 1个 <br><br></b>
<b>@fitzxxx: 1个 <br><br></b>
<b>@ki10Moc: 1个 <br><br></b>
<b>@陈皮老四: 1个 <br><br></b>
<b>@🇯: 1个 <br><br></b>
<b>@猫哥: 1个 <br><br></b>
<b>@放飞梦想จุ๊บ: 1个 <br><br></b>
<b>@Darkid_98: 1个 <br><br></b>
<b>@-A1ert: 1个 <br><br></b>
<b>@kkbo: 1个 <br><br></b>
<b>@huclilu: 1个 <br><br></b>
<b>@wlaq-su: 1个 <br><br></b>
<b>@RL: 1个 <br><br></b>
<b>@xiaojj2021: 1个 <br><br></b>
<b>@哈哈: 1个 <br><br></b>
<b>@yuwan-jpg: 1个 <br><br></b>
<b>@烧烤老师傅: 1个 <br><br></b>
<b>@六六: 1个 <br><br></b>
<b>@辞忧: 1个 <br><br></b>
<b>@ymbzd: 1个 <br><br></b>
<b>@WasteMaterial: 1个 <br><br></b>
<b>@lwjdsgz: 1个 <br><br></b>
<b>@jisanlong: 1个 <br><br></b>
<b>@Phonk: 1个 <br><br></b>
<b>@rkabyss: 1个 <br><br></b>
<b>@wvykey: 1个 <br><br></b>
<b>@那个少年: 1个 <br><br></b>
<b>@DeEpinGh0st: 1个 <br><br></b>
<b>@endin9: 1个 <br><br></b>
<b>@高歌: 1个 <br><br></b>
<b>@WangGang: 1个 <br><br></b>
<b>@一口蛋黄苏: 1个 <br><br></b>
<b>@nuanfeng1yue: 1个 <br><br></b>
<b>@清风拂杨柳: 1个 <br><br></b>
<b>@Thron_bird: 1个 <br><br></b>
<b>@咕噜咕噜: 1个 <br><br></b>
<b>@行者无疆: 1个 <br><br></b>
<b>@impdx: 1个 <br><br></b>
<b>@2gggggg: 1个 <br><br></b>
<b>@pei: 1个 <br><br></b>
<b>@80576560: 1个 <br><br></b>
<b>@下完雪🍁: 1个 <br><br></b>
<b>@Huck-Lim: 1个 <br><br></b>
<b>@sq565163: 1个 <br><br></b>
<b>@Lelylsj: 1个 <br><br></b>
<b>@Sharlong-Wen: 1个 <br><br></b>
<b>@bupsdx: 1个 <br><br></b>
<b>@Hhhnee: 1个 <br><br></b>
<b>@Grit: 1个 <br><br></b>
<b>@一起看雪: 1个 <br><br></b>
<b>@南: 1个 <br><br></b>
<b>@冰點: 1个 <br><br></b>
<b>@piaolingshusheng: 1个 <br><br></b>
<b>@LC: 1个 <br><br></b>
<b>@龙猫爱吃鱼: 1个 <br><br></b>
<b>@xg: 1个 <br><br></b>
<b>@rtfghd: 1个 <br><br></b>
<b>@qtz777: 1个 <br><br></b>
    </td>
  </tr>
</table>






[url-poc-key]: POC提交及无影Key获取说明.md

