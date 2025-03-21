# TscanClient

`TscanClient`是`TscanPlus`的命令行版本，保留了`TscanPlus`的核心功能，包括端口扫描、URL指纹识别、POC漏洞验证、弱口令破解、目录扫描、JS敏感信息收集、子域名枚举以及网络资产测绘等功能模块。

`TscanClient`与`TscanPlus`可以共享配置文件`config.yaml` 和数据库 `config.db`，且命令行版本能支持更多平台和系统，使用更加灵活便捷。

## 功能特点

- **多功能集成**：提供端口扫描、漏洞验证、弱口令检测等多种安全检测功能，一站式解决安全评估需求
- **高性能扫描**：采用高并发设计，支持大规模目标快速扫描
- **精准识别**：集成丰富的指纹库和POC库，准确识别Web应用和常见漏洞
- **可定制化**：支持自定义扫描策略，灵活配置扫描参数
- **跨平台兼容**：命令行版本支持更多操作系统平台，使用更加灵活
- **资源共享**：与TscanPlus共享配置文件和数据库，实现数据互通
- **友好输出**：结果展示清晰直观，支持分离进度条显示，方便结果分析

## 核心功能模块

TscanClient 包含以下八个核心功能模块：

1. 端口扫描
2. URL指纹识别
3. POC漏洞验证
4. 弱口令破解
5. 目录扫描
6. JS敏感信息收集
7. 子域名枚举
8. 网络资产测绘


## 参数详解与使用示例

### 各功能模块的使用

命令行格式：

```
TscanClient -m port,url,poc,crack,dir,js,domain,cyber [参数]
```

其中`-m`是最重要的功能选择参数，控制是否开启`端口扫描(port)、web探测(url)、Poc检测(poc)、密码破解(crack)、目录枚举(dir)、JS敏感信息(js)、子域名枚举(domain)、空间测绘(cyber)`八大功能。

多功能的联动等同于`TscanPlus`的项目管理，当八项功能都开启时，会以下面的流程进行检测，**前一项检测的所有结果都会输入给下一项检测作为输入**。

**空间测绘(cyber) -> 子域名枚举(domain) ->  端口扫描(port) ->  密码破解(crack) ->  web探测(url) -> Poc检测(poc) -> 目录枚举(dir) -> JS敏感信息(js)**

**扫描结果：**

1、`TscanClient`在根目录下会产生`TscanClient.txt`的日志文件，包含所有的日志和过程结果

2、`TscanClient`还会将八大功能模块的结果分别存放在独立的txt文档中，方便结果查看。

3、`TscanClient`还会把所有结果保存到`config.db`中，该文件可以替换到`TscanPlus`的配置目录下，使用`TscanPlus`打开再利用。

除各单项功能外，最常用的几种组合模式：

1、端口扫描 `-m port,poc,crack`

2、web探测 `-m url,poc,dir,js`

3、子域名枚举 `-m domain,port,url,poc`

注意：`如果资产太多，尽量不要开启太多功能，以免耗时太久或耗尽CPU资源。`

### 通用参数

| 参数         | 说明                                            | 默认值               |
|------------|-----------------------------------------------|-------------------|
| `-pr`      | 项目名称，可自定义，方便在数据库中保存                           | `Default`         |
| `-m`       | 任务模块，可选：port,url,poc,crack,dir,js,domain,cyber | `port,poc,crack`  |
| `-o`       | 结果输出文件                                        | `TscanClient.txt` |
| `-no`      | 禁用结果保存                                        | `false`           |
| `-nocolor` | 禁用彩色输出                                        | `false`           |
| `-proxy` | 设置HTTP或socks5代理，注：端口扫描只能使用socks5代理        | -        |

**通用参数使用示例：**

```bash
# 使用默认端口进行ip扫描，同时开启指纹匹配poc和弱口令自动破解
TscanClient -h 192.168.1.1/24

# 对URL地址批量进行扫描，并进行poc检测和目录检测
TscanClient -m url,poc,dir,js -uf urls.txt

#对子域名进行枚举，并对发现的子域名进行端口扫描、poc检测、url指纹识别
TscanClient -m domain,port,url,poc -d example.com

# 指定项目名称并开启多个模块
TscanClient -pr MyProject -m port,url,poc -h 192.168.1.1

# 指定自定义输出文件
TscanClient -h 192.168.1.1 -o scan-results.txt

# 禁用彩色输出和结果保存
TscanClient -h 192.168.1.1 -nocolor -no
```

### 端口扫描参数（port模块）

| 参数       | 说明                                        | 默认值      |
|----------|-------------------------------------------|----------|
| `-h`     | 目标主机IP，例如: `192.168.1.1`,`192.168.1.1/24` | -        |
| `-hn`    | 排除的主机范围，例如: -hn `192.168.1.1/24`          | -        |
| `-p`     | 端口配置，例如: `22`或`1-65535`或`22,80,3306`      | Top100端口 |
| `-pa`    | 在默认端口基础上添加端口，`-pa 3389`                   | -        |
| `-hf`    | 主机列表文件                                    | -        |
| `-portf` | 端口列表文件                                    | -        |
| `-t`     | 线程数量                                      | `600`    |
| `-time`  | 超时时间(秒)                                   | `3`      |
| `-np`    | 禁用存活探测                                    | `false`  |

**端口扫描使用示例：**

```bash
# 扫描主机，使用默认端口和线程
TscanClient -m port -h 192.168.1.1/24

# 扫描单个主机的指定端口
TscanClient -m port -h 192.168.1.1 -p 80,443,3306

# 扫描C段网络上的常用Web端口,设置更高线程数
TscanClient -m port -h 192.168.1.0/24 -p 80,443,8080,8443 -t 1000 

# 使用主机列表文件进行扫描
TscanClient -m port -hf hosts.txt -p 22,80,443

# 在默认端口基础上添加自定义端口
TscanClient -m port -h 192.168.1.1 -pa 8080,9000
```

### Web应用扫描参数（url模块）

| 参数        | 说明                                    | 默认值    |
|-----------|---------------------------------------|--------|
| `-u`      | 目标URL                                 | -      |
| `-uf`     | URL列表文件                               | -      |
| `-cookie` | 设置Cookie                              | -      |
| `-wt`     | Web请求超时时间                             | `10`   |
| `-proxy`  | 设置HTTP或socks5代理                       | -      |
| `-finger` | 设置web指纹策略，例如：-finger min 或 tiny 或 all | `tiny` |

**Web应用扫描使用示例：**

```bash
# 指定URL进行Web指纹识别
TscanClient -m url -u http://example.com 

# 从文件加载URL列表并选择全量指纹
TscanClient -m url,poc -uf urls.txt -finger all

# 设置Cookie进行认证扫描
TscanClient -m url -u http://example.com -cookie "session=123456"

# 通过代理进行扫描
TscanClient -m url,poc -u http://example.com -proxy http://127.0.0.1:8080 

# 增加Web请求超时时间
TscanClient -m url,poc -u http://example.com -wt 10
```

### POC漏洞验证参数（poc模块）

| 参数          | 说明                                         | 默认值         |
|-------------|--------------------------------------------|-------------|
| `-pocpath`  | POC文件路径，和`TscanPlus`一样，仅支持`xray 1.0`格式的Poc | -           |
| `-pocname`  | 使用包含指定名称的POC,例如: `-pocname weblogic`       | -           |
| `-full`     | 不匹配指纹，完整POC扫描，默认匹配指纹后检测poc                 | `false`     |
| `-num`      | POC并发数                                     | `20`        |
| `-poclevel` | 设置使用的POC级别，默认1+2+3+4+5                     | `1+2+3+4+5` |
| `-poclist`  | 打印所有POC列表                                  | `false`     |
| `-pd`       | 当poc检测成功时显示数据包                             | `false`     |

**POC漏洞验证使用示例：**

```bash
# 对目标进行默认POC验证
TscanClient -m poc -u http://example.com 

# 使用指定POC检测漏洞，在检测到Poc时打印请求和响应数据包
TscanClient -m poc -u http://example.com -pocname weblogic -pd

# 使用自定义POC路径
TscanClient -m poc -u http://example.com -pocpath /path/to/pocs

# poc不匹配指纹，会检测所有内置poc
TscanClient -m poc -u http://example.com -full

# 调整POC并发数和级别
TscanClient -m poc -u http://example.com -num 50 -poclevel 1+2 

# 打印所有可用POC列表
TscanClient -poclist

```

### 弱口令检测参数（crack模块）

| 参数       | 说明                         | 默认值      |
|----------|----------------------------|----------|
| `-br`    | 密码爆破线程数                    | `1`      |
| `-s`     | 暴力破解的服务，例如: -s ssh,mysql   | `all`    |
| `-user`  | 用户名，不指定时使用内置字典             | -        |
| `-pwd`   | 密码，不指定时使用内置字典              | -        |
| `-c`     | 执行命令(支持ssh、wmiexec、mysql等) | `whoami` |
| `-userf` | 用户名字典文件                    | -        |
| `-pwdf`  | 密码字典文件                     | -        |

**弱口令检测使用示例：**

```bash
# 对SSH服务进行弱口令检测
TscanClient -m crack -h 192.168.1.1 -p 22 -s ssh

# 使用自定义字典进行MySQL密码破解
TscanClient -m crack -h 192.168.1.1 -p 3306 -s mysql -userf users.txt -pwdf pass.txt

# 增加爆破线程数
TscanClient -m crack -h 192.168.1.1 -p 3389 -s rdp -br 5

# 指定用户名和密码进行爆破
TscanClient -m crack -h 192.168.1.1 -p 22 -s ssh -user root,admin -pwd 123456,password 

# 爆破成功后执行命令
TscanClient -m crack -h 192.168.1.1 -p 22 -s ssh -c "id"
```

### 子域名枚举参数（domain模块）

| 参数     | 说明                | 默认值     |
|--------|-------------------|---------|
| `-d`   | 域名枚举目标，支持逗号分隔     | -       |
| `-df`  | 域名枚举目标文件          | -       |
| `-dc`  | 域名枚举字典，需完整绝对路径    | -       |
| `-api` | 域名枚举是否使用API，默认不启用 | `false` |

**子域名枚举使用示例：**

**子域名枚举时默认是开启API查询的，但API的key需要在`config.yaml`文件中手动配置，也可把`TscanPlus`的配置文件拷贝过来直接使用。
**

```bash
# 对单个域名进行子域名枚举
TscanClient -m domain -d example.com 

# 对多个域名进行子域名枚举，并启用api检索，api的key需自行在config.yaml文件中配置
TscanClient -m domain -d example.com,example.org -api

# 使用自定义字典进行子域名枚举
TscanClient -m domain -df domains.txt -dc /path/to/subdomains.txt

# 子域名枚举后进行指纹识别和漏洞扫描
TscanClient -m domain,url,poc -d example.com
```

### 目录扫描参数（dir模块）

| 参数   | 说明                           | 默认值 |
|------|------------------------------|-----|
| `-u` | URL地址                        | -   |
| `-uf` | URL列表文件                      | -   |
| `-ds` | 目录枚举线程设置                     | 20  |
| `-dd` | 目录枚举字典，需完整绝对路径，不指定时使用内置10k字典 | -   |

**目录扫描使用示例：**

```bash
# 对目标URL进行目录扫描
TscanClient -m dir -u http://example.com

# 使用自定义字典进行目录扫描
TscanClient -m dir -u http://example.com -dd /path/to/dirlist.txt 

# 设置目录扫描线程数
TscanClient -m dir -u http://example.com -ds 50 
```

### JS敏感信息收集（js模块）

| 参数        | 说明              | 默认值  |
|-----------|-----------------|------|
| `-u`      | 目标URL           | -    |
| `-uf`     | URL列表文件         | -    |
| `-cookie` | 设置Cookie        | -    |
| `-wt`     | Web请求超时时间       | `10` |
| `-proxy`  | 设置HTTP或socks5代理 | -    |

**JS敏感信息收集使用示例：**

```bash
./TscanClient -m js -u https://example.com -wt 10
```

此命令对example.com进行JS文件敏感信息收集，Web请求超时10秒。

### 空间测绘参数（cyber模块）

| 参数    | 说明                                   | 默认值 |
|-------|--------------------------------------|-----|
| `-ck` | 空间测绘查询语句，例如：-ck domain="tidesec.com" | -   |

**空间测绘使用示例：**

**空间测绘API的key需要在`config.yaml`文件中手动配置，也可把`TscanPlus`的配置文件拷贝过来直接使用。**

```bash
# 查询特定域名的资产
TscanClient -m cyber -ck domain="example.com"

# 查询特定IP段的资产
TscanClient -m cyber -ck ip="192.168.1.0/24" 

# 查询特定服务的资产
TscanClient -m cyber -ck service="nginx"

# 空间测绘后进行进一步扫描
TscanClient -m cyber,port,poc -ck domain="example.com" 
```

### 批量扫描示例

```bash
# 对C段进行全面扫描
TscanClient -h 192.168.1.0/24 -m port,url,poc,crack

# 从URL文件加载并进行全面扫描
TscanClient -uf target-urls.txt -m url,poc,dir,js
```

### 综合扫描示例

```bash
# 端口扫描+指纹识别+POC检测+弱口令破解
TscanClient -h 192.168.1.0/24 -p 1-65535 -t 1000 -m port,url,poc,crack

# 全功能扫描
TscanClient -h 192.168.1.0/24 -d example.com -m port,url,poc,crack,dir,js,domain,cyber
```

## 与TscanPlus的关系

TscanClient 是 TscanPlus 的命令行版本，两者共享核心功能和检测引擎：

- TscanClient 与 TscanPlus 共享配置文件 config.yaml 和数据库 config.db
- TscanClient 具有更好的跨平台兼容性，支持更多操作系统环境
- TscanClient 适合自动化脚本集成和服务器环境使用
- TscanPlus 提供图形界面，更适合需要可视化展示的环境

## 使用注意事项

- 扫描前请确保已获得授权，未经授权的扫描行为可能违反法律法规
- 建议先使用较小的线程数和端口范围进行测试，避免对目标系统造成过大负载
- 针对生产环境进行扫描时，建议在非业务高峰期进行
- 使用代理进行扫描时，请确保代理配置正确且稳定

## 适用场景

- 内网安全评估和资产梳理
- 外部渗透测试前的信息收集
- 企业安全基线检查
- 安全漏洞应急响应
- 自动化安全扫描流程
- 服务器环境下的批量扫描任务

更多信息可参考 TscanPlus 项目：[https://github.com/TideSec/TscanPlus](https://github.com/TideSec/TscanPlus)

