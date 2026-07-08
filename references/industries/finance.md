# 金融 Router

Use with `references/industry-module-framework.md`. This is a routing module, not a concrete playbook. Use it only when the user says `金融` or `金融行业` and the exact subcategory is unclear.

Source: row 27 `金融行业观点情绪选题生成器`, converted into a router because it overlaps with several narrower regulated modules.

## Aliases

- 金融
- 金融行业
- 金融产品
- 金融服务

## Use When

- The request only says financial industry, financial product, or financial services without a clear subcategory.
- The task is to choose the correct finance-related module before creating topics, scripts, or private-domain conversion.

## Do Not Use When

- Use `personal-finance.md` for ordinary household理财, budgeting, emergency funds, and basic asset allocation.
- Use `stocks-futures.md` for stock/futures trading, investor education, or market psychology.
- Use `financing-loans.md` for new loans, financing qualification, approval, rates, or business cash turnover.
- Use `debt-optimization.md` for existing debt pressure, overdue accounts, repayment sequence, or negotiation preparation.
- Use `wealth-management.md` for high-income family asset allocation and wealth preservation planning.
- Use `high-net-worth.md` for high-net-worth audience identity, privacy, inheritance, and family governance.
- Use `insurance.md` for coverage, policies, claims, exclusions, and family protection planning.
- Use `blockchain-web3.md` for Web3, crypto, wallet safety, or project due diligence.

## Routing Table

| User Says | Load |
| --- | --- |
| 理财、家庭资产、备用金、退休规划 | `personal-finance.md` |
| 股票、期货、交易、仓位、市场情绪 | `stocks-futures.md` |
| 融资、贷款、放款、利率、企业周转 | `financing-loans.md` |
| 负债、逾期、协商、上岸、还款顺序 | `debt-optimization.md` |
| 财富管理、资产配置、家族目标 | `wealth-management.md` |
| 高净值、隐私、传承、家族治理 | `high-net-worth.md` |
| 保险、保单、理赔、保障规划 | `insurance.md` |
| 区块链、Web3、钱包、项目尽调 | `blockchain-web3.md` |

## Compliance Notes

Financial content is regulated and high-risk. Do not recommend specific products, securities, loans, policies, crypto assets, or guaranteed returns. State assumptions and require source verification for laws, rates, fees, yield, approval, tax, and suitability claims.
