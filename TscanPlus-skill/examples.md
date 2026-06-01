# TscanPlus MCP 对话与模块示例

以下示例适用于任何能调用 TscanPlus MCP 工具的 AI 助手。参数语义对齐 **TscanClient** / **TscanPlus CLI**（`-m` 八大模块）。执行前须确认**授权**。

**模块对照：** `port`→`ip_scan`，`url`→`url_scan`，`poc`→`poc_scan`，`crack`→`pwd_crack`，`dir`→`dir_scan`，`js`→`js_scan`，`domain`→`subdomain_scan`，`cyber`→`cyber_search`，多模块联动→`tscan_scan`。

---

## 一、端口扫描 `ip_scan`（port）

### 示例 1-1：单 IP 常见 Web 端口

**用户：** 帮我扫 10.211.55.2 有哪些常见 Web 端口。

**Agent：**

1. 确认授权。
2. 调用 `ip_scan`：

```yaml
target: "10.211.55.2"
ports: "80,443,8080,8443,8000,8888,22"
ping_scan: true
ip_finger: false
poc_check: false
pwd_check: false
thread: 200
timeout: 3
include_results: true
```

3. 汇报 `data.results.ipscan` 的 `host`、`port`、`target`、`title`。

**CLI 等价：** `TscanPlus -m port -h 10.211.55.2 -p 80,443,8080,8443,8000,8888,22 -t 200`

---

### 示例 1-2：C 段 Top100（lab）

**用户：** 扫 192.168.1.0/24 的 Top100 端口，不要 POC。

```yaml
tool: ip_scan
target: "192.168.1.0/24"
ports: "Top100"
thread: 400
ping_scan: true
poc_check: false
pwd_check: false
include_results: true
result_limit: 300
```

**CLI：** `TscanPlus -m port -h 192.168.1.0/24 -t 400`

---

### 示例 1-3：指定端口 + 服务指纹

**用户：** 对 192.168.1.10 扫 22,80,443,3306,3389 并识别服务。

```yaml
tool: ip_scan
target: "192.168.1.10"
ports: "22,80,443,3306,3389"
ip_finger: true
poc_check: false
thread: 300
```

---

### 示例 1-4：端口扫描联动弱口令（需明确授权）

**用户：** 已对 192.168.1.5 授权，对 22 和 3306 做弱口令检测。

```yaml
tool: ip_scan
target: "192.168.1.5"
ports: "22,3306"
pwd_check: true
poc_check: false
thread: 100
```

**CLI：** `TscanPlus -m port,crack -h 192.168.1.5 -p 22,3306`

---

### 示例 1-5：端口 + POC（需明确授权）

```yaml
tool: ip_scan
target: "10.0.0.100"
ports: "80,443,8080"
poc_check: true
pwd_check: false
thread: 200
```

---

## 二、Web 指纹 `url_scan`（url）

### 示例 2-1：单 URL 指纹

**用户：** 识别 http://test.lab:8080 的 Web 指纹。

```yaml
tool: url_scan
targets: "http://test.lab:8080"
finger: tiny
web_timeout: 10
poc_check: false
thread: 30
include_results: true
```

**CLI：** `TscanPlus -m url -u http://test.lab:8080 -finger tiny`

---

### 示例 2-2：批量 URL

**用户：** 对这些站做 Web 探测：a.com 和 b.com 的 https。

```yaml
tool: url_scan
targets: "https://a.com,https://www.b.com"
finger: min
thread: 50
include_results: true
```

**CLI：** `TscanPlus -m url -u https://a.com,https://www.b.com -finger min`

---

### 示例 2-3：带 Cookie 的认证站

```yaml
tool: url_scan
targets: "http://internal.lab/admin/"
cookie: "session=abc123; token=xyz"
finger: tiny
web_timeout: 15
```

**CLI：** `TscanPlus -m url -u http://internal.lab/admin/ -cookie "session=abc123"`

---

### 示例 2-4：URL 指纹 + 联动 POC

**用户：** 已对下列 URL 授权打 POC。

```yaml
tool: url_scan
targets: "http://10.0.0.1:8080,http://10.0.0.2"
poc_check: true
finger: tiny
thread: 30
```

**CLI：** `TscanPlus -m url,poc -u http://10.0.0.1:8080,http://10.0.0.2`

---

### 示例 2-5：代理访问

```yaml
tool: url_scan
targets: "http://target.lab"
proxy: "http://127.0.0.1:8080"
finger: all
```

---

## 三、POC 漏洞 `poc_scan`（poc）

### 示例 3-1：默认 POC（匹配指纹）

```yaml
tool: poc_scan
targets: "http://test.lab"
thread: 20
poc_full: false
include_results: true
```

**CLI：** `TscanPlus -m poc -u http://test.lab`

---

### 示例 3-2：指定 POC 名称

**用户：** 用 weblogic 相关 POC 测 http://10.0.0.8:7001。

```yaml
tool: poc_scan
targets: "http://10.0.0.8:7001"
poc_name: weblogic
thread: 15
```

**CLI：** `TscanPlus -m poc -u http://10.0.0.8:7001 -pocname weblogic`

---

### 示例 3-3：全量 POC（高危，需授权）

```yaml
tool: poc_scan
targets: "http://vuln.lab"
poc_full: true
thread: 10
poc_level: "1+2+3"
```

**CLI：** `TscanPlus -m poc -u http://vuln.lab -full -poclevel 1+2+3`

---

### 示例 3-4：批量 URL 文件场景（Agent 拆分）

**用户：** 我有 50 个 URL 要打 POC。

Agent：分批逗号传入（每批 ≤20），或建议用户改用 CLI `-uf urls.txt`。

```yaml
tool: poc_scan
targets: "http://a.lab,http://b.lab"
thread: 20
```

---

## 四、弱口令 `pwd_crack`（crack）

### 示例 4-1：SSH 单主机

```yaml
tool: pwd_crack
targets: "192.168.1.1:22"
services: ssh
user: "root,admin"
pwd: "123456,password,admin123"
thread: 2
timeout: 5
```

**CLI：** `TscanPlus -m crack -h 192.168.1.1 -p 22 -s ssh -user root,admin -pwd 123456,password`

---

### 示例 4-2：MySQL

```yaml
tool: pwd_crack
targets: "192.168.1.20:3306"
services: mysql
thread: 1
```

---

### 示例 4-3：多目标多服务

```yaml
tool: pwd_crack
targets: "10.0.0.1:22,10.0.0.1:3389,10.0.0.2:3306"
services: "ssh,rdp,mysql"
thread: 1
```

---

### 示例 4-4：爆破成功后执行命令

```yaml
tool: pwd_crack
targets: "192.168.1.1:22"
services: ssh
cmd: "id"
user: root
pwd: "toor,123456"
```

**CLI：** `TscanPlus -m crack -h 192.168.1.1 -p 22 -s ssh -c "id"`

---

## 五、子域名 `subdomain_scan`（domain）

### 示例 5-1：单域字典枚举

```yaml
tool: subdomain_scan
domains: "example.com"
sub_api: false
ports: "80,443"
include_results: true
```

**CLI：** `TscanPlus -m domain -d example.com`

---

### 示例 5-2：多域 + API（config 已配 key）

```yaml
tool: subdomain_scan
domains: "example.com,example.org"
sub_api: true
ports: "80,443,8080"
```

**CLI：** `TscanPlus -m domain -d example.com,example.org -api`

---

### 示例 5-3：自定义字典

```yaml
tool: subdomain_scan
domains: "target.lab"
sub_dict: "/path/to/subdomains.txt"
sub_api: false
```

**CLI：** `TscanPlus -m domain -d target.lab -dc /path/to/subdomains.txt`

---

## 六、目录扫描 `dir_scan`（dir）

### 示例 6-1：内置字典

```yaml
tool: dir_scan
urls: "http://test.lab"
thread: 30
timeout: 5
include_results: true
```

**CLI：** `TscanPlus -m dir -u http://test.lab`

---

### 示例 6-2：自定义字典 + 高线程

```yaml
tool: dir_scan
urls: "https://test.lab"
dict: "/path/to/dirlist.txt"
thread: 50
```

**CLI：** `TscanPlus -m dir -u https://test.lab -dd /path/to/dirlist.txt -ds 50`

---

## 七、JS 敏感信息 `js_scan`（js）

### 示例 7-1：单站 JS 收集

```yaml
tool: js_scan
urls: "https://test.lab"
timeout: 10
include_results: true
```

**CLI：** `TscanPlus -m js -u https://test.lab -wt 10`

---

### 示例 7-2：多 URL

```yaml
tool: js_scan
urls: "https://a.lab,https://b.lab"
proxy: "socks5://127.0.0.1:1080"
```

---

## 八、空间测绘 `cyber_search`（cyber）

> 须在 `config.yaml` 配置 Hunter/FOFA 等引擎与 Key。

### 示例 8-1：按域名查资产

```yaml
tool: cyber_search
query: 'domain="example.com"'
field: domain
include_results: true
```

**CLI：** `TscanPlus -m cyber -ck 'domain="example.com"'`

---

### 示例 8-2：按 IP 段

```yaml
tool: cyber_search
query: 'ip="192.168.1.0/24"'
field: ip
```

---

### 示例 8-3：指定引擎

```yaml
tool: cyber_search
query: 'title="管理"'
field: custom
engines: "hunter,fofa"
```

---

## 九、综合扫描 `tscan_scan`（多模块联动）

联动顺序：**cyber → domain → port → crack → url → poc → dir → js**

### 示例 9-1：端口 + Web（最常用）

**用户：** 对 192.168.1.100 做端口和 Web 指纹，先不要 POC。

```yaml
tool: tscan_scan
targets: "192.168.1.100"
modules: "port,url"
ports: "Top100"
thread: "300"
url_thread: "50"
finger: tiny
ping_scan: true
include_results: true
```

**CLI：** `TscanPlus -m port,url -h 192.168.1.100 -finger tiny`

---

### 示例 9-2：内网 C 段 端口+URL+POC（授权）

```yaml
tool: tscan_scan
targets: "192.168.1.0/24"
modules: "port,url,poc"
ports: "Top100"
thread: "400"
poc_thread: "15"
finger: tiny
include_results: true
result_limit: 500
```

**CLI：** `TscanPlus -h 192.168.1.0/24 -m port,url,poc`（默认 -m）

---

### 示例 9-3：端口 + 弱口令 + POC

```yaml
tool: tscan_scan
targets: "192.168.1.0/24"
modules: "port,crack,url,poc"
ports: "22,80,443,3306,3389,8080"
crack_services: "ssh,mysql,rdp"
thread: "300"
```

**CLI：** `TscanPlus -m port,poc,crack -h 192.168.1.0/24 -p 22,80,443,3306,3389,8080`

---

### 示例 9-4：子域 → 端口 → Web → POC

```yaml
tool: tscan_scan
targets: "example.com"
domains: "example.com"
modules: "domain,port,url,poc"
sub_api: true
ports: "80,443,8080"
thread: "200"
include_results: true
```

**CLI：** `TscanPlus -m domain,port,url,poc -d example.com -api`

---

### 示例 9-5：Web 全链路 url+poc+dir+js

```yaml
tool: tscan_scan
targets: "http://test.lab,http://api.test.lab"
modules: "url,poc,dir,js"
finger: tiny
dir_thread: "30"
include_results: true
```

**CLI：** `TscanPlus -m url,poc,dir,js -u http://test.lab,http://api.test.lab`

---

### 示例 9-6：测绘后联动扫描

```yaml
tool: tscan_scan
targets: 'domain="target.lab"'
cyber_query: 'domain="target.lab"'
cyber_field: domain
modules: "cyber,port,url"
ports: "Top100"
thread: "300"
```

**CLI：** `TscanPlus -m cyber,port,url -ck 'domain="target.lab"'`

---

### 示例 9-7：追加端口、排除主机

```yaml
tool: tscan_scan
targets: "10.0.0.0/24"
modules: "port,url"
ports: "Top100"
ports_add: "3389,5985,6379"
exclude_hosts: "10.0.0.1"
smart_scan: true
thread: "400"
```

**CLI：** `TscanPlus -m port,url -h 10.0.0.0/24 -pa 3389,5985,6379 -hn 10.0.0.1`

---

### 示例 9-8：关闭启发式大网段扫描

```yaml
tool: tscan_scan
targets: "10.0.0.0/16"
modules: "port"
ports: "80,443"
smart_scan: false
thread: "200"
```

**CLI：** `TscanPlus -m port -h 10.0.0.0/16 -p 80,443 -nosmart`

---

## 十、项目管理

### 示例 10-1：默认 MCP 项目（每次清空）

未传 `project` 时自动使用 `MCP` 并在调用前清空，适合一次性对话扫描。

### 示例 10-2：命名项目、累积结果

```yaml
tool: subdomain_scan
domains: "example.com"
project: pentest-acme
# fresh_project 默认 false → 追加
```

### 示例 10-3：清空后重扫

```yaml
tool: ip_scan
target: "10.0.0.0/24"
ports: "Top100"
project: pentest-acme
fresh_project: true
```

### 示例 10-4：综合项目登记

```yaml
tool: tscan_scan
targets: "192.168.1.0/24"
modules: "port,url,poc"
project: pentest-acme
fresh_project: true
```

` tscan_scan` 会在 GUI `project` 表登记；单工具可能仅写分表。

---

## 十一、分阶段工作流（推荐 Agent 策略）

### 工作流 A：IP → Web → 漏洞

1. `ip_scan`：`ports: "80,443,8080,8443"`
2. 从 `results.ipscan` 提取 `target` URL
3. `url_scan`：`finger: tiny`
4. 用户确认后 `poc_scan` 或 `tscan_scan` 仅 `poc` 模块

### 工作流 B：子域资产扩张

1. `subdomain_scan` + `sub_api: true`
2. `tscan_scan`：`modules: "port,url"`，`targets` 为子域列表
3. 对高危 URL 单独 `poc_scan`

### 工作流 C：测绘驱动

1. `cyber_search` 获取 IP/域名
2. 向用户展示摘要，确认范围
3. `ip_scan` / `url_scan` 分批执行（控制 `result_limit`）

---

## 十二、拒绝未授权扫描

**用户：** 扫一下 https://www.baidu.com 有没有漏洞。

**Agent 应：**

说明无法对未授权的第三方生产站点执行扫描；可改为在用户自有 lab 靶机上演示 `poc_scan` 参数与返回结构，不进行真实请求。

---

## 十三、返回 JSON 结构参考

```json
{
  "success": true,
  "message": "ip_scan completed",
  "data": {
    "project": "MCP",
    "project_cleared": true,
    "target": "10.211.55.2",
    "ports": "80,443,8080",
    "result_limit": 200,
    "counts": { "ipscan": 3, "urlscan": 1, "poccheck": 0 },
    "results": {
      "ipscan": [
        {
          "host": "10.211.55.2",
          "port": "8083",
          "target": "http://10.211.55.2:8083",
          "title": "..."
        }
      ],
      "urlscan": [],
      "poccheck": []
    }
  }
}
```

**各表关键字段（汇报时优先提取）：**

| 表名 | 字段 |
|------|------|
| `ipscan` | `host`, `port`, `target`, `title`, `banner` |
| `urlscan` | `target`, `title`, `finger`, `status` |
| `poccheck` | `target`, `poc_vul`, `level`, `request` |
| `pwdcrack` | `host`, `port`, `service`, `user`, `pass` |
| `dirscan` | `url`, `path`, `status`, `len` |
| `jsfinder` | `url`, `match`, `type` |
| `subdomain` | `domain`, `subdomain`, `ips` |
| `cyber` | `ip`, `domain`, `port`, `title`, `source` |

---

## 十四、CLI 批量对照（无 MCP 时）

```bash
# C 段全面（慎用范围）
TscanPlus -h 192.168.1.0/24 -m port,url,poc,crack

# URL 文件
TscanPlus -uf target-urls.txt -m url,poc,dir,js

# 全功能（lab 仅限）
TscanPlus -h 192.168.1.0/24 -d example.com -m port,url,poc,crack,dir,js,domain,cyber

# 指定项目
TscanPlus -pr MyProject -m port,url,poc -h 192.168.1.1
```

Agent 在 MCP 可用时应优先调用工具并解析 JSON，CLI 仅作备选说明。
