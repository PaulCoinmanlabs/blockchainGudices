# 稳定币（Stablecoin）：为什么它会出现？

## 1.什么是稳定币
稳定币（Stablecoin）是一类锚定现实世界资产（如美元）的数字货币，设计目的是在加密市场中提供价格稳定性。它通常挂钩于：
- 美元（最常见）
- 欧元、人民币等法币
- 黄金、甚至 CPI 指数等资产

## 2.为什么需要稳定币？
### 2.1. 加密货币波动性太大
| BTC                  | ETH                 |
| -------------------- | ------------------- |
| 价格波动剧烈，24小时内可涨跌10%以上 | 难以作为“日常支付”和“资产计价单位” |

> 用户很难用这些资产稳定交易，也不利于 DeFi 等金融操作。

### 2.2. 2. 解决链上“美元”问题
传统的 USDT、美元只存在银行账户里，无法直接用于区块链操作，比如：
- 链上支付/结算
- DeFi 抵押/借贷/流动性池
- NFT 挂单、DAO 资金管理

> 需要一种能在链上自由流通，但价值又稳定的“数字美元”。

### 2.3. 更强的跨境金融属性
稳定币无国界，低门槛，特别适合以下场景：
- 向海外打款（绕过繁复的 SWIFT）[SWIFT（Society for Worldwide Interbank Financial Telecommunication）是全球银行之间转账用的通信网络]
- 在不稳定国家保值（如阿根廷/委内瑞拉）
- Web3团队全球结算工资

## 3.稳定币如何解决问题？
| 问题             | 稳定币如何应对                       |
| -------------- | ----------------------------- |
| 加密货币剧烈波动       | 锚定美元或实物资产，保持 1:1 稳定性          |
| 法币难以链上使用       | 通过 USDT / USDC / DAI 实现链上“美元” |
| 去中心化金融需要稳定抵押物  | 稳定币是 DeFi 世界的主流结算单位           |
| 跨境转账难、慢、贵      | 稳定币秒级到账、0手续费（部分链）             |
| Web3 薪资、奖金如何发？ | 用稳定币可避免汇率风险和监管复杂性             |

## 4.常见稳定币类型
| 类型      | 示例         | 原理             | 风险点          |
| ------- | ---------- | -------------- | ------------ |
| 中心化稳定币  | USDT、USDC  | 储备美元托管，1:1 可兑换 | 中心化风险、监管审查   |
| 去中心化稳定币 | DAI、crvUSD | 超额抵押 + 清算机制    | 锚定机制复杂、风险积压  |
| 算法稳定币   | UST（已崩溃）   | 依赖市场套利和通缩机制维稳  | 易死亡螺旋、高系统性风险 |

<div class="stablecoin-cards">

  <div class="stablecoin-card">
    <h3>USDT（Tether）</h3>
    <p><strong>发行方：</strong> Tether Limited（与 Bitfinex 关联）</p>
    <p><strong>类型：</strong> 中心化法币抵押型</p>
    <p><strong>特点：</strong></p>
    <ul>
      <li>加密市场流通最广的稳定币</li>
      <li>多链支持（ERC20、TRC20、Solana等）</li>
      <li>在亚洲、发展中国家普及度极高</li>
    </ul>
    <p><strong>争议：</strong> 储备不透明，曾被罚款</p>
  </div>

  <div class="stablecoin-card">
    <h3>USDC（Circle）</h3>
    <p><strong>发行方：</strong> Circle & Coinbase 联合推出</p>
    <p><strong>类型：</strong> 中心化法币抵押型</p>
    <p><strong>特点：</strong></p>
    <ul>
      <li>合规性高，美国监管机构支持</li>
      <li>每月审计，透明度强</li>
      <li>DeFi 协议首选（MakerDAO、Aave 等）</li>
    </ul>
    <p><strong>风控：</strong> 可被冻结指定地址</p>
  </div>

  <div class="stablecoin-card danger">
    <h3>UST（已崩盘）</h3>
    <p><strong>发行方：</strong> Terraform Labs</p>
    <p><strong>类型：</strong> 算法稳定币</p>
    <p><strong>机制：</strong> 通过 LUNA 铸销保持挂钩</p>
    <p><strong>崩盘过程：</strong></p>
    <ul>
      <li>2022 年 5 月市场恐慌导致脱锚</li>
      <li>LUNA 无限增发 → 死亡螺旋</li>
      <li>400 亿美元市值蒸发</li>
    </ul>
    <p><strong>结果：</strong> 项目死亡，分叉为 Terra 2.0</p>
  </div>

</div>

<!-- 公共提示 -->
<div class="card-footer">
  <strong>⚠️ 提醒：</strong> 稳定币 ≠ 永远稳定，使用前应了解其机制与风险，切勿盲目押注。
</div>

<style>
.stablecoin-cards {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  margin-bottom: 1rem;
}
.stablecoin-card {
  flex: 1 1 300px;
  background: #f7f7f9;
  border-left: 5px solid #2d8cf0;
  padding: 1rem;
  border-radius: 10px;
  box-shadow: 0 0 8px rgba(0,0,0,0.05);
}
.stablecoin-card h3 {
  margin-top: 0;
}
.stablecoin-card ul {
  padding-left: 1.2rem;
}
.stablecoin-card.danger {
  border-left-color: #f56c6c;
  background: #fff4f4;
}
.card-footer {
  margin-top: 1rem;
  padding: 1rem;
  background: #fffbe6;
  border-left: 5px solid #faad14;
  border-radius: 6px;
  font-size: 0.95rem;
}
</style>
---

| 稳定币  | 类型    | 是否中心化 | 是否合规       | 崩盘风险  | 用途广泛性        |
| ---- | ----- | ----- | ---------- | ----- | ------------ |
| USDT | 法币储备型 |  是   |  否（多次被质疑） | 中等    |  最广         |
| USDC | 法币储备型 |  是   |  是        | 低     |  合规 DeFi 首选 |
| UST  | 算法型   |  否   |  否        |  极高 |  已废         |


## UST崩盘前后

<div class="timeline-ust">

  <div class="ust-event">
    <div class="date">2020年9月</div>
    <h4>UST 正式推出</h4>
    <p>Terraform Labs 发布 UST（TerraUSD），为 LUNA 生态内的算法稳定币，主打“无须法币担保的稳定币”。</p>
  </div>

  <div class="ust-event">
    <div class="date">2021年</div>
    <h4>Anchor Protocol 上线</h4>
    <p>推出 DeFi 借贷平台 Anchor，用户存入 UST 可获得<strong>近20%的高年化收益</strong>，吸引大量资金流入。</p>
  </div>

  <div class="ust-event">
    <div class="date">2021年末</div>
    <h4>UST 市值飞涨</h4>
    <p>UST 市值超过 <strong>$10B</strong>，成为 DeFi 领域最大算法稳定币。LUNA 价格也随之上涨。</p>
  </div>

  <div class="ust-event danger">
    <div class="date">2022年5月7日</div>
    <h4>大额资金开始套利</h4>
    <p>市场察觉 LUNA-UST 模型脆弱，一笔 <strong>近两亿美元</strong> 的 UST 被提现并抛售，引发锚定脱钩。</p>
  </div>

  <div class="ust-event danger">
    <div class="date">2022年5月9日</div>
    <h4>锚定彻底失控</h4>
    <p>UST 价格跌破 $0.8，市场恐慌加剧，LUNA 被不断增发试图稳定价格，导致<strong>LUNA 无限稀释</strong>。</p>
  </div>

  <div class="ust-event danger">
    <div class="date">2022年5月11日</div>
    <h4>死亡螺旋</h4>
    <p>UST 跌至 <strong>$0.3 以下</strong>，LUNA 崩盘近乎归零。投资者资产几乎清零，损失超过 $40B。</p>
  </div>

  <div class="ust-event">
    <div class="date">2022年5月16日</div>
    <h4>社区投票分叉</h4>
    <p>Terraform 社区决定<strong>以快照分叉</strong>，诞生新链 Terra 2.0（无稳定币），原链改名为 Terra Classic。</p>
  </div>

  <div class="ust-event">
    <div class="date">2023年后</div>
    <h4>Do Kwon 被通缉</h4>
    <p>韩国政府和国际刑警通缉 Terraform 创始人 <strong>Do Kwon</strong>，其后在塞尔维亚被捕。</p>
  </div>

</div>

<div class="card-footer">
  <strong>教训：</strong> 算法稳定币<strong>缺乏真实抵押</strong>，依赖市场信心。UST 的崩溃标志着去中心化稳定币必须重构信任机制。
</div>

<style>
.timeline-ust {
  border-left: 3px solid #ccc;
  margin-left: 1rem;
  padding-left: 1rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.ust-event {
  position: relative;
  padding-left: 1.5rem;
}
.ust-event::before {
  content: '';
  position: absolute;
  left: -0.65rem;
  top: 0.3rem;
  width: 10px;
  height: 10px;
  background-color: #2d8cf0;
  border-radius: 50%;
}
.ust-event.danger::before {
  background-color: #f56c6c;
}
.ust-event .date {
  font-size: 0.9rem;
  color: #888;
  margin-bottom: 0.3rem;
}
.ust-event h4 {
  margin: 0.2rem 0;
  font-size: 1.05rem;
}
.ust-event p {
  margin: 0;
  font-size: 0.95rem;
}
.card-footer {
  margin-top: 1.5rem;
  background: #fff9e6;
  padding: 1rem;
  border-left: 5px solid #faad14;
  border-radius: 6px;
}
</style>
