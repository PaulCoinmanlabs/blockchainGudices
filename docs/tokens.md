# Token 类型详解（ERC-20、ERC-721、ERC-1155）

## 📖 什么是 Token？
Token（代币）是部署在区块链上的资产单位，可以代表价值、身份、门票、游戏物品等。

Token 并不是区块链原生币（如 ETH、SOL），而是智能合约生成的数字资产。

> **🧱 Token = 合约 = 可转移的数字资产**  
> 常部署在支持智能合约的链上（如以太坊、Polygon、BNB Chain）



## 🔠 什么是 ERC 标准？
ERC（Ethereum Request for Comments）是以太坊社区提出的合约“接口规范”。

每一种 Token 类型本质上就是一组预定义的函数接口，保证它可以：

- 被钱包识别 ✅
- 被交易所处理 ✅
- 被合约交互 ✅

**常见接口示例：**

- `totalSupply()` → 总供应量
- `transfer(address to, uint256 amount)` → 转账
- `balanceOf(address)` → 查询余额



## 📦 ERC-20：可替代代币（Fungible Token）

ERC-20 是最常见的 Token 类型，用于代币、治理币、稳定币等。

**特点：**

- 每个 Token 单位是等价的（1 USDC = 1 USDC）
- 可分割（通常支持小数点后 18 位）
- 可用于支付、投票、质押、流动性等用途

**常见函数：**
```solidity
function balanceOf(address account) external view returns (uint256);
function transfer(address recipient, uint256 amount) external returns (bool);
function approve(address spender, uint256 amount) external returns (bool);
function allowance(address owner, address spender) external view returns (uint256);
```

**示例项目：**

| 项目名      | Token 名称 | 用途说明           |
|-------------|------------|--------------------|
| USDC / USDT | 稳定币     | 1:1 锚定美元       |
| UNI         | 治理币     | 用于 Uniswap 投票  |
| AAVE        | 借贷代币   | 用于 AAVE 平台     |
| LINK        | Oracle     | Chainlink 网络激励 |



## 🖼️ ERC-721：不可替代代币（NFT）

ERC-721 定义了“独一无二”的资产类型，每个 Token ID 唯一。

**特点：**

- 每个 Token 都有自己的 ID、属性、图片、元数据
- 不能相互替代或分割（如两张图不能直接互换）
- 常用于头像类 NFT、门票、认证证书、游戏角色等

**常见函数：**
```solidity
function ownerOf(uint256 tokenId) external view returns (address);
function tokenURI(uint256 tokenId) external view returns (string memory);
function safeTransferFrom(address from, address to, uint256 tokenId) external;
```

**示例项目：**

| 项目名        | 用途                 |
|---------------|----------------------|
| CryptoPunks   | 头像收藏             |
| Bored Ape     | 社交身份 + 会员通行证 |
| Lens Profile  | Web3 身份账号 NFT    |
| Mirror Post   | 内容创作版权 NFT     |



## ⚔️ ERC-1155：混合代币标准（Multi Token）

ERC-1155 是一种同时支持“可替代 + 不可替代”的复合 Token 标准。

**特点：**

- 同一个合约可以管理多个 Token 类型
- 支持“批量转账”，节省 gas
- 常用于游戏道具、装备、票务等场景

**常见函数：**
```solidity
function balanceOf(address account, uint256 id) external view returns (uint256);
function safeBatchTransferFrom(...);  // 一次转多个 ID
```

**示例项目：**

| 项目名                        | 用途                    |
|-------------------------------|-------------------------|
| OpenSea                       | ERC-721 + ERC-1155混用  |
| GameFi 项目如 Illuvium、EmberSword | 游戏物品、装备、NFT      |
| Event Tickets                 | 一场活动中多类门票发行   |



## 📊 ERC-20 vs ERC-721 vs ERC-1155 总对比表

| 特性         | ERC-20            | ERC-721             | ERC-1155               |
|--------------|-------------------|---------------------|------------------------|
| 替代性       | 可替代（同质化）   | 不可替代（独一无二） | 可混合（多种类型）     |
| 是否可分割   | ✅ 是              | ❌ 否                | ✅/❌ 取决于设计         |
| 典型用途     | 治理、支付、激励   | 收藏品、会员、身份    | 游戏物品、票务、混合资产 |
| Gas 成本     | 中                 | 高                  | 较低（支持批量操作）    |
| 钱包支持度   | ✅ 普遍支持         | ✅ 普遍支持           | ⚠️ 不是所有钱包支持      |



## ✅ 小结

- **ERC-20**： 钱的标准（FT），适合通证、支付、投票
- **ERC-721**： 身份 & 收藏品的标准（NFT），每个都独特
- **ERC-1155**： 混合场景标准，适合游戏 / 票务 / 资源型资产

所有标准都建立在“合约即资产”基础上，钱包与 DApp 通过标准接口交互，从而形成生态兼容性。
