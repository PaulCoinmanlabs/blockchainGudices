<style>
.token-container {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
  margin-top: 20px;
}

.token-card {
  width: 300px;
  padding: 20px;
  background: linear-gradient(135deg, #121c2b, #1f3d64);
  color: #fff;
  border-radius: 15px;
  box-shadow: 0 8px 20px rgba(0,0,0,0.3);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.token-card:hover {
  transform: scale(1.05);
  box-shadow: 0 12px 25px rgba(0, 255, 255, 0.4);
}

.token-title {
  font-size: 1.3em;
  font-weight: bold;
  margin-bottom: 12px;
  color: #ffdd57;
}

.token-tag {
  display: inline-block;
  background: #ffdd57;
  color: #000;
  padding: 2px 8px;
  border-radius: 8px;
  font-size: 0.8em;
  margin-bottom: 8px;
}

.token-body {
  font-size: 0.95em;
  line-height: 1.5em;
}
</style>
<div class="token-container">

  <div class="token-card">
    <div class="token-title">Native Token</div>
    <div class="token-tag">原生资产</div>
    <div class="token-body">
      由区块链系统原生发行。用于支付交易手续费（Gas）、质押、激励。<br><br>
      <strong>举例：</strong> ETH、BTC、BNB、SOL。
    </div>
  </div>

  <div class="token-card">
    <div class="token-title">非 Native Token</div>
    <div class="token-tag">合约资产</div>
    <div class="token-body">
      由智能合约创建的资产，用于治理、激励、生态运营等，不可直接支付 Gas。<br><br>
      <strong>举例：</strong> USDT、UNI、AAVE、MKR。
    </div>
  </div>
</div>
<br/>

# 什么是 Native Token？什么是非 Native Token
## Native Token 是链的“官方货币”
| 区块链网络         | Native Token 名称 |
| ------------- | --------------- |
| Ethereum（以太坊） | ETH             |
| Bitcoin（比特币）  | BTC             |
| BNB Chain     | BNB             |
| Solana        | SOL             |
| Avalanche     | AVAX            |
| Polygon       | MATIC           |

这些币的特点：
- 是区块链底层定义的资产
- 通常用来支付手续费（Gas）
- 通常用于 PoS/PoW 激励机制
- 不是通过智能合约创建的

## 非Native Token 是“链上的项目币”
| 特征                 | 说明                              |
| ------------------ | ------------------------------- |
| 运行在主链之上            | 例如 ERC-20 Token 是运行在以太坊上的智能合约代币 |
| 依赖主链基础设施           | 它们自己不能支付 Gas，调用时仍需用 ETH（或其他原生币） |
| 用于特定 DApp 的激励或治理用途 | 例如 UNI、AAVE、SAND 等              |

| 项目   | 所属链        | 类型    | 用途             |
| ---- | ---------- | ----- | -------------- |
| UNI  | Ethereum   | 非原生代币 | Uniswap 的治理代币  |
| AAVE | Ethereum   | 非原生代币 | 借贷协议中的投票权与质押代币 |
| USDT | Ethereum 等 | 非原生代币 | 稳定币，用于支付、交易等   |


| 类比场景  | Native Token      | 非 Native Token          |
| ----- | ----------------- | ----------------------- |
| 操作系统  | 操作系统自带的货币（如金币）    | 游戏内发行的点券、代币             |
| 城市/国家 | 官方货币（如新台币）        | 商场积分、信用卡返现、超市券等         |
| 区块链系统 | ETH / BNB / BTC 等 | ERC-20、BEP-20 合约创建的项目代币 |

> 非Native Token可能有无限多种，但一条链通常只有一个Native Token。

### 这个区别很重要？
#### 1.Gas 只能用 Native Token 支付
- 想在以太坊调用合约？你得有 ETH。
- 即使你有 100 万个 USDT，没有 ETH 也动不了（后续升级是可以的，本次就当前而言）。

#### 2.Native Token决定链的经济安全
- ETH 被质押用来维持网络运行；
- 项目币不参与安全机制，价值更容易波动。

#### 3.投资风险差异巨大
- Native Token：更基础设施级，更长久；
- 非 Native Token：可能暴涨暴跌，容易跑路（如土狗币）。

## 小结
| 特征       | Native Token  | 非 Native Token |
| -------- | ------------- | -------------- |
| 是否原生     |  是           |  否，合约创建       |
| 用于支付 Gas |  是           |  否            |
| 数量限制     | 一个            | 多个项目可自定义       |
| 作用       | 网络安全、Gas、价值储存 | 治理、奖励、流动性等     |
