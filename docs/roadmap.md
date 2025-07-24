## Web2 程序员转 Web3 路线图
路线图面向拥有 Web 开发基础（如 JS/Node.js/Vue/React）的开发者，帮助你系统性迈入 Web3 世界，从入门到构建完整 DApp（去中心化应用）。

### 阶段一：理解 Web3 的基础理念

**目标**  
掌握 Web3 世界观、核心概念和常用术语

**内容**  
- 什么是 Web3？
- 区块链基础知识（区块、交易、哈希、节点、Gas）
- 公链与私链（Ethereum、Solana、Polygon 等）
- 钱包、地址、私钥、公钥、助记词
- Token 类型（ERC-20、ERC-721、ERC-1155）
- 智能合约、DApp、DAO、DeFi、NFT、RWA 是什么？

**📚 推荐资源**  
- [Ethereum.org 入门教程](https://ethereum.org/)
- [CryptoZombies（Solidity 游戏式学习）](https://cryptozombies.io/)

---

### 阶段二：开发工具 & 钱包实战

**目标**  
熟悉 Web3 钱包、区块链浏览器与测试网环境

**内容**  
- 安装并使用 MetaMask
- 学会使用测试网（Goerli、Sepolia、Polygon Mumbai 等）
- 使用 Etherscan 查交易
- 认识钱包签名机制（EIP-712）
- 与合约交互的前端体验（如连接钱包按钮、授权、签名）

**📚 推荐工具**  
- WalletConnect
- Ethers.js / web3.js（前端调用合约）
- Remix IDE（在线合约测试工具）

---

### 阶段三：学习 Solidity 智能合约开发

**目标**  
能编写简单的智能合约并理解部署流程

**内容**  
- Solidity 语法入门（变量、函数、修饰符、继承）
- 编写简单的代币合约（ERC-20）
- 编写简单的 NFT 合约（ERC-721）
- 使用 Hardhat/Foundry 进行本地开发与部署
- 了解安全性概念（重入攻击、权限控制）

**📚 推荐工具**  
- Hardhat（部署/测试框架）
- OpenZeppelin（合约库）
- Foundry（高级开发工具）

---

### 阶段四：前端 + 合约集成（构建 DApp）

**目标**  
能开发一个完整的 Web3 应用

**内容**  
- 使用 React / Vue 构建前端页面
- 使用 Ethers.js 连接钱包（MetaMask、WalletConnect）
- 获取链上数据：账户地址、余额、合约状态
- 发起交易：mint NFT、发送 Token、调用函数
- 离线签名（EIP-712）、多链适配（链切换）
- 构建 DApp 实战项目（如 NFT mint 页面、DAO 投票界面）

**📚 推荐工具**  
- wagmi（React Web3 Hooks）
- Vue + Ethers（轻量集成）
- RainbowKit / ConnectKit（连接 UI）
- The Graph（链上数据索引）

---

### 阶段五：探索进阶领域（可选方向）

| 方向           | 说明                                      |
| -------------- | ----------------------------------------- |
| DeFi 开发      | 构建交易所、流动性池、借贷协议             |
| DAO 治理       | 创建治理 Token、投票机制                   |
| NFT Marketplace| 铸造、挂单、交易、版税                    |
| RWA 上链       | 构建现实资产的映射合约和平台               |
| ZK / 隐私链    | 零知识证明、隐私交易、链下计算             |
| 跨链通信       | 使用 LayerZero、Wormhole 等工具跨链传输数据和资产 |

---

###  项目实战建议

| 项目名称           | 技术点覆盖                                 |
| ------------------ | ------------------------------------------ |
|  NFT Mint 网站   | 合约部署、mint 调用、链上状态展示         |
|  DAO 投票前端    | 签名发起、投票读取、治理 Token            |
|  Token Airdrop   | Merkle Tree 验证、白名单合约、EIP-712 签名授权 |
|  Mini Uniswap    | LP、swap 逻辑、流动性池部署               |
|  NFT 抵押借贷    | NFT 抵押合约 + 利息模型 + 清算机制         |

---

###  学会后你可以：

- 独立开发 Web3 应用或工具
- 加入 Web3 团队做前端 / 合约 / 全栈开发
- 部署自己的项目，获得用户与社区支持
- 在 Hackathon / Grant 项目中申请资助
- 构建你的 Web3 简历（GitHub + 链上作品）

