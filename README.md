# 跨境账桥 · BorderLedger

**BorderLedger v2.1 — Zyla（美国）× 万里汇 WorldFirst（香港）× TikTok Shop US**

正式网站：https://templehao.github.io/borderledger/

收款有路径，付款有依据，税务有底稿。

## 核心假设

- TikTok Shop US 的开店/商品销售主体是美国公司。
- 香港合作企业和美国公司为**彼此独立的法人实体**，双方发生真实贸易或服务交易。
- **Zyla 是美国市场品牌**，由 AUS Merchant Services, Inc. 提供服务；**WorldFirst（万里汇）是香港等地区的产品品牌**。不能把美国服务一律称为 WorldFirst。
- **万里汇与 Zyla 解决收款、支付和跨境资金流转，不替客户申报或缴纳所得税**；美国及香港税务需另委托适当专业人员处理。

## 两层业务选型

**第一层：TikTok Shop US 的平台结算。**

1. 美国公司名下 Zyla 收款账户：Zyla 官方有 TikTok 收款教程，实际仍需通过平台/服务商审查。
2. 香港 WorldFirst 收款账号 + 美国店铺持有人：万里汇确有修改店铺持有人的流程，但**跨独立法人、不同地区、具体 TikTok US 平台的准入**不得仅凭该功能推定；须有书面审核结论。
3. 美国公司名下银行账户：传统同名 ACH 结算路径。

**第二层：KA 单向资金互转。**

- 配置 A：**美国 Zyla → 香港 WorldFirst**。
- 配置 B：**香港 WorldFirst → 美国 Zyla**。
- 业务提供的 KA 机制要求**一组配置只能二选一，不可同时双向启用**；上线前由专属客户经理确认客户白名单、账户资格、方向、地区、限额、币种和费用。
- WorldFirst 官方公开了 WorldFirst → Zyla 转账操作，提示同币种转账；反向及 KA 排他性以业务资料和审核为准，不应视作面向全体商户的通用条款。

以上两层可以独立选型，均不能取代真实商业合同和税务归属认定。

## 网站组件

- Zyla / WorldFirst 品牌区分及公开官方规则
- TikTok Shop 美国店铺的三种收款路径（可切换）
- KA 双方向候选、**单选互斥**的资金流向可视化
- 收付轨道与税务轨道并行的职责说明
- 美国 C-Corp / 香港公司示意所得税计算器（不随收款通道切换）
- 12 项账户、平台、合同与税务验证清单，状态仅在浏览器本地保存
- 原始官方资料链接与争议/待验证条款标注

## 技术与部署

- 静态 `index.html` + `favicon.svg`，不依赖服务端、API Key 或支付工具账号。
- 使用 `.github/workflows/pages.yml` GitHub Actions 自动部署到 GitHub Pages。
- GitHub Pages Settings → Build and deployment → Source 应为 **GitHub Actions**。
- 推送至 `main` 即触发自动部署。

## 来源

- [Zyla 官方 TikTok Shop 收款](https://www.zyla.com/help-center/receiving-money-from-marketplaces/tiktokshop/)
- [Zyla 服务条款](https://www.zyla.com/disclaimer-policies/terms-and-conditions/)
- [万里汇：如何转账至 Zyla](https://www.worldfirst.com.cn/content/articles/b2b_gbl_portal/transfertoZyla)
- [万里汇：店铺持有人与错名收款](https://www.worldfirst.com.cn/content/articles/rlny8jsi/uuyf4tgh)
- [TikTok US 企业店铺结算账户帮助](https://seller-us.tiktok.com/university/essay?knowledge_id=2404078778124034)
- [IRS Form 1120 instructions](https://www.irs.gov/instructions/i1120)
- [香港税务局：两级制利得税](https://www.ird.gov.hk/eng/faq/2tr.htm)

**研究用途声明**：所有税负计算为简化教学示例，均非税务法律意见、税务申报服务或产品准入保证。KA 互转政策源自客户侧业务条件，并不表示所有客户/地域已开放。任何实际资金交易需独立验证公司关系、资金权属及相关税务处理。
