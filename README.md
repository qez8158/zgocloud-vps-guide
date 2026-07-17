# ZgoCloud套餐全攻略：美国/日本/香港/德国机房怎么选？CN2 GIA、9929、CMIN2优化线路实测对比，附年付9.5折优惠码与全部方案价格表

第一次听到 ZgoCloud（也叫 ZgoVPS）这个名字，是去年帮一个朋友找海外 VPS 的时候。他要做一个小博客，预算卡得死死的，年付最好别超过 100 块人民币，但又嫌弃那些动不动就抽风的廉价机房。我在几个主机论坛里翻了一圈，发现这家 2021 年才成立的"小厂"被反复提到，关键词很统一：AMD EPYC、9929、CMIN2、原生 IP、价格还能打。就这么半信半疑地帮他下了单，跑了几个月，居然真的没翻车。

后来我自己也陆续入手了几台不同机房、不同线路的套餐，正好趁着整理手上这几台机器，把 ZgoCloud 目前在售的**全部套餐**梳理一遍。如果你正卡在"到底选哪个机房、哪条线路、哪个套餐"这个纠结点上，这篇应该能帮你把账算清楚。

## ZgoCloud 是个什么来头

先把品牌底子交代清楚，免得你下单前心里没底。

ZgoCloud 的运营主体叫 ZgoShop, Inc.，注册在美国特拉华州，备案号 6298021，成立时间是 2021 年——在 VPS 这个圈子里算年轻选手。它自己运营着一个 ASN：**AS197767**，和 NTT、Orange S.A.、Cogent 这几个 Tier 1 网络对接，是 ARIN 和 RIPE 的成员。说白了，它不是那种租个机柜倒卖资源的二级分销商，自己手里是有网络资源的。

数据中心目前覆盖四个城市：

- **美国洛杉矶**：主力机房，套餐最多，线路分得最细（CN2 GIA / 9929 / CMIN2 三网优化、双 ISP 原生 IP、国际线路）
- **日本东京**：Intel Xeon Gold 6248，BGP 大陆优化直连
- **日本大阪**：AMD EPYC 9354P 和 Ryzen9 7950X，IIJ 线路（不针对中国优化，但带宽大、延迟稳）
- **中国香港**：AMD EPYC 7002，BGP 三网直连，延迟最低但带宽只有 100Mbps
- **德国 Falkenstein**：Intel Xeon Gold 5412U，国际线路，主打大流量便宜

硬件方面基本是当下主流偏上的配置：AMD EPYC 7002/7003/9004 Genoa、Ryzen 9 7950X、Intel Xeon Platinum 8452Y、Xeon Gold 5412U，内存从 DDR4 到 DDR5 ECC 都有，硬盘清一色 NVMe SSD，部分高端套餐上 PCIe 4.0。支付支持 PayPal、Stripe（信用卡）和支付宝，国内用户付款没什么障碍。

## 先看一张总表：所有在售套餐一次看全

下面这张表是这次整理的核心，覆盖 ZgoCloud 官网目前展示的**全部套餐**，按机房和线路分组。价格分两类：**Specials** 是限量特价款（年付为主，不可退款、不能用优惠码），**常规款**是按季付的长期在售方案（可用 9.5 折优惠码 `8NU44CM6LZ`，续费同价）。

### 美国洛杉矶机房

洛杉矶是 ZgoCloud 的"主战场"，套餐按线路和 CPU 平台分了 7 个系列。

**① Los Angeles AMD Optimised VPS — CN2 GIA + 9929 + CMIN2 三网优化（AMD EPYC 7002）**

| 套餐 | CPU | 内存 | NVMe | 流量/月 | 带宽 | 价格 | 购买 |
|---|---|---|---|---|---|---|---|
| Specials - Starter | 1 核 EPYC 7002 | 1GB DDR4 | 10GB | 500GB | 200Mbps | $52/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=142) |
| Specials - Standard | 2 核 EPYC 7002 | 2GB DDR4 | 20GB | 1TB | 200Mbps | $96/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=143) |
| Starter | 1 核 EPYC 7002 | 1GB DDR4 | 10GB | 500GB | 200Mbps | $18/季 | [立即购买](https://bit.ly/zgovps) |
| Standard | 2 核 EPYC 7002 | 2GB DDR4 | 20GB | 1TB | 200Mbps | $32/季 | [立即购买](https://bit.ly/zgovps) |
| Pro | 3 核 EPYC 7002 | 3GB DDR4 | 30GB | 1.5TB | 200Mbps | $45/季 | [立即购买](https://bit.ly/zgovps) |
| Premium | 4 核 EPYC 7002 | 4GB DDR4 | 50GB | 2TB | 200Mbps | $58/季 | [立即购买](https://bit.ly/zgovps) |

这条线是 ZgoCloud 的招牌，CN2 GIA + AS9929 + CMIN2 三网都走优化，电信/联通/移动晚高峰都比较稳，适合做站、远程办公、看流媒体。

**② Los Angeles AMD VPS — 9929 + CMIN2 优化（AMD EPYC 7003，DDR4/DDR5 ECC + PCIe 4.0）**

| 套餐 | CPU | 内存 | NVMe | 流量/月 | 带宽 | 价格 | 购买 |
|---|---|---|---|---|---|---|---|
| Specials - Lite | 1 核 EPYC 7003 | 1GB DDR4 | 20GB | 600GB | 200Mbps | $25/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=65) |
| Specials - Starter | 1 核 EPYC 7003 | 2GB DDR4 | 30GB | 1TB | 300Mbps | $36/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=115) |
| Specials - Standard | 2 核 EPYC 7003 | 3GB DDR4 | 50GB | 2TB | 300Mbps | $66/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=67) |
| Starter | 1 核 EPYC 7003 | 2GB DDR4 | 30GB | 1TB | 300Mbps | $16/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=68) |
| Standard | 2 核 EPYC 7003 | 3GB DDR4 | 50GB | 2TB | 300Mbps | $24/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=69) |
| Pro | 3 核 EPYC 7003 | 4GB DDR4 ECC | 80GB PCIe 4.0 | 2TB | 300Mbps | $32/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=72) |
| Premium | 4 核 EPYC 7003 | 6GB DDR4 ECC | 100GB PCIe 4.0 | 2TB | 300Mbps | $40/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=73) |
| Ultra | 6 核 EPYC 7003 | 8GB DDR4 ECC | 120GB PCIe 4.0 | 2TB | 500Mbps | $52/季 | [立即购买](https://bit.ly/zgovps) |

这是性能和性价比平衡得最好的一条线：EPYC 7003 比 7002 新一代，带宽普遍 300Mbps，Pro 档以上还升级了 DDR5 ECC 和 PCIe 4.0。如果你预算够不到 Ryzen9，又想要点性能余量，这条线的中配套餐很值。

**③ Los Angeles Intel Performance VPS — 9929 + CMIN2 优化（Intel Xeon Platinum 8452Y，DDR5 + PCIe 4.0）**

| 套餐 | CPU | 内存 | NVMe | 流量/月 | 带宽 | 价格 | 购买 |
|---|---|---|---|---|---|---|---|
| Specials - Lite | 1 核 Platinum 8452Y | 768MB DDR5 | 15GB | 600GB | 200Mbps | $30/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=39) |
| Specials - Starter | 1 核 Platinum 8452Y | 1GB DDR5 | 20GB | 1TB | 300Mbps | $42/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=32) |
| Specials - Standard | 2 核 Platinum 8452Y | 2GB DDR5 | 40GB | 2TB | 300Mbps | $88/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=31) |
| Starter | 1 核 Platinum 8452Y | 1GB DDR5 | 20GB | 1TB | 300Mbps | $18/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=26) |
| Standard | 2 核 Platinum 8452Y | 2GB DDR5 | 40GB | 2TB | 300Mbps | $28/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=27) |
| Pro | 3 核 Platinum 8452Y | 4GB DDR5 | 80GB PCIe 4.0 | 2TB | 300Mbps | $38/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=28) |
| Premium | 4 核 Platinum 8452Y | 6GB DDR5 | 100GB PCIe 4.0 | 2TB | 300Mbps | $48/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=29) |

Intel 平台全线 DDR5 + PCIe 4.0，单核性能强，适合跑数据库、编译这类吃单核的任务。价格和 AMD 7003 系列差不多，选哪个看你更信 Intel 还是 AMD。

**④ Los Angeles AMD ISP VPS — 双 ISP 原生 IP（9929 + CMIN2，AMD EPYC 7002）**

| 套餐 | CPU | 内存 | NVMe | 流量/月 | 带宽 | 价格 | 购买 |
|---|---|---|---|---|---|---|---|
| Specials - Starter | 1 核 EPYC 7002 | 1GB DDR4 | 10GB | 500GB | 100Mbps | $58/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=148) |
| Specials - Standard | 2 核 EPYC 7002 | 2GB DDR4 | 20GB | 1TB | 100Mbps | $108/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=149) |
| Starter | 1 核 EPYC 7002 | 1GB DDR4 | 10GB | 500GB | 100Mbps | $20/季 | [立即购买](https://bit.ly/zgovps) |
| Standard | 2 核 EPYC 7002 | 2GB DDR4 | 20GB | 1TB | 100Mbps | $38/季 | [立即购买](https://bit.ly/zgovps) |
| Pro | 3 核 EPYC 7002 | 3GB DDR4 | 30GB | 1.5TB | 200Mbps | $56/季 | [立即购买](https://bit.ly/zgovps) |
| Premium | 4 核 EPYC 7002 | 4GB DDR4 | 50GB | 2TB | 200Mbps | $72/季 | [立即购买](https://bit.ly/zgovps) |

这条线的核心卖点是**双 ISP 原生 IP**——除 IP2Location 外，主流 IP 库都会把它识别为双 ISP，适合做流媒体解锁、跨境电商、对 IP 归属敏感的业务。注意它不支持优惠码，直接下单即可。

**⑤ Los Angeles Ryzen9 Performance VPS — CN2 GIA + 9929 + CMIN2（AMD Ryzen9 7950X）**

| 套餐 | CPU | 内存 | NVMe | 流量/月 | 带宽 | 价格 | 购买 |
|---|---|---|---|---|---|---|---|
| Specials - Lite | 1 核 Ryzen9 7950X | 512MB DDR5 | 15GB | 500GB | 200Mbps | $38.9/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=101) |
| Specials - Starter | 1 核 Ryzen9 7950X | 1GB DDR5 | 25GB | 1TB | 500Mbps | $58.9/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=60) |
| Starter | 1 核 Ryzen9 7950X | 1GB DDR5 | 25GB | 1TB | 500Mbps | $18/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=58) |
| Standard | 2 核 Ryzen9 7950X | 2GB DDR5 | 40GB | 2TB | 500Mbps | $28/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=59) |

Ryzen9 7950X 是目前消费级单核性能的天花板之一，Geekbench 6 单核能跑到 2000+，跑 WordPress、编译、轻量数据库这类吃单核的活儿比 EPYC 还快。带宽给到 500Mbps，是优化线路里最高的。缺点是套餐档位少，最高只到 2 核 2GB。

**⑥ Los Angeles Global VPS — 国际线路（AMD EPYC 7002，1Gbps 大带宽）**

| 套餐 | CPU | 内存 | NVMe | 流量/月 | 带宽 | 价格 | 购买 |
|---|---|---|---|---|---|---|---|
| Specials - Lite | 1 核 EPYC 7002 | 512MB DDR4 | 15GB | 1TB | 1Gbps | $9.9/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=91) |
| Specials - Basic | 1 核 EPYC 7002 | 768MB DDR4 | 18GB | 1.5TB | 1Gbps | $12.9/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=92) |
| Specials - Starter | 1 核 EPYC 7002 | 1GB DDR4 | 20GB | 2TB | 1Gbps | $15/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=93) |
| Specials - Standard | 2 核 EPYC 7002 | 2GB DDR4 | 40GB | 4TB | 1Gbps | $25/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=94) |
| Specials - Pro | 3 核 EPYC 7002 | 4GB DDR4 | 60GB | 6TB | 1Gbps | $45/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=95) |
| Starter | 1 核 EPYC 7002 | 1GB DDR4 | 20GB | 2TB | 1Gbps | $8/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=84) |
| Standard | 2 核 EPYC 7002 | 2GB DDR4 | 40GB | 4TB | 1Gbps | $12/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=85) |
| Pro | 3 核 EPYC 7002 | 4GB DDR4 | 60GB | 6TB | 1Gbps | $20/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=86) |
| Premium | 4 核 EPYC 7002 | 6GB DDR4 | 80GB | 8TB | 1Gbps | $28/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=87) |

这是 ZgoCloud 最便宜的一条线，年付最低 $9.9 起步，1Gbps 带宽 + 大流量。代价是走国际线路（NTT/Cogent），不针对中国优化，国内直连延迟偏高、晚高峰可能掉速。适合做海外落地、代理节点、不面向国内用户的服务。**官方明确说明：国际线路套餐不支持因网络原因退款**。

**⑦ Los Angeles AMD VDS — 国际线路，支持 Windows（AMD EPYC 7003）**

| 套餐 | CPU | 内存 | NVMe | 流量/月 | 带宽 | 价格 | 购买 |
|---|---|---|---|---|---|---|---|
| Specials - Starter | 2 核 EPYC 7003 | 4GB DDR4 | 60GB | 10TB | 1Gbps | $66/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=125) |
| Specials - Standard | 4 核 EPYC 7003 | 8GB DDR4 | 150GB | 20TB | 1Gbps | $96/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=106) |
| Specials - Pro | 8 核 EPYC 7003 | 16GB DDR4 | 250GB | 20TB | 2Gbps | $166/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=107) |
| Specials - Premium | 12 核 EPYC 7003 | 24GB DDR4 | 500GB | 20TB | 2Gbps | $258/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=108) |
| Starter | 2 核 EPYC 7003 | 4GB DDR4 | 60GB | 10TB | 1Gbps | $24/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=124) |
| Standard | 4 核 EPYC 7003 | 8GB DDR4 | 150GB | 20TB | 1Gbps | $32/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=103) |
| Premium | 12 核 EPYC 7003 | 24GB DDR4 | 500GB | 20TB | 2Gbps | $76/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=105) |

VDS 严格说不是 VPS，资源是独享的，性能更接近独服。最大卖点是**支持用自带授权装 Windows**，流量动辄 10–20TB，适合跑 RDP 远程桌面、挂机软件、爬虫这类吃内存和流量的场景。

### 日本机房

日本有两个机房，东京和大阪，定位完全不同。

**⑧ Tokyo Intel VPS — BGP 大陆优化直连（Intel Xeon Gold 6248）**

| 套餐 | CPU | 内存 | NVMe | 流量/月 | 带宽 | 价格 | 购买 |
|---|---|---|---|---|---|---|---|
| Specials - Starter | 1 核 Xeon Gold 6248 | 1GB DDR4 | 10GB | 500GB | 100Mbps | $45/年 | [立即购买](https://bit.ly/zgovps) |
| Specials - Standard | 2 核 Xeon Gold 6248 | 2GB DDR4 | 20GB | 1TB | 100Mbps | $88/年 | [立即购买](https://bit.ly/zgovps) |
| Starter | 1 核 Xeon Gold 6248 | 1GB DDR4 | 10GB | 500GB | 100Mbps | $18/季 | [立即购买](https://bit.ly/zgovps) |
| Standard | 2 核 Xeon Gold 6248 | 2GB DDR4 | 20GB | 1TB | 100Mbps | $32/季 | [立即购买](https://bit.ly/zgovps) |
| Pro | 3 核 Xeon Gold 6248 | 3GB DDR4 | 30GB | 1.5TB | 100Mbps | $45/季 | [立即购买](https://bit.ly/zgovps) |
| Premium | 4 核 Xeon Gold 6248 | 4GB DDR4 | 50GB | 2TB | 100Mbps | $58/季 | [立即购买](https://bit.ly/zgovps) |

东京机房走 BGP 大陆优化直连，国内三网延迟都比较低（电信 50ms 左右、移动 40ms 左右），IP 自带流媒体解锁。CPU 是相对老一点的 Xeon Gold 6248，但跑轻量服务完全够。带宽卡在 100Mbps 是它的主要短板。

**⑨ Osaka AMD Performance VPS — IIJ 线路（AMD EPYC 9354P，DDR5 ECC + PCIe 4.0）**

| 套餐 | CPU | 内存 | NVMe | 流量/月 | 带宽 | 价格 | 购买 |
|---|---|---|---|---|---|---|---|
| Specials - Starter | 1 核 EPYC 9354P | 1GB DDR5 ECC | 20GB PCIe 4.0 | 1TB | 400Mbps | $12/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=43) |
| Specials - Standard | 2 核 EPYC 9354P | 2GB DDR5 ECC | 40GB PCIe 4.0 | 1TB | 800Mbps | $17/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=44) |
| Specials - Pro | 3 核 EPYC 9354P | 4GB DDR5 ECC | 80GB PCIe 4.0 | 1TB | 800Mbps | $24/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=45) |
| Starter | 1 核 EPYC 9354P | 1GB DDR5 ECC | 20GB PCIe 4.0 | 1TB | 400Mbps | $16/季 | [立即购买](https://bit.ly/zgovps) |
| Standard | 2 核 EPYC 9354P | 2GB DDR5 ECC | 40GB PCIe 4.0 | 2TB | 800Mbps | $22/季 | [立即购买](https://bit.ly/zgovps) |
| Pro | 3 核 EPYC 9354P | 4GB DDR5 ECC | 80GB PCIe 4.0 | 2TB | 800Mbps | $30/季 | [立即购买](https://bit.ly/zgovps) |
| Premium | 4 核 EPYC 9354P | 6GB DDR5 ECC | 100GB PCIe 4.0 | 2TB | 800Mbps | $40/季 | [立即购买](https://bit.ly/zgovps) |
| Ultra | 6 核 EPYC 9354P | 8GB DDR5 ECC | 120GB PCIe 4.0 | 2TB | 800Mbps | $52/季 | [立即购买](https://bit.ly/zgovps) |

大阪这条线用的是 EPYC 9004 Genoa 系列，是 ZgoCloud 全产品线里最新的 CPU，DDR5 ECC + PCIe 4.0 全线标配，带宽最高 800Mbps，标配 1 个 IPv4 + /64 IPv6。走的是 IIJ 线路——不针对中国优化，但日本本地和海外访问很稳，适合做日本本土业务、亚太节点、或者对 CPU 性能要求高的开发环境。

**⑩ Osaka AMD Ryzen9 Performance VPS — IIJ 线路（AMD Ryzen9 7950X）**

| 套餐 | CPU | 内存 | NVMe | 流量/月 | 带宽 | 价格 | 购买 |
|---|---|---|---|---|---|---|---|
| Specials - Lite | 1 核 Ryzen9 7950X | 512MB DDR5 ECC | 15GB PCIe 4.0 | 700GB | 400Mbps | $28/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=19) |
| Specials - Starter | 1 核 Ryzen9 7950X | 1GB DDR5 ECC | 20GB PCIe 4.0 | 1TB | 800Mbps | $38/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=20) |
| Starter | 1 核 Ryzen9 7950X | 1GB DDR5 ECC | 20GB PCIe 4.0 | 1TB | 800Mbps | $15/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=18) |
| Standard | 2 核 Ryzen9 7950X | 2GB DDR5 ECC | 40GB PCIe 4.0 | 2TB | 800Mbps | $25/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=21) |

单核性能最强的日本节点，IIJ 线路 + 800Mbps 大带宽，跑编译、跑测试环境非常爽。套餐档位同样偏少。

### 香港机房

**⑪ HongKong AMD VPS — BGP 三网直连（AMD EPYC 7002）**

| 套餐 | CPU | 内存 | NVMe | 流量/月 | 带宽 | 价格 | 购买 |
|---|---|---|---|---|---|---|---|
| Specials - Lite | 1 核 EPYC 7002 | 512MB DDR4 | 10GB | 300GB | 100Mbps | $36.8/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=123) |
| Specials - Starter | 1 核 EPYC 7002 | 1GB DDR4 | 10GB | 500GB | 100Mbps | $45/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=121) |
| Specials - Standard | 2 核 EPYC 7002 | 2GB DDR4 | 20GB | 1TB | 100Mbps | $88/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=122) |
| Starter | 1 核 EPYC 7002 | 1GB DDR4 | 10GB | 500GB | 100Mbps | $18/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=117) |
| Standard | 2 核 EPYC 7002 | 2GB DDR4 | 20GB | 1TB | 100Mbps | $32/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=118) |
| Pro | 3 核 EPYC 7002 | 3GB DDR4 | 30GB | 1.5TB | 100Mbps | $45/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=119) |
| Premium | 4 核 EPYC 7002 | 4GB DDR4 | 50GB | 2TB | 100Mbps | $58/季 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=120) |

香港机房主打"低延迟"——国内三网直连，电信/联通 30ms 以内，移动甚至能到 20ms 出头，是所有机房里离国内最近的。IP 自带流媒体解锁（Netflix、Disney+ 等）。缺点很直接：带宽只有 100Mbps，且价格是同配置里偏贵的。适合对延迟敏感、但对带宽不敏感的场景，比如远程桌面、小型 API 服务。

### 德国机房

**⑫ Falkenstein Intel VPS — 国际线路（Intel Xeon Gold 5412U，DDR5 + 1Gbps）**

| 套餐 | CPU | 内存 | NVMe | 流量/月 | 带宽 | 价格 | 购买 |
|---|---|---|---|---|---|---|---|
| Starter | 1 核 Xeon Gold 5412U | 1GB DDR5 | 20GB | 2TB | 1Gbps | $12.9/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=53) |
| Standard | 2 核 Xeon Gold 5412U | 2GB DDR5 | 40GB | 4TB | 1Gbps | $22.9/年 | [立即购买](https://clients.zgovps.com/?cmd=cart&action=add&affid=1247&id=54) |

德国 Falkenstein 是 ZgoCloud 性价比的另一极——$12.9/年就能拿到 1Gbps 带宽 + 2TB 流量 + DDR5 内存，折合每月一块多美元。CPU 是 Intel Xeon Gold 5412U（第四代至强），性能不弱。线路是纯国际网络，国内访问延迟 200ms+，不适合面向国内用户，但做欧洲本地业务、海外落地节点、爬虫代理非常划算。

## 当前可用优惠码

ZgoCloud 的优惠码体系比较简单，目前确认有效的主要是这一个：

- **`8NU44CM6LZ`** — 年付 **9.5 折循环优惠**，适用于所有常规套餐的年付周期，**续费同价**，有效期至 **2026 年 12 月 31 日**。下单时在结算页找到 "Use promotional code" 输入框，粘贴提交即可。

需要注意的是：

- Specials（特价款）**不能用优惠码**，价格已经是底价；
- 双 ISP 套餐、大阪 Ryzen9 Performance 系列、部分限时活动机型也不支持优惠码；
- 优惠码只在年付周期生效，季付/月付不打折。

除了优惠码，ZgoCloud 时不时还会搞"新购福利"活动——比如年付满 $46 可选带宽 +100Mbps、内存 +1GB、硬盘 +20GB 或流量 +100GB 四选一，购买后提交工单申请。这类活动不固定，下单前可以去官网活动页或者他们的 Telegram 频道看一眼最新动态。

## 不同需求怎么选：实操建议

光看参数表容易犯晕，下面按几种典型用途直接给结论。

**做面向国内用户的网站/博客**
首选洛杉矶 AMD EPYC 7003 系列（②）的 Starter 或 Standard，9929+CMIN2 三网优化，300Mbps 带宽够用，DDR4/DDR5 ECC 内存稳定。预算紧就蹲 Specials - Starter 年付 $36；想长期稳定就常规款年付 + 9.5 折优惠码。

预算更宽裕、追求单核性能，可以上 Ryzen9 Performance（⑤）Starter，$18/季 拿 1 核 7950X + 500Mbps，跑 WordPress 这种 PHP 应用飞快。

**做远程桌面/RDP/挂机**
直接看 VDS（⑦），自带 Windows 支持授权，2 核 4GB 起步，$66/年 或 $24/季。流量 10TB 起步，挂机软件、爬虫、自动化脚本都扛得住。

**做流媒体解锁/对 IP 归属敏感**
双 ISP 套餐（④）是专门为此设计的，IP 在主流库里显示为双 ISP，解锁成功率比普通原生 IP 高。Pro 档以上带宽 200Mbps，看 4K 不卡。

**追求极致低延迟**
香港机房（⑪），国内三网 30ms 以内，远程操作几乎无感。接受 100Mbps 带宽限制就行。

**预算极低的海外落地/代理**
Global VPS（⑥）Specials - Lite，$9.9/年 拿 1Gbps + 1TB 流量，是 ZgoCloud 最低门槛的入场券。国际线路，国内访问慢，但做海外节点刚好。

**日本本土业务/亚太节点**
大阪 EPYC 9354P（⑨），CPU 最新、带宽 800Mbps、DDR5 ECC，配置比东京高一代，价格还更便宜。IIJ 线路在日本本地和亚太表现稳定。

**欧洲业务/爬虫代理**
德国 Falkenstein（⑫），$12.9/年 起，1Gbps 大带宽 + 2TB 流量，欧洲 IP，做爬虫、做欧洲本地服务性价比拉满。

## 用户评价与真实体验

把几个中文测评社区和论坛里反复出现的反馈汇总一下，挑能交叉验证的说：

**正面反馈**

- **晚高峰表现稳**：多个测评博主在 21:00–23:00 晚高峰实测洛杉矶和大阪套餐，优化线路套餐的延迟和丢包都控制得不错，没有出现明显的"晚高峰跳水"。
- **CPU 性能货真价实**：AMD EPYC 7003、Ryzen9 7950X、Intel Platinum 8452Y 这些型号都是真硬件，Geekbench、UnixBench 跑分和官方标称一致，没有超卖嫌疑。有博主原话是"E5 上要等 1 分钟的命令这儿几秒就好了"。
- **商家诚信**：虽然成立时间不长（2021 年），但订单、续费、退款流程都规范，没出现过跑路、扣费异常这类硬伤。

**需要注意的点**

- **上行 QoS 阈值偏低**：有测评博主明确指出，ZgoCloud 部分套餐的上行带宽会被 QoS 限制在 25Mbps 左右，下行能跑满但上行不一定。如果你要做大文件上传、视频直播这类对上行敏感的事，下单前最好先开个低配实测一下。
- **国际线路套餐不支持网络原因退款**：Global、VDS、德国、大阪 IIJ 这几条线，官方明确写了"不支持因网络问题申请退款"。下单前要确认自己的网络环境能接受。
- **MaxMind 反欺诈检测较严**：购买时 IP 地址、电话号码、选择的国家三者必须保持一致（不要求信息真实，但要一致），否则会被判 Fraud 拒单。用代理下单的朋友尤其要注意。
- **特价款限量补货**：Specials 系列经常处于"缺货"状态，补货时间不固定，蹲到就下单，犹豫基本就没了。

## 购买流程与注意事项

ZgoCloud 用的是标准 WHMCS 系统，下单流程不复杂：

1. 选套餐 → 进入购物车，选计费周期（年付/季付）；
2. 有优惠码的在这一步输入 `8NU44CM6LZ`，点 Apply；
3. 填账户信息——**国家、电话、IP 三者要一致**，否则容易被 MaxMind 拦；
4. 选支付方式（PayPal / Stripe 信用卡 / 支付宝）；
5. 付款后机器一般几分钟内自动开通，IP 和 root 密码发邮件。

几个容易踩的坑提前说：

- **IP 更换**：每月可申请 1 次，每台 VPS 最多 3 次，普通 IP 收 $6/次，ISP IP 收 $10/次，只适用 IPv4。
- **退款政策**：常规套餐支持 3 天内、流量不超过 10GB 全额退款；Specials 特价款不退款；国际线路套餐不支持因网络原因退款。
- **续费价格**：常规套餐用优惠码下单的，续费同价（这点比很多家厚道，不少商家续费会涨回原价）。
- **支持**：工单系统 + Telegram 频道，响应速度看时段，紧急问题建议直接工单。

## 常见问题

**Q：ZgoCloud 支持支付宝吗？**
支持。除了 PayPal 和 Stripe（信用卡），支付宝是默认支付选项之一，国内用户付款无障碍。

**Q：特价款（Specials）和常规款有什么区别？**
Specials 是限量年付特价，价格最低但不可退款、不能用优惠码、库存有限；常规款按季付/年付长期在售，可用 9.5 折优惠码，支持 3 天内退款。

**Q：哪个套餐最适合做站？**
面向国内用户首选洛杉矶 AMD EPYC 7003 系列（9929+CMIN2）的中配套餐；面向海外用户选 Global VDS 或德国 Falkenstein。

**Q：能装 Windows 吗？**
只有 Los Angeles AMD VDS（⑦）官方明确支持用自带授权装 Windows。其他套餐默认只提供 Linux 系统，想装 Windows 得自己想办法（且可能违反 TOS）。

**Q：优惠码续费还能用吗？**
`8NU44CM6LZ` 是循环优惠，续费时同样 9.5 折，只要在有效期内（2026 年 12 月 31 日前）都有效。

**Q：双 ISP IP 和普通原生 IP 有什么区别？**
双 ISP IP 在 IP2Location 之外的主流 IP 库（MaxMind、IPinfo 等）都会显示为双 ISP 归属，对某些流媒体和服务的解锁成功率更高；普通原生 IP 只显示为数据中心 IP。如果你不做流媒体解锁，普通原生 IP 完全够用，没必要多花一倍价钱上双 ISP。

## 写在最后

ZgoCloud 这个牌子用到现在，最直接的感受是"知道自己要做什么"——它没有铺一堆华而不实的高配套餐，而是在中等配置上把线路和价格打磨到位。三网优化线路确实是它的护城河，洛杉矶那几条 9929+CMIN2 的线，晚高峰的稳定性在同价位里很难找到对手；国际线路和德国机房又把"便宜大碗"这件事做到了 $9.9/年 这个量级。

如果你正在挑第一台海外 VPS，或者想从某家老牌但越来越拉胯的商家换出来，ZgoCloud 的洛杉矶优化线路套餐值得试一台。先用低配 Specials 跑一两个月，确认网络和性能符合预期再加配，比一次到位稳妥。所有套餐下单都走 👉 [这个链接](https://bit.ly/zgovps) 进官网，别从第三方跳转，免得优惠码和售后对不上号。
