# 论文笔记
## 论文信息

* 标题：A Formal Treatment of Deterministic Wallets

* 作者：Poulami Das, Sebsatian Faust, Julian Loss

* 出处：ACM CCS 2019

* 链接：https://dl.acm.org/doi/abs/10.1145/3319535.3354236 

* 笔记作者昵称：hlr

## 论文简要

该文章主要介绍了一种新的可证明安全的可用于加密货币的热/冷钱包方案，通过该方案可以保障加密货币中交易的安全性，有效抵御攻击者的攻击。

## 主要内容

该篇论文主要介绍了一种安全模型来增强冷/热钱包机制的安全性，并且提出了一种基于此的新的钱包方案，并且对这一方案的安全性进行了数学的证明。

### Security model for wallets

作为论文中提出的第一个概念，这是论文中所提出的一种为钱包所设计的**安全模型**，作者考虑了可能出现的安全问题合并到模型当中，保证了即使在热钱包受到攻击的情况下，冷钱包中的资金仍然可以安全。

### Stateful deterministic wallets

作者为了实现钱包的安全模型，提出了一种模块化的方法，这是一种带有可重定向密钥的安全签名方案，并且在论文中详细展示了实例化钱包的方法。

### Provably secure ECDSA-based wallets

这是作者提出的钱包方案，是一个具体的模型。在这里作者给出了一个具体的急于ECDMA的钱包的解决方案，通过在比特币现有实现的一些基础上构建一个可以兼容现有钱包模型的钱包，达到更为安全的目的。

## 创新点

文章中提出了一种新的安全模型，以及对应的钱包方案，可以从一定程度上解决加密货币交易过程中受到攻击从而遭受经济损失的问题。而且该安全模型得到了充分的证明，可以证明可以提高现有钱包的安全性

## 目前缺点

作者目前研究的点是基于比特币之上的，其安全模型可以兼容的类型也是需要和比特币的机制相同的加密货币，如果在未来出现了更多类型的加密货币，又会出现新的安全问题，而该问题的泛用性目前不得而知，所以其适用范围有待考虑。  
考虑到未来可能各个国家都会发行对应的数字货币，其不同货币之间的安全交易也会是一个重要的议题。  


