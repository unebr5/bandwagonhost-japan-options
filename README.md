# BandwagonHost Japan：东京/大阪机房怎么选，三大线路套餐价格与限量款购买指南

搜"BandwagonHost Japan"的人，多半卡在同一个问题上：这家以 CN2 GIA 线路闻名的 VPS 商家，日本方向到底有哪几个机房、线路差在哪、哪款套餐值得买。这篇文章把搬瓦工目前日本方向的所有在售方案整理清楚——包括价格比较高的东京/大阪 CN2 GIA 系列、能买到软银线路的 CN2 GIA-E 系列，以及常年断货的限量款，最后按运营商给出选择建议。

## 先搞清楚：搬瓦工在日本有哪几个机房

搬瓦工（BandwagonHost，IT7 旗下品牌）目前在日本方向公开运营三个机房，加上一个限量款专用的东京机房，实际可选的位置是四个：

| 机房编号 | 位置 | 线路 | 标称带宽 | 套餐获取方式 |
| --- | --- | --- | --- | --- |
| JPTYO_8 | 东京 Equinix TY8 | 三网回程 CN2 GIA | 1.2 Gbps | TOKYO CN2 GIA 专属套餐 |
| JPOS_6 | 大阪 Equinix | 三网回程 CN2 GIA | 1.5 Gbps | OSAKA CN2 GIA 专属套餐 |
| JPOS_1 | 大阪 Equinix OS1（软银 Softbank / bbtec） | 软银线路 | 2.5 Gbps | CN2 GIA-E 套餐内切换 |
| DC39v2 | 东京 | 三网 CMI 直连混合线路 | 2.5–5 Gbps | The Tokyo Plan 限量款 |

这里要先说清楚一个容易混淆的点：JPOS_1 是搬瓦工日本方向唯一的软银线路机房，但它没有独立套餐系列，只能通过购买 CN2 GIA-E 套餐后在 KiwiVM 面板里免费迁移过去。而 JPTYO_8 和 JPOS_6 的 CN2 GIA 套餐是独立系列，买哪个就只能用哪个机房（CN2 GIA-E 除外，它可以在十几个机房之间自由切换，JPOS_1 就是选项之一）。

三个常规机房的数据中心都在 Equinix，软银机房对等的还是 Equinix OS1，官方标注支持 Google、Cloudflare、NTT、Softbank 等 peering，所有套餐都带 1–10 Gbps 上联。

## 东京 CN2 GIA（JPTYO_8）：日本方向的天花板，价格也是天花板

JPTYO_8 是搬瓦工日本线路里定位最高的机房：三网回程 CN2 GIA，去程电信联通移动直连，带宽 1.2 Gbps。这个机房最大的意义是给电信用户提供一个直连日本的 CN2 GIA 选择——电信 CN2 GIA 的线路成本极高（官方在 CN2 GIA 介绍页里提到过每 Mbps 转接成本可达上百美元量级），所以这个系列的定价也明显高于普通套餐。

目前 JPTYO_8 共 6 档配置，月付和年付价格如下：

| 套餐 | 内存 | CPU | 硬盘 | 月流量 | 带宽 | 月付 | 年付 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| TOKYO 40G | 2 GB | 2 核 | 40 GB | 500 GB | 1.2 Gbps | $89.99 | $899.99 | [ 查看 Tokyo CN2 GIA 入门款](https://bandwagonhost.com/aff.php?aff=79616&pid=108) |
| TOKYO 80G | 4 GB | 4 核 | 80 GB | 1 TB | 1.2 Gbps | $155.99 | $1559.99 | [ 购买 Tokyo 80G 方案](https://bandwagonhost.com/aff.php?aff=79616&pid=109) |
| TOKYO 160G | 8 GB | 6 核 | 160 GB | 2 TB | 1.2 Gbps | $299.99 | $2999.99 | [ 选购 Tokyo 160G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=110) |
| TOKYO 320G | 16 GB | 8 核 | 320 GB | 4 TB | 1.2 Gbps | $589.99 | $5899.99 | [ 下单 Tokyo 320G 配置](https://bandwagonhost.com/aff.php?aff=79616&pid=111) |
| TOKYO 640G | 32 GB | 10 核 | 640 GB | 6 TB | 1.2 Gbps | $989.99 | $9989.99 | [ 查看 Tokyo 640G 大盘鸡](https://bandwagonhost.com/aff.php?aff=79616&pid=123) |
| TOKYO 1280G | 64 GB | 12 核 | 1280 GB | 8 TB | 1.2 Gbps | $1889.99 | $18989.99 | [ 选购 Tokyo 旗舰配置](https://bandwagonhost.com/aff.php?aff=79616&pid=125) |

这套方案的定位很明确：预算充足、对电信方向线路质量有硬需求的企业或进阶用户。月付 $89.99 起步的价格决定了它不是入门首选——如果你是电信用户但预算有限，后面的大阪 CN2 GIA 会更实际。

## 大阪 CN2 GIA（JPOS_6）：同样是 CN2 GIA，门槛低了一半

JPOS_6 是搬瓦工后来上线的大阪 CN2 GIA 机房，规格上和东京 JPTYO_8 一个思路：三网回程 CN2 GIA（去程三网接入，回程电信走 CN2 GIA/CTG），但带宽给到 1.5 Gbps，价格却便宜了不少——同规格配置下，大阪比东京每月便宜 $40 左右。

| 套餐 | 内存 | CPU | 硬盘 | 月流量 | 带宽 | 月付 | 年付 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| OSAKA 40G | 2 GB | 2 核 | 40 GB | 500 GB | 1.5 Gbps | $49.99 | $499.99 | [ 购买 Osaka CN2 GIA 入门款](https://bandwagonhost.com/aff.php?aff=79616&pid=134) |
| OSAKA 80G | 4 GB | 4 核 | 80 GB | 1 TB | 1.5 Gbps | $86.99 | $869.99 | [ 查看 Osaka 80G 方案](https://bandwagonhost.com/aff.php?aff=79616&pid=135) |
| OSAKA 160G | 8 GB | 6 核 | 160 GB | 2 TB | 1.5 Gbps | $165.99 | $1665.99 | [ 选购 Osaka 160G 套餐](https://bandwagonhost.com/aff.php?aff=79616&pid=136) |
| OSAKA 320G | 16 GB | 8 核 | 320 GB | 4 TB | 1.5 Gbps | $329.99 | $3199.00 | [ 下单 Osaka 320G 配置](https://bandwagonhost.com/aff.php?aff=79616&pid=137) |
| OSAKA 640G | 32 GB | 10 核 | 640 GB | 6 TB | 1.5 Gbps | $549.99 | $5549.99 | [ 查看 Osaka 640G 方案](https://bandwagonhost.com/aff.php?aff=79616&pid=138) |
| OSAKA 1280G | 64 GB | 12 核 | 1280 GB | 8 TB | 1.5 Gbps | $1059.99 | $10559.99 | [ 选购 Osaka 旗舰配置](https://bandwagonhost.com/aff.php?aff=79616&pid=139) |

月付 $49.99 / 年付 $499.99 的入门款，是目前能买到"真·日本 CN2 GIA"的最低门槛。根据第三方测评站的近期实测记录，这个机房的新批次节点已经换用 AMD EPYC 平台，性能表现比早期 Xeon 批次有明显提升。对于电信用户来说，如果觉得东京太贵，大阪 JPOS_6 基本是同线路质量下的平替首选；大阪到中国大陆的物理距离只比东京远一点点，延迟差距通常不如线路本身的影响大。

## 大阪软银 JPOS_1：联通用户的宝藏机房，通过 CN2 GIA-E 套餐购买

JPOS_1 走的是软银（Softbank / bbtec）线路，2.5 Gbps 带宽。软银线路的特点是联通方向直连质量极好——第三方实测数据里，JPOS_1 到联通节点的延迟普遍在 60–90ms 区间，路由直接从软骨干网进入联通 4837，不绕路；电信和移动方向的表现则取决于软银的对等互联，整体延迟大致在 60–140ms 之间浮动。一句话总结：**联通用户选软银，性价比极高；电信用户优先 CN2 GIA**。

购买方式是买 CN2 GIA-E 套餐，然后在 KiwiVM 面板里把机房迁到 JPOS_1（迁移免费、不丢数据）。CN2 GIA-E 是搬瓦工最经典的系列，可以在 DC6、DC9、JPOS_1、荷兰等十几个机房之间随时切换，入门档 2.5 Gbps 起步：

| 套餐 | 内存 | CPU | 硬盘 | 月流量 | 带宽 | 季付 | 年付 | 购买 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| CN2 GIA-E 20G | 1 GB | 2 核 | 20 GB | 1 TB | 2.5 Gbps | $49.99 | $169.99 | [ 购买 CN2 GIA-E 入门款（可迁 JPOS_1）](https://bandwagonhost.com/aff.php?aff=79616&pid=87) |
| CN2 GIA-E 40G | 2 GB | 3 核 | 40 GB | 2 TB | 2.5 Gbps | $89.99 | $299.99 | [ 查看 CN2 GIA-E 40G 方案](https://bandwagonhost.com/aff.php?aff=79616&pid=88) |
| CN2 GIA-E 80G | 4 GB | 4 核 | 80 GB | 3 TB | 2.5 Gbps | $56.99 | $549.99 | [ 选购 CN2 GIA-E 80G](https://bandwagonhost.com/aff.php?aff=79616&pid=89) |
| CN2 GIA-E 160G | 8 GB | 6 核 | 160 GB | 5 TB | 5 Gbps | $86.99 | $879.99 | [ 购买 CN2 GIA-E 160G](https://bandwagonhost.com/aff.php?aff=79616&pid=90) |
| CN2 GIA-E 320G | 16 GB | 8 核 | 320 GB | 8 TB | 5 Gbps | $159.99 | $1599.99 | [ 选购 CN2 GIA-E 320G](https://bandwagonhost.com/aff.php?aff=79616&pid=91) |
| CN2 GIA-E 640G | 32 GB | 10 核 | 640 GB | 10 TB | 10 Gbps | $289.99 | $2759.99 | [ 查看 CN2 GIA-E 640G](https://bandwagonhost.com/aff.php?aff=79616&pid=92) |
| CN2 GIA-E 1280G | 64 GB | 12 核 | 1280 GB | 12 TB | 10 Gbps | $549.99 | $5399.99 | [ 选购 CN2 GIA-E 1280G](https://bandwagonhost.com/aff.php?aff=79616&pid=93) |
| CN2 GIA-E 1280G 大流量 | 64 GB | 12 核 | 1280 GB | 15 TB | 10 Gbps | $679.00 | $6790.00 | [ 查看 15TB 流量版](https://bandwagonhost.com/aff.php?aff=79616&pid=160) |
| CN2 GIA-E 1280G 超大流量 | 64 GB | 12 核 | 1280 GB | 20 TB | 10 Gbps | $899.00 | $8999.00 | [ 查看 20TB 流量版](https://bandwagonhost.com/aff.php?aff=79616&pid=161) |
| CN2 GIA-E 1280G 多核 | 64 GB | 24 核 | 1280 GB | 12 TB | 10 Gbps | $749.99 | $7599.00 | [ 查看 24 核版](https://bandwagonhost.com/aff.php?aff=79616&pid=148) |

[👉 查看全部在售套餐与当前库存](https://bit.ly/BandwagonHost)

对大多数人来说，第一档 $169.99/年的 20G 方案就够用了：1GB 内存、1TB 月流量、2.5Gbps 端口，买完迁到 JPOS_1 就是软银线路。它是搬瓦工日本方向最便宜的正规姿势，缺点只有两个——内存偏小，以及软银机房的库存经常紧张（迁移选项有没有货以面板实际显示为准）。

## 限量款：The Tokyo Plan v2 和日本软银限量版

除了常规系列，搬瓦工这两年在日本方向连续放了几波限量套餐，配置和价格都相当激进，但共同点是：**限量发售、售完即止、不可迁移机房**。

**The Tokyo Plan v2**（$99/年）：2 核 AMD、2GB 内存、40GB SSD、1000GB 月流量、5Gbps 带宽，位于东京 DC39v2 机房，三网直连、回程接入 CMI。它是所有限量款里带宽最高的，对移动用户尤其友好——CMI 是移动自己的国际出口，移动方向直连质量好。前代 The Tokyo Plan（$79/年，1核/1GB/20GB/500GB/2.5Gbps）配置全面减半，两者定位就是"低配走量"和"加量主力"的关系。

**日本大阪软银限量版**（$79.99/年）：1 核、2GB 内存、40GB SSD、2000GB 月流量、2.5Gbps，固定 JPOS_1 机房。相当于把 CN2 GIA-E 里最便宜的软银姿势直接做成了固定套餐，流量还翻倍，同样是联通方向的好选择。早年还有一款 $69.99/年、512MB/10GB/500GB 的入门"传家宝"版本，基本处于长期售罄状态。

限量款的现实问题是抢不到。这几款常年处于断货-补货循环，想要的话只能蹲库存通知，[👉 前往官方页面确认限量款是否有货](https://bit.ly/BandwagonHost)。如果限量款无货，退而求其次买 CN2 GIA-E 迁 JPOS_1，或者直接上大阪 CN2 GIA，都是可行的替代路径。

## 怎么选：按你的运营商对号入座

选日本 VPS，机房位置其实是次要的，线路才是决定体验的关键。结合三个机房的线路特性和第三方实测数据，选择逻辑可以简化成这样：

1. **电信用户**：首选 CN2 GIA。预算充足选东京 JPTYO_8，追求性价比选大阪 JPOS_6。电信走 163 骨干网晚高峰拥堵严重，CN2 GIA 是目前电信方向体验最稳的商用线路。
2. **联通用户**：大阪软银 JPOS_1 性价比最高。联通到日本软银是直连，晚高峰表现甚至不输 CN2 GIA，而 $169.99/年的价格只有东京 CN2 GIA 的五分之一。
3. **移动用户**：关注 CMI 直连的 The Tokyo Plan v2（限量），买不到再看软银 JPOS_1 或 CN2 GIA 系列——软银和 CN2 GIA 对移动方向的接入也都不差。
4. **纯粹需要一台日本 VPS、不挑剔线路**：CN2 GIA-E 入门款 $169.99/年，反正可以在十几个机房随便切，试错成本最低。

## 优惠与省钱：循环折扣码 + 计费周期

搬瓦工的折扣体系比较简单，主要靠两件事：

**循环优惠码**。搬瓦工长期维持一个约 6.77%–6.78% 的循环折扣码（BWHCGLUKKB 用了很多年，第三方优惠信息站显示它在 2026 年的大多数时间仍处于可用状态；官方偶尔会在大促期间更换新码）。"循环"的意思是续费同样有效，不是只优惠首单。以 CN2 GIA-E 入门款为例，$169.99/年 用码后大约 $158/年，一年省十来美元；大阪 CN2 GIA $499.99/年 的方案能省 $30 出头。付款前在结账页输入当期有效码即可，具体哪个码活着，以下单页实测为准。

**选长计费周期**。几乎所有套餐年付都比按月付划算：大阪 CN2 GIA 月付 $49.99，年付折合 $41.66/月；东京 CN2 GIA 年付折合 $75/月。CN2 GIA-E 入门款干脆没有月付选项，最低从季付 $49.99 起步。

另外两个购买前值得知道的规则：搬瓦工提供 **30 天退款保障**（常规套餐，官方页面标注 99.9% 在线率保障），买错了不至于砸手里；所有套餐都是 **自主管理**（self-managed），官方不提供代维，出问题靠自己通过 KiwiVM 面板和工单解决——这也是它能维持这个价格体系的原因。

## 常见问题

**BandwagonHost 的日本 VPS 能跑满带宽吗？**
常规套餐共享端口，限量款和 CN2 GIA 系列的 CPU 配额在官方服务条款里有明确限制（例如 The Tokyo Plan v2 限制为单核 45% 的长期用量），跑持续高负载会被限速。官方条款页对各套餐的 CPU 用量规则写得非常细，买前可以翻一下。

**买错了机房能换吗？**
分套餐：CN2 GIA-E 和 KVM PROMO 这类多机房套餐可以在面板里免费迁移、不丢数据；TOKYO/OSAKA CN2 GIA 专属套餐和所有限量款绑定机房，不可迁移。下单前想清楚这一点。

**需要备案或实名吗？**
不需要。搬瓦工是海外商家，自助开通，支持支付宝/ PayPal 等常见付款方式，开机即用，IPv4 + IPv6(/64) 都会分配。

**日本机房和香港机房怎么选？**
两地延迟都在低延迟区间，香港 CN2 GIA 套餐起步价和东京持平（$89.99/月），但香港流量给得更少（500GB/月，同价）。日本方向胜在带宽更大（1.2–1.5Gbps vs 1Gbps）、限量的 Tokyo Plan v2 性价比突出。如果主要服务中国大陆电信用户，两地 CN2 GIA 都值得考虑，剩下的差别就是你对东京还是香港节点有偏好。

**总结一下**：搬瓦工日本方向的选择其实就三条线——电信认 CN2 GIA（东京高端、大阪平价），联通认软银 JPOS_1（CN2 GIA-E 迁移或限量款），移动蹲 CMI 的 The Tokyo Plan v2。限量款看运气，常规款随时能买。下单前记得套上循环优惠码，年付比月付划算，30 天内不满意还能退。
