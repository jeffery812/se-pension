# 瑞典养老金体系 · se-pension

一份用中文介绍瑞典养老金体系（Det svenska pensionssystemet）的单页网站，面向在瑞典工作和生活的中文读者。

**在线访问：<https://jeffery812.github.io/se-pension>**

## 页面内容

| 章节 | 内容 |
|---|---|
| 00 三层结构 | 国家养老金、职业养老金、私人储蓄，按 2024 年全国实际发放金额等比例显示，国家养老金再细分为收入养老金、补充养老金、保障养老金、积累养老金和收入养老金补贴 |
| 图 互动图解 | 月薪计算器：拖动月薪，实时显示每月进入收入养老金、积累养老金和 ITP1 的金额，并用折线图标出国家养老金封顶（约 56 048 kr）和 ITP1 改按 30% 缴费（52 125 kr）这两个拐点 |
| 01 国家养老金 | 18.5% 缴费、名义账户与自动平衡机制、AP7 Såfa、保障养老金、领取年龄 |
| 02 职业养老金 | ITP1、ITP2、SAF-LO、AKAP-KR、PA16 等集体协议对比 |
| 03 私人储蓄 | IPS、ISK、KF |
| 04 税务 | 养老金的征税方式与 66 岁以上的税收优惠 |
| 05 实用工具 | 橙色信封、minpension.se、pensionsmyndigheten.se |
| 06 外籍居民 | 哪些养老金能带出瑞典、欧盟社保协调，以及瑞典与中国之间没有社保协定 |

## 使用

直接打开在线页面：<https://jeffery812.github.io/se-pension>

整个网站只有一个文件 `index.html`，不需要构建，也没有依赖，本地也可以直接打开：

```sh
open index.html        # macOS
```

页面通过 GitHub Pages 从 `main` 分支发布，推送到 `main` 后会自动更新。字体从 Google Fonts 加载，离线时会退回系统字体。

## 数据来源

- 三层结构比例：Pensionsmyndigheten《Årsredovisning 2024》表 19（国家养老金各部分），以及《Sveriges pensioner 2006–2024》表 1（职业养老金和私人养老金）
- 月薪计算器使用以下规则：
  - 国家养老金 = (月薪 − 7% 养老金费) × 18.5%（其中 16% 进收入养老金，2.5% 进积累养老金），上限为 7.5 个收入基数
  - ITP1：7.5 IBB/12 以下部分按 4.5%，以上部分按 30%
  - 2026 年收入基数（inkomstbasbelopp）按 83 400 kr 计，修改 `index.html` 脚本中的 `IBB` 常量即可更新

## 免责声明

本页面仅作概览性介绍，不构成财务或法律建议。收入基数、领取年龄和缴费率每年都会调整，具体请以 [Pensionsmyndigheten](https://www.pensionsmyndigheten.se)、[minpension.se](https://www.minpension.se) 和你所在的集体协议为准。
