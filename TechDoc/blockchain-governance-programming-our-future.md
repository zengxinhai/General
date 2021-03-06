# Blockchain Governance: Programming Our Future |区块链治理：设计我们的未来

> 本文翻译自：https://medium.com/@FEhrsam/blockchain-governance-programming-our-future-c3bfe30f2d74

> 译者：[区块链中文字幕组](https://github.com/BlockchainTranslator/EOS) [鱼](https://github.com/oscnet)

> 翻译时间：2017-11-29

This post describes why blockchain governance design is one of the most important problems out there, its critical components, current approaches, potential future approaches, and concludes with suggestions for the community.

这篇文章描述了为什么区块链治理设计是区块链设计中最重要的问题之一，包括治理设计的关键组成部分，当前所使用的治理方案，以及未来潜在的方案，并以对社区的建议作为文章的结束。

## Why Blockchain Governance Matters | 为什么区块链治理至关重要

**As with organisms, the most successful blockchains will be those that can best adapt to their environments. Assuming these systems need to evolve to survive, [initial design](https://en.wikipedia.org/wiki/Butterfly_effect) is important, but over a long enough timeline, the mechanisms for change are [most](https://en.wikipedia.org/wiki/Natural_selection) [important](https://briankeng.com/2015/07/a-little-bit-of-slope/)**.

As a result, I believe **governance is the most vital problem in the space**. Other fundamental problems like scalability are arguably best approached by using governance to set the right incentives for people to solve them. Yet little research has gone into governance and it feels poorly understood.

**如同生物一样，成功的区块链也是那些能够很好地适应环境的区块链。假设这些系统需要进化以求得生存，显然[初始设计](https://en.wikipedia.org/wiki/Butterfly_effect)是重要的，但是如果需要长时间生存下来，那么有一个做出改变并进化的机制则显然[更为](https://en.wikipedia.org/wiki/Natural_selection)[重要](https://briankeng.com/2015/07/a-little-bit-of-slope/)**。

因此，我认为**治理是这个领域最重要的问题**。其他一些基本问题，如可扩展性问题，可能最好通过治理，采用设置适当的激励措施来解决。但是，对于有关治理地研究却极少，甚至对治理不甚了解。

![](https://cdn-images-1.medium.com/max/1000/1*N7VAEAH8-_Sqxmy8_0bgNQ.png)
Evolutionary tree of life, from [Leonard Eisenberg](https://www.evogeneao.com/explore/tree-of-life-explorer).进化的生命之树，取自[Leonard Eisenberg](https://www.evogeneao.com/explore/tree-of-life-explorer)。

Satoshi showed us the immense power of releasing a blockchain-based incentive structure into the world. A 9 page [whitepaper](https://bitcoin.org/bitcoin.pdf) spawned a $150bn cryptocurrency, a computer network [bigger than the top 500 supercomputers by 10,000x](https://www.reddit.com/r/Bitcoin/comments/5kfuxk/how_powerful_is_the_bitcoin_network/), and a diverse ecosystem of developers, users, and companies. This was arguably one of the highest leverage actions in human history. It showed the power of blockchains as networks that can connect everyone and bootstrap themselves into existence if well constructed.

We are increasingly living in digital networks, spending an average of [11 hours a day on screens](http://www.kpcb.com/internet-trends) in the US with over half of that on internet connected devices, growing 11% each year. However, these networks are highly centralized (Facebook, Google, Apple, Twitter) and [continue to consolidate](http://fortune.com/2017/01/04/google-facebook-ad-industry/). In the current model, all of the profit and power of a network is within one company, and you’re either inside or you’re outside. It’s important the networks we live in serve our best interests. With blockchains emerging as the new global infrastructure, **we have the opportunity to create vastly different power structures and program the future we want for ourselves**.

For these reasons, I believe **blockchain governance system design is one of the highest leverage activities known**.

中本聪向我们展示了其基于区块链的激励结构向世界呈现出来的巨大能力。仅仅9页的[白皮书](https://bitcoin.org/bitcoin.pdf)创造了1500亿美元的加密货币市场，形成了一个[比前500名超级计算机还大10,000倍的计算机网络](https://www.reddit.com/r/Bitcoin/comments/5kfuxk/how_powerful_is_the_bitcoin_network/)，并最终形成开发者，用户和公司的多元生态系统。成为人类历史上影响力最高的行动之一。看来只要区块链被良好设计并构造，它就可以把我们每个人连接起来，自主运行并生存下来，这充分展示了区块链作为网络蕴含的巨大能量。

我们越来越多地生活在数字网络中，在美国，人们每天平均花费11个小时在屏幕上，其中有一半以上是连接了互联网的设备，而且这个时间每年增长11％。不过，这些网络都是高度集中化的（如 Facebook，Google，Apple，Twitter），并且它们的地位继续进一步得到巩固。在目前的模式中，网络的所有利润和权力都在一个公司内部，而你要么在内部要么在它外面。但是，重要的是，我们生活的网络要服务于我们的最佳利益。随着区块链成为新的全球基础设施，**我们有机会创造出截然不同的权力机构，并且设计出我们自己想要的未来**。

出于这些原因，我坚信**区块链治理系统设计是已知影响力最高的活动之一**。

## A Cambrian Explosion | 寒武纪大爆发

It’s rare a new government or central bank gets created, and even more rare to see experimentation with a new form of governance when it does.

Blockchains are unique because they 1) allow thousands of governance systems and monetary policies to be tried at the speed of software with 2) in some cases, much lower consequences of failure. As a result, **there will be a [Cambrian explosion](https://en.wikipedia.org/wiki/Cambrian_explosion) of economic and governance designs** where many approaches will be tried in parallel at hyperspeed. To be clear, I am including economic design and monetary policy (said another way, incentive structure) in governance because, like other aspects of the system, they can be modified as time passes.

我们知道，一个新政府或中央银行成立，这样的情况是很少见的，而在成立时实施新的治理形式则更为罕见。

区块链是独一无二的，因为它 1）允许成千上万的治理系统和货币政策以软件运行的速度进行尝试，2）在某些情况下，治理失败引起的后果常常并不严重。因此，**有关经济和治理设计将会出现类似于[寒武纪的爆炸式增长](https://en.wikipedia.org/wiki/Cambrian_explosion)**，在这种情况下，各种方案将可以并行和极速地进行测试。需要说明的是，我在治理中包括经济设计和货币政策（也就是说，激励结构），因为像系统的其他方面一样，随着时间的推移它们可能被修改。

![](https://cdn-images-1.medium.com/max/800/1*SDRcq6gCVc4TcI5YUnrY3g.jpeg)

Many of these attempts will be spectacular failures. With millions of algorithmic central banks we will have millions of crypto [George Soroses trying to break the Bank of England](https://en.wikipedia.org/wiki/Black_Wednesday). Through this process, **blockchains may teach us more about governance in the next 10 years than we have learned from the “real world” in the last 100 years**.

通过数百万个基于算法的中央银行，我们将可以进行类似数百万个加密的[索罗斯试图打破英格兰银行](https://en.wikipedia.org/wiki/Black_Wednesday)地尝试。虽然这些尝试绝大部分都将壮丽地失败。通过这个过程，**在接下来的10年中，区块链教会我们的有关治理知识将大大多于我们过去100年在“现实世界”中所学到的知识**。

## Two Critical Components of Governance | 治理的两个关键组成部分

1. Incentives

 Each group in the system has their own incentives. Those incentives are not always 100% aligned with all other groups in the system. Groups will propose changes over time which are advantageous for them. Organisms are biased towards their own survival. This commonly manifests in changes to the reward structure, monetary policy, or balances of power.

2. Mechanisms for coordination

 Since it’s unlikely all groups have 100% incentive alignment at all times, the ability for each group to coordinate around their common incentives is critical for them to affect change. If one group can coordinate better than another it creates power imbalances in their favor.

 In practice, a major factor is how much coordination can be done on-chain vs. off-chain, where on-chain coordination makes coordinating easier. In some new blockchains, on-chain coordination allows the rules or even the ledger history itself to be changed.


1. 激励措施

 系统中的每个组织都有自己的激励机制。 这些激励措施并不总是与系统中的所有其他组织保持一致。随着时间的推移，组织将提议对他们有利的改变。有机体通常倾向于有利自己的生存的变化。通常体现在奖励结构，货币政策或权力平衡的变化上。

2. 协调机制

 在任何时候，对所有的组织都有100％的激励，这是不可能的。每个团队围绕共同的激励进行协调的能力是至关重要的，体现了它们对变革的影响力。如果一个组织比另一个组织具有更好的协调能力，那么就会造成对自己有利的权力失衡。

 在实践中，一个主要的因素是可以在链上和链外进行多少协调，链上协调相对来说更为容易。在一些新型的区块链中，链上协调允许规则或者甚至历史账本本身被改变。

## Current Approaches | 目前的方案

What follows is a dissection of the benefits and drawbacks of today’s two largest blockchains: Bitcoin and Ethereum. We are currently in the primordial ooze phase of blockchain governance. Systems are simple and little has been tried.

以下是对当今两大区块链的优点和缺点的剖析：比特币和以太坊。我们目前处于区块链治理的初级阶段。系统很简单，治理的方案只有也很少被尝试过。

### Bitcoin | 比特币

Bitcoin was the first successful attempt to create a standalone blockchain. Let’s examine it as a base:

比特币是第一个创建独立区块链的成功尝试。做为基础，让我们来看一下：

1. Incentives

 * Developers: increase value of existing token holdings, social recognition, maintain power for control over future direction.

 * Miners: increase value of existing token holdings, expected future block rewards, and expected future transactions fees.

 * Users: increase value of existing token holdings, increase functional utility (e.g. store of value, uncensorable transactions, file storage).

2. Mechanisms for coordination

 Mostly off-chain. Developers coordinate through the Bitcoin Improvement Proposals (BIPs) process and a mailing list. Miners can coordinate on-chain in the sense that they are creating the chain itself.


1. 激励措施

  * 开发人员：增加持有的代币价值，增强社会认可度，保持对未来发展方向的控制权。

  * 矿工：增加持有的代币价值，期待未来更高的区块奖励以及未来更多的交易费用。

  * 用户：增加持有的代币价值，增加功能效用（例如，存储价值，不可审查的交易，文件存储）。

2. 协调机制

  主要通过链下协调。开发人员通过比特币改进建议（BIPs）流程和邮件列表进行协调。矿工们可以在链上协调，因为是他们自己创造了区块链。

#### Resulting system | 最终得到的系统

The **checks and balances system created is somewhat analogous to the US government** and has a number of benefits. Similar to the Senate submitting new bills, developers submit pull requests. Similar to the judiciary, miners decide whether or not to actually adopt the laws in practice. Similar to the executive branch, the nodes of the network can veto by not running a version which aligns with what the miners are running. And similar to citizens, the users can revolt. Finally, economic incentives dictate that it is in everyone’s best interest to maintain trust in the system. For example: if miners alienated all the users, the tokens would decrease in value and they would go out of business. **As the first system of its kind, it’s incredible that Bitcoin is still going strong**.

比特币**建立的制衡系统有些类似于美国政府**，并拥有多项好处。与参议院提交新法案类似，开发者提交请求。与司法部门类似，矿工决定是否在实践中实际采纳。类似于行政部门，网络的节点可以通过不运行与矿工正在运行的版本相一致的版本来否决。
和公民类似，用户可以造反。最后，经济激励要求维护对系统的信任符合每个人的最佳利益。例如：如果矿工疏远了所有的用户，这些代币的价值就会下降，他们就会倒闭。**作为第一个这样的系统，比特币仍然强劲，这是不可思议的**。

![](https://cdn-images-1.medium.com/max/800/1*GM32YcRx7C_XgheMWld4RA.png)
Bitcoin as branches of US Government. Image from Buck Perley.

将比特币比作美国政府各部门。图片来自Buck Perley。

There are risks to the system caused by asymmetries in incentives. Miners push for changes which increase future cumulative transaction fees, while developers don’t care as long as the value of Bitcoin keeps going up. Developers’ direct economic incentives are weak. New developers have little incentive to work on Bitcoin because there is no direct way to earn money by doing it. As a result, they often work on new projects — either by creating Ethereum tokens, entirely new chains, or companies. No new blood entering increases the perception and reality of early developers as the most knowledgable and experienced. This [results](https://medium.com/@BuckPerley/crypto-governance-f1318affbbe0) in **a self-reinforcing cycle of more power becoming concentrated in a small group of early core developers, slower technological advancement, and conservatism**. Developers are at risk of being bribed since they have a lot of power but weak economic incentives. Some [early holders](http://chaincode.com/) and [universities](https://bitcoinmagazine.com/articles/gavin-andresen-core-developers-join-mits-digital-currency-initiative-1429743725/) have sponsored developers, but with limited impact thus far.

由于激励措施的不对称系统存在风险。矿工们试图推动变革以增加未来累计交易费用，但只要比特币的价值持续上涨，开发人员并不在乎此。对开发人员的直接经济刺激是微弱的。新的开发人员没有什么动力去为比特币工作，因为没有直接的方法来赚钱。因此，他们经常从事其它新项目的工作 - 如创建以太坊代币，新的区块链开发或进入公司工作。没有新的血液进入以提高早期开发人员的观念和认知，因为他们是最有知识和经验的。这将导致周期性自我强化的[结果](https://medium.com/@BuckPerley/crypto-governance-f1318affbbe0)：**越来越多的权力集中在一小群早期的核心开发者身上，使得系统技术进步缓慢，并趋于保守**。由于开发人员拥有巨大权力，但经济激励力度不足，所以开发人员有面临着被贿赂的风险。一些比特币的[早期持有者](http://chaincode.com/)和[大学](https://bitcoinmagazine.com/articles/gavin-andresen-core-developers-join-mits-digital-currency-initiative-1429743725/)赞助了开发人员，但迄今为止影响有限。

Similarly, asymmetries in ability to coordinate give miners disproportionate power. Communication amongst miners is easier because they are a small and concentrated group. Since mining is a business with economies of scale, we’d expect **a continued trend towards [natural monopoly](https://en.wikipedia.org/wiki/Natural_monopoly) in mining** and even greater coordination advantage. As a reference point, [95% of mining power was able to sit on one small stage](https://pbs.twimg.com/media/CVhkEhtUAAAl0LH.jpg) 2 years ago. Miners can also gain disproportionate power by bribing developers or hiring their own. Finally, the checks and balances system of Bitcoin relies on some level of transparency: for example, users becoming aware of a single miner gaining more than 51% of the hashing power or developers having some level of independence. And a miner who was able to gain >51% of hashing power would be incented to remain anonymous. Rather than sparking a specific catastrophic event, this would cause an unknowing descent into a centralized world of control through censorship and asset freezing.

同样，不平衡的协调能力给了矿工不相称的权力。矿工之间更容易沟通，因为他们是一个小而集中的群体。
由于采矿业是一个规模经济的行业，**我们预计采矿业将继续趋向[自然垄断(指因产业发展的自然需要而形成的垄断状态)](https://en.wikipedia.org/wiki/Natural_monopoly)**，将具有更大的协调优势。
作为参考点，2年前，具有[95％的采矿权的矿工代表们能够出现在一个小的舞台上](https://pbs.twimg.com/media/CVhkEhtUAAAl0LH.jpg)。矿工也可以通过贿赂开发人员或雇用更多的矿工的来获得更大的权力。最后，比特币的制衡机制依赖于某种程度的透明度：例如，人们意识到一个单一的获得超过51％算力的矿工和开发者人员一样具有某种程度的独立性。而一个能够获得大于51％算力的矿工可以保持匿名。这虽然不会引发特定的灾难性事件，但是通过审查和资产冻结却可以不知情的将它导向一个中心化控制的世界。

### Ethereum | 以太坊

The systemic incentives and mechanisms of coordination in Ethereum are similar to Bitcoin at the moment.

Dynamics will change as Ethereum [moves to proof of stake](https://blog.ethereum.org/2015/08/01/introducing-casper-friendly-ghost/). The power of miners will be replaced by anyone who holds a sufficient amount of Ether to run a virtual miner (a “validator”). This is especially true as solutions like [1protocol](https://1protocol.com/) will allow even the smallest Ether holder to participate, **flattening the distinction between a miner and a user, and potentially reducing the biggest centralization risk in Bitcoin**.

以太坊的系统性激励机制和协调机制目前与比特币相似。

以太坊正将共识机制[转移到权益证明](https://blog.ethereum.org/2015/08/01/introducing-casper-friendly-ghost/)，这将会引发激励机制的改变。任何拥有足够数量以太的持有人，可以通过运行虚拟矿工（“验证人”）来取获得矿工的权力。尤其是像[1 协议](https://1protocol.com/)这样的解决方案，让即使是很少的以太持有者也可以参与，**从而使矿工和用户的区别变小，并有可能降低在比特币中存在的最大的集中化风险**。


The incentives of core developers remain the same. Coordination around challenging issues has been swifter and smoother than in Bitcoin to date. This is due to 1) a culture more open to change because [Ethereum was created as a reaction to what could not be done in a rigid Bitcoin environment](https://coinjournal.net/vitalik-buterin-early-versions-ethereum-supposed-launch-bitcoin/) and 2) direction from Vitalik who is widely trusted in the community.

Current weaknesses in the model include 1) over reliance on its creator (Vitalik) and 2) like Bitcoin, limited ways to incentivize core development, forcing more projects to create tokens to support themselves. Vitalik is [making a conscious effort to step back](https://twitter.com/VitalikButerin/status/928172344631115776), which will be a delicate process.

核心开发者的激励机制保持不变。但是对具有挑战性的问题进行的协调，将比比特币更快，更顺畅。这是由于1）一种更加开放的变革文化，因为[以太坊是针对僵化的比特币环境中无法做到的事情而创建的](https://coinjournal.net/vitalik-buterin-early-versions-ethereum-supposed-launch-bitcoin/)，2）它由来自广受社区信赖的 Vitalik 指导。

该模式目前的弱点包括：1）过度依赖其创建者（Vitalik），2）像比特币，对核心开发者的激励方式有限，迫使更多的项目通过创建代币来支持自己。Vitalik [正在有意识地退后一步](https://coinjournal.net/vitalik-buterin-early-versions-ethereum-supposed-launch-bitcoin/)，这将是一个微妙的过程。

## New Chains Experimenting with On-Chain Governance | 新区块链在链上治理方面的实验

New blockchains are making it much easier to coordinate by enabling on-chain governance.

为了使得协调更为容易，新的区块链项目正在启用链上治理方案。

* Tezos

 In [Tezos](https://www.tezos.com/), [anyone can submit a change to the governance structure](https://www.quora.com/How-is-Tezos-different-from-Ethereum?share=d5c26090&srid=OAAh) in the form of a code update. An on-chain vote occurs, and if passed, the update makes its way on to a test network. After a period of time on the test network, a confirmation vote occurs, at which point the change goes live on the main network. They call this concept a “self-amending ledger”.

 Such a system is interesting because **it shifts power towards users and away from the more centralized group of developers and miners**. On the developer side, anyone can submit a change, and most importantly, everyone has an economic incentive to do it. Contributions are rewarded by the community with newly minted tokens through [inflation funding](https://medium.com/@FEhrsam/funding-the-evolution-of-blockchains-87d160988481). This shifts from the current Bitcoin and Ethereum dynamics where a new developer has little incentive to evolve the protocol, thus power tends to concentrate amongst the existing developers, to one where everyone has equal earning power.

 This also enables users to directly coordinate on-chain, dramatically increasing their power and reducing the power of miners compared to a system like Bitcoin or Ethereum.

 在[Tezos](https://www.tezos.com/)中，[任何人都可以以代码更新的形式提交对治理结构的更改](https://www.quora.com/How-is-Tezos-different-from-Ethereum?share=d5c26090&srid=OAAh)。开启链上投票，如果通过，则更新进入测试网络。在测试网络上经过一段时间之后，再次通过投票确认，更改就可以在主网络上进行。他们把这个概念为“自我修正账簿”。

 这样的系统是有趣的，**因为它将权力转移给用户，而不是给更显集中化的开发者和矿工**。在开发者方面，任何人都可以提交更改，最重要的是，每个人都有经济动机去这样做。社区通过新铸造的代币 - 使用[通货膨胀资金](https://medium.com/@FEhrsam/funding-the-evolution-of-blockchains-87d160988481)来奖励贡献。不同于目前的比特币和以太坊，新的开发者没有什么动力来进化协议，因此权力往往集中在现有的开发者中。这样的系统使得每个人都具有相同的收益能力。

 与比特币或以太坊系统相比，这也使用户能够直接在链上协调，大大增加他们的权力，从而减少了矿工的权力。

![](https://cdn-images-1.medium.com/max/800/1*sKjsh_IrxHvST_aZbaGk_g.png)

* DFINITY

 One step further would be a system which allows on-chain votes to the rules of the system like Tezos and [direct, retroactive changes to the ledger itself](https://medium.com/dfinity/the-dfinity-blockchain-nervous-system-a5dd1783288e). In other words, if something happens that tokenholders do not like (ex: a hack, a marketplace selling drugs), they can **roll back or edit the ledger in addition to the rules of governance themselves**. [DFINITY](https://dfinity.org/), an in-development blockchain, is taking this approach. Proponents of this system point to events like hard fork caused by The DAO hack and the recent [$150m Parity multi-sig bug](https://paritytech.io/blog/security-alert.html) and suggest such events would be much smoother if everyone could just vote to undo them. On the flip side, this system allows direct censorship and peoples’ tokens to be forcibly taken. As we saw with Ethereum’s hard fork to revert The DAO hack, this is possible with existing blockchains, but requires higher friction through off-chain coordination and hard forking instead of on-chain coordination with no forking.

 更进一步，系统允许像 Tezos 一样对系统规则进行链上投票，并[对账本本身进行直接的，追溯性的改变](https://medium.com/dfinity/the-dfinity-blockchain-nervous-system-a5dd1783288e))。换句话说，如果发生代币持有者不喜欢发生的事情（例如：黑客，卖药的市场），**除了本身的治理规则之外，他们还可以回滚或编辑帐本**。
 正在开发的区块链 [DFINITY](https://dfinity.org/) 正在采用这种方案。系统的支持者认为，对于处理类似 the DAO 黑客攻击引起的硬分叉和最近 [冻结150亿美元的 Parity 多重签名错误问题](https://paritytech.io/blog/security-alert.html)，如果毎个人都可以通来投票来撤消，会让事情的解决变得更为顺畅。另一方面，这个系统允许直接审查且代币可以被强制取回。正如我们在以太坊上通过硬分叉来恢复the DAO 攻击一样，这在现有的区块链中是可能的，但是需要通过高难度的链外协调和硬叉来实现。采用这种方案的系统就可以通过链上协调，而且不用分叉。

 DFINITY is maximally flexible. Depending on what parts of the protocol Tezos allows to be changed, it is possible protocol changes effectively let you re-write the ledger as in DFINITY. As a result, it’s likely these systems will have different voting thresholds for different changes, perhaps requiring a supermajority for some things and a simple majority for others.

 DFINITY 是最灵活的。协议的部分内容如果是 Tezos 允许更改的，就能通过对协议进行有效地更改，来重写 DFINITY 中的帐簿。当然，对于不同的改变要求，这些系统可能会使用不同的投票门槛，对某些事情可能需要绝对多数人同意，而其它则仅需要简单的多数通过即可。

### The Double-Edged Sword of On-Chain Governance | 链上治理的双刃剑

[Vlad Zamfir](https://medium.com/@Vlad_Zamfir), one of the chief architects of Ethereum’s proof of stake system, describes on-chain governance as a double edged sword. On the upside it helps make sure a process is consistently followed which can increase coordination and fairness. It also allows for quicker decision making. On the downside it’s risky because the metasystem becomes harder to change once instituted. Like anything put directly into code, **it can be exploited or [gamed](https://en.wikipedia.org/wiki/Nomic) more quickly and easily if flawed**.

以太坊权益证明首席构筑师之一[Vlad Zamfir](https://medium.com/@Vlad_Zamfir)将链上治理称为一把双刃剑。好的一面是，它有助于确保一个过程得到贯彻执行，从而提高协调性和公平性。它也允许更快的决策。不利的一面是风险，因为元系统一旦制定就变得难以改变。就像任何直接写入代码的东西一样，如果有缺陷的话，**它就有可能更快、更容易地被用户所[玩弄](https://en.wikipedia.org/wiki/Nomic)或利用**。

For some use cases, tending towards being static may be good. This may be especially true for store of value. **Perhaps lower level protocols should lean toward stasis and conservatism — “measure twice and cut once” — while higher level protocols should be more flexible — “move fast and break things”**. In the words of Calvin Coolidge: [“it is much more important to kill bad bills than to pass good ones”](https://coolidgefoundation.org/blog/kill-bad-bills/). Like established companies, some of the more established protocols may be able to watch what new protocols do and adopt techniques which seem to be working. This seems especially true of Ethereum which has shown a willingness to hard fork and the ability to maintain network value through them. Consequently, I’d expect to see the most innovation in the next few years from Ethereum tokens and entirely new chains.

在某些使用情况下，系统倾向于静态固定可能更好。这对于存储价值可能尤其如此。**底层协议应倾向于静态和保守 - “三思而后行” - 在更高层次的协议则应该更灵活 - “快速行动，打破陈规”**。用卡尔文·柯立芝（Calvin Coolidge）的话来说：[“废除一个有问题的法案比通过一条好的律法要重要得多”](https://coolidgefoundation.org/blog/kill-bad-bills/)。像已建立的公司一样，一些更为成熟的协议能够借鉴新协议的做法，并可以适配采用正在起作用的技术。对于以太坊来说，似乎更是如此，它表现出了硬分叉的意愿和通过它们来维护网络价值的能力。因此，我期望在接下来的几年里能够看到以太坊代币和新型区块链的重大创新。

It’s probable we haven’t found the best governance systems yet, which means a more general system which allows many different methods to be tried is valuable, if for nothing more than [learning](https://en.wikipedia.org/wiki/Nomic). [A more complex system can simulate less complex ones, but the reverse is generally hard](https://en.m.wikipedia.org/wiki/Automata_theory).

The most interesting learnings will come from exploring the balance of mutability so systems can evolve and immutability for stability.

很有可能我们还没有找到最好的治理体系，这意味着让许多不同的方案在一个更一般的系统上测试是非常有价值的，即使仅为了[学习](https://en.wikipedia.org/wiki/Nomic)。[更复杂的系统可以模拟较不复杂的系统，但反过来通常很难](https://en.m.wikipedia.org/wiki/Automata_theory)。

最有趣的学习将来自于探索思考如何平衡可变性，让系统可以演化发展但是又能保持足够的稳定性。

## Future Approaches | 未来的方案

Next we’ll talk about future governance strategies with potential which have yet to be tried.

接下来，我们将讨论未来的治理策略，这些策略还有待测试。

* Futarchy

 In [futarchy](https://en.wikipedia.org/wiki/Futarchy), **society defines its values and then prediction markets are used to decide what actions will maximize those values**. Said another way: [“vote on values, bet on beliefs”](http://mason.gmu.edu/~rhanson/futarchy.html). It was [originally proposed](http://mason.gmu.edu/~rhanson/futarchy2000.pdf) in 2000 by [Robin Hanson](http://www.overcomingbias.com/bio), an economics professor at George Mason University.

 在 [futarchy](https://en.wikipedia.org/wiki/Futarchy) 中，**社会定义了它的价值，然后通过预测市场来决定采用什么样的行动来最大化价值**。或者说：[“投资价值，对赌理念”](http://mason.gmu.edu/~rhanson/futarchy.html)。这句话是乔治梅森大学（George Mason University）的经济学教授[罗宾汉森（Robin Hanson）](http://www.overcomingbias.com/bio)[最初是在2000年提出](http://mason.gmu.edu/~rhanson/futarchy2000.pdf)的。

 [Ralph Merkle](https://en.wikipedia.org/wiki/Ralph_Merkle) has a particularly eye-opening proposal for a blockchain implementation of futarchy in his paper called [DAOs, Democracy, and Governance](http://merkle.com/papers/DAOdemocracyDraft.pdf). In his proposal, every citizen is polled once a year and asked the question “how satisfied were you this year on a scale of 0 to 1?”. Averaged together, these give an overall societal welfare score. A prediction market on this welfare score is developed for every year for the next 100 years, where traders can speculate on the welfare score for any year into the future. An overall future welfare score is then created by averaging the scores for the next 100 years, weighting earlier years more than future years. When a new bill is introduced, there is a 1 week period where markets speculate on whether the overall welfare score will go up or down if the bill is passed. If the bill is passed, the traders who bet on the overall welfare going up now own the overall welfare contracts they bet on. They will make money if they are right and lose money if they are wrong.

 [拉尔夫·默克尔（Ralph Merkle）](https://en.wikipedia.org/wiki/Ralph_Merkle)在他的论文 《[去中心化的自治组织，民主和治理](http://merkle.com/papers/DAOdemocracyDraft.pdf)》中
 对 futarchy 区块链的实现提出了一个特别另人大开眼界的建议。在他的提议中，每个公民每年都要接受一次对当年满意程度的调查，并让他们在0到1之间打分。然后把这些分数平均，就得出了一个比较全面的社会福利分数。在未来的100年中每一年都会有一个关于这个福利评分的预测市场，交易员可以在这里对未来任何一年的福利评分进行推测。然后通过对未来100年的平均分数来创建未来整体福利分数，当然以前年份的权重比来来年份要高。当一个新的法案出台时，市场有一个星期的时间，可以猜测如果法案通过，整体的福利得分会上升还是下降。如果议案获得通过，那些押注整体福利上升的交易员就拥有了他们所押注的全部合同福利。如果他们是对的，他们会赚钱，如果他们错了就赔钱。

 ![Example of futarchy for deciding whether or not to fire a CEO where the value to maximize is revenue. Image from ConsenSys.](https://cdn-images-1.medium.com/max/600/1*ckQP_t0rBlgVJMIvK_jmtg.png)
 Example of futarchy for deciding whether or not to fire a CEO where the value to maximize is revenue. Image from ConsenSys.futarchy 决定是否解雇一位首席执行官的例子,收益来自于其价值的最大化。来自ConsenSys的图片。

 This system could be incredibly powerful for a few reasons. First, voting becomes extremely simple. People don’t need to vote, they are just asked about one thing once a year: their satisfaction. Second, people do not need to develop extensive knowledge of candidates or bills. This is important because candidates are often persuasive and bills are complex to the point where it is hard for a domain-specific researcher to understand their implications, let alone an elected official or an average citizen. Instead, we rely on the wisdom of the markets. Like trading in stocks, only people who are extremely well informed on a topic will bet on it — otherwise they are likely to lose money to others who are better informed. Finally, it is a system where **market incentives are aligned with societal values**.

 这样的系统可能变得非常强大。因为首先，投票变得非常简单。人们不需要投票，他们每年只会被问到一件事：他们的满意度。其次，人们不需要学习掌握对候选人或者议案方面的广泛的知识。这一点很重要，因为候选人往往具有说服力，而且议案很复杂，以至于即使某个特定领域的研究人员也很难理解他们的含义，更不用说当选官员或普通公民。相反，我们依靠市场的智慧。就像股票交易一样，只有那些对某个主题非常了解的人才会下注，否则他们很可能会赔钱给那些更了解情况的人。最后，这是一个**市场激励与社会价值观一致的体系**。

 In futarchy the devil is in the implementation details. [Hard problems include](http://www.overcomingbias.com/2016/07/merkles-futarchy.html) the governance metaproblem of how to decide on the societal value(s) to maximize in the first place and making sure people aren’t incented to [tactically vote](https://en.wikipedia.org/wiki/Gibbard–Satterthwaite_theorem) an extreme satisfaction score of 0 or 1 to swing policy.

 在 futarchy 中实施细节是魔鬼。[困难的问题包括](http://www.overcomingbias.com/2016/07/merkles-futarchy.html)，如何决定最大化的社会价值的治理元问题，以及确保人们不会采用[策略性投票](https://zh.wikipedia.org/wiki/%E7%AD%96%E7%95%A5%E6%80%A7%E6%8A%95%E7%A5%A8)([详见](https://en.wikipedia.org/wiki/Gibbard–Satterthwaite_theorem))策略，投出极端的 0 或 1 分的满意度。

 **Setting goal functions is both important and tricky, as there are always unforeseen consequences**. For example, in the case of capitalism, this can manifest in rising wealth inequality and environmental externalities. In the case of artificial intelligence, this can manifest in [wireheading](https://wiki.lesswrong.com/wiki/Wireheading) or rapidly maximizing something at the unexpected expense of other things, commonly illustrated through the example of a [paperclip maximizer](https://wiki.lesswrong.com/wiki/Paperclip_maximizer) which destroys everything to build as many paperclips as possible. These are serious concerns, as I believe [the most powerful AIs will be bootstrapped into existence on the blockchain](https://twitter.com/FEhrsam/status/912388216396824576) by using tokenized incentives for everyone to feed them the best data and algorithms. If this is true, blockchain governance is the largest determinant of our future trajectory as a species. More on this in a future post.

 **设定目标函数既重要又棘手，因为总会有无法预料的后果**。例如，就资本主义而言，这可以表现在不断上升的财富不均和环境的外部性。在人工智能的情况下，表现为如[脑机接口(通过直接刺激大脑使快感最大化)](https://wiki.lesswrong.com/wiki/Wireheading)，或极快速的在意外的消耗掉某个事物后使另外的事物最大化。通常我们可以通过[回形针制造机](https://wiki.lesswrong.com/wiki/Paperclip_maximizer)的例子来说明，这个回形针制造机破坏消耗所有东西以尽可能多地制造出回形针。（译者注：回形针制造机指的是一种强人工智能，一个设计称职且无恶意，但最终毁灭人类的思想实验。实验表明，具有明显无害价值的人工智能可能构成一种存在的威胁）这些都是严重的问题，因为我相信，通过为所有人使用代币化的激励措施，并且给它们优质的数据和算法，[最强大的人工智会在区块链上自动运行并生存下来](https://twitter.com/FEhrsam/status/912388216396824576)。如果这是真的，区块链治理是我们这个物种未来发展轨迹的最大决定因素。我将在以后发表更多有关于这方面的文章。

* Liquid Democracy | 委任式民主

 [Liquid democracy](https://en.wikipedia.org/wiki/Delegative_democracy) is system where everyone has the ability to vote themselves, to delegate their vote to someone else, and to remove the delegation of their vote at any time. In the U.S. we do not have a liquid democracy because we cannot vote on many bills directly (our representatives do that for us) and once we elect a representative, they are typically in office for 4 years.

 This seems like it will be used in proof of stake blockchains given its simplicity.

 [委任式民主](https://en.wikipedia.org/wiki/Delegative_democracy)是一种人人有能力投票的制度，可以将选票委托给别人，或随时取消委托。在美国，我们没有委任式民主，因为我们不能对法案进行直接投票（而是由我们的代表帮我们做了这件事），一旦我们选出代表，他们通常在任期4年。

 因为它的简单性，看起来它似乎将被用于权益证明的区块链系统。

* Quadratic Voting | 二次方投票

 [Quadratic voting](http://ericposner.com/quadratic-voting/) is a system of buying votes, where each additional vote costs twice as much as the one before it. In other words, money buys votes, but with strong diminishing returns. [Vitalik proposed](https://www.reddit.com/r/ethereum/comments/4rtpmm/on_coinlock_voting_futarchy_and_optimal/) a variant on this he calls “quadratic coin lock voting” where N coins let you make N * k votes by locking up those coins for a time period of k². This is a nice modification because it aligns incentives over time: more voting power requires living with your decisions for longer. In a tokenized world with little friction of entering or leaving a community, this is especially important.

 [二次方投票](http://ericposner.com/quadratic-voting/)是一个购买投票的系统，每增加一票，票价就是前一票的两倍。换句话说，用钱买票，但收益递减。[维塔利克在这方面提出了](https://www.reddit.com/r/ethereum/comments/4rtpmm/on_coinlock_voting_futarchy_and_optimal/)一个变种，他称之为“二次币锁定投票”方法，其中N个代币让你进行 N * k 次投票，并锁定这些代币 k² 时间。这是一个很好的修改，因为随着时间的推移它调整了激励：越多的投票权需要决定的时间越长。在一个进入或离开社区几乎没有代价的代币化世界，这一点尤为重要。

* Voting with People or Money? | 用人还是用币来投票？

 A major problem with one person = one vote systems on the blockchain is their susceptibility to sybil attacks. Near zero cost to create infinite accounts means it’s easy to generate infinite votes. This is why the default model in proof of stake and Ethereum-based token governance is one token = one vote.

 一人一票的最主要问题是： 系统如何应对女巫攻击。创建帐户近乎零成本意味着可以产生无穷的投票。这就是为什么权益证明和基于以太代币的治理缺省模式是一币一票。

 Blockchain-based identity systems like [Civic](https://www.civic.com/) can help enable one person = one vote systems. However, anonymity is likely to be preserved in most cryptocurrencies. Identity gives each coin its own unique history, which can be subjectively judged to be more or less clean than that of another coin, causing [fungibility](https://en.wikipedia.org/wiki/Fungibility) to break down. One potential approach is a balance between identity and money: a fully verified identity gets 100% of the voting power of their money, a partially verified identity gets 50%, and an entirely anonymous identity gets 25%.

 像[Civic](https://www.civic.com/)这样基于区块链的身份识别系统可以帮助实现一人一票。但是，大多数加密货币可能会保留匿名性。身份会赋予每个代币自己独特的历史，这样可以主观地判断一个代币比其它代币更干净或更不干净，从而导致[可替代性](https://en.wikipedia.org/wiki/Fungibility)的崩溃。一种可能的方法是取得身份和金钱之间的平衡：完全验证的身份获得其金钱投票权的100％，部分验证身份获得50％，完全匿名身份获得25％。

 As mentioned in quadratic voting, other mechanisms which weight community members differently independent of real-world identity are likely to evolve. For example, a new token holder may have diminished voting power until they have been a member of the community for a while, similar to not being able to vote until you are a full citizen of a country.

 In any case, **today’s world would look a lot different if modern governments ran on voting with money, so this change in defaults is not to be taken lightly**.

 正如在二次方投票中提到的那样，其他不同的机制，如社区成员不依赖于其现实身份具有不同的权重的机制也可能发展出来。例如，一个新的代币持有者可能会减少投票权，直到他们成为社区成员一段时间，类似于只有当您是一个国家的正式公民时才能投票。

 无论如何，**如果现代政府用金钱投票，今天的世界将会有很大的不同，所以这种在默认上的改变是不能掉以轻心的**。

Finally, **reputation within a token community will be critical**. This is already shown through indirect means, where Vitalik’s suggestions carry a lot of weight in the Ethereum community. In a liquid democracy system reputation manifests in the number of votes delegated to a particular person. Someone with high reputation and no money could have 10 million Ether delegated to them and have tremendous governing power.

最后，**代币社区内的声誉将是至关重要的**。这已经通过间接手段显示出来，如 Vitalik 的建议在以太坊社区中占有很大的份量。在委任式民主制度中，授予特定人的选票数量体现了他的声誉值。信誉好但没有钱的人，也可能有10亿以上的以太托付给他们，并因此拥有巨大的执政权。

## Other Tools | 其他工具

Simple **off-chain futures markets have already shown themselves as a powerful tool**. In the recently proposed and contentious Bitcoin [SegWit2x](https://www.coindesk.com/explainer-what-is-segwit2x-and-what-does-it-mean-for-bitcoin/) fork, futures markets speculated on the expected value of SegWit2x vs. non-SegWit2x chains. The markets consistently valued a SegWit2x chain [at less than 20%](https://www.reddit.com/r/Bitcoin/comments/75xncv/2x_futures_prices_drops_below_02_btc/) of a non-SegWit2x chain for 3 weeks. Supporters of SegWit2x then [called off](https://lists.linuxfoundation.org/pipermail/bitcoin-segwit2x/2017-November/000685.html) their forking efforts because they felt they had “not built sufficient consensus”. While it’s hard to know exactly what caused them to reach this conclusion, it seems like futures markets were a strong indicator of lack of support.

简单的**链下期货市场已经显示出自己是一个强有力的工具**。在最近提出的有争议的比特币[SegWit2x](https://www.coindesk.com/explainer-what-is-segwit2x-and-what-does-it-mean-for-bitcoin/)分叉中，期货市场推测了SegWit2x与非SegWit2x链的预期价值。在3周的时间里，SegWit2x链的市场价值一直[低于非SegWit2x链20％](https://www.reddit.com/r/Bitcoin/comments/75xncv/2x_futures_prices_drops_below_02_btc/)。SegWit2x的支持者然后因为觉得自己“没有达成足够的共识”而[取消](https://lists.linuxfoundation.org/pipermail/bitcoin-segwit2x/2017-November/000685.html)了分叉的努力。虽然很难确切地知道是什么使得他们得出这个结论，但期货市场似乎是是否缺乏支持的有力指标。

![Futures markets on Bitcoin’s SegWit2x](https://cdn-images-1.medium.com/max/800/1*KSPwq45dIQJxAekdSwCakg.png)

Futures markets on Bitcoin’s SegWit2x 比特币的SegWit2x期货市场

Other tools are being built for governance and standardization at different layers. [ZeppelinOS](https://zeppelinos.org/) is [a series of basic libraries](https://github.com/OpenZeppelin/zeppelin-solidity) which are commonly being used as the base of Ethereum token systems, covering things like token sale mechanics, token vesting, and access controls to the treasury of the project. [Aragon](http://aragon.one/) is trying to create standard implementations of these systems in the same way Delaware C corporations implement corporations in a standard way.

其他工具正在为不同层次的治理和标准化而建立。[ZeppelinOS](https://zeppelinos.org/) 是[一系列基本库](https://github.com/OpenZeppelin/zeppelin-solidity)，通常被用作以太坊代币系统的基础，涵盖了代币销售机制，代币归属以及对项目财务的访问控制。[Aragon](http://aragon.one/)正试图以如特拉华州C公司以标准方式实现公司这样的方式创建这些系统的标准实施方式。

### Forking | 分叉

It’s worth noting that forking is always an option. Applying Albert Hirschman’s classic [voice or exit](https://en.wikipedia.org/wiki/Exit,_Voice,_and_Loyalty) paradigm for affecting change in a system, **voice is governance, weak exit is selling your coins, and strong exit is forking**.

We’ve seen many examples of forking so far, and this is great! In physical nations forking is nearly impossible. This was also the case in software until blockchains emerged. They make it easy to take all the code and state of a system and try a new path. In the Web 2.0 world, **forking is the equivalent of Facebook allowing any competitor to take their entire database and codebase to a competitor**. Don’t like how Facebook is operating it’s newsfeed? Create a fork with all the same code, social connections, and photos.

值得注意的是分叉总是一个可选项。使用阿尔伯特·赫希曼（Albert Hirschman）经典的[发表意见或退出](https://en.wikipedia.org/wiki/Exit,_Voice,_and_Loyalty)范式来影响系统的变化，**提出意见就是治理，弱势退出就是卖出你的代币，而强大的退出就是分叉**。

到目前为止，我们已经看到了很多分叉的例子，这真是太棒了！在实体国家分叉几乎是不可能的。区块链出现之前，软件也是如此。他们可以很容易地获取系统的所有代码和状态，并尝试新的发展路径。在Web 2.0的世界里，**分叉就等于Facebook允许任何竞争者把他们的整个数据库和代码库带给竞争对手**。不喜欢Facebook如何操作它的新闻源？就可以创建一个分叉用 Facebook 所有相同的代码，社交连接和照片。

**The ability to fork significantly reduces lock-in and increases diversity**, allowing many [more paths](https://medium.com/@FEhrsam/accelerating-evolution-through-forking-6b0bba85a2ba) to be tried than we would ever see in modern governments, central banks, or Web 2.0 companies. As in [corporate spinoffs](https://www.investopedia.com/terms/s/spinoff.asp), forking is also beneficial when two niche chains can more effectively serve distinct needs than one chain ineffectively serving both sets of needs.

However, it is still valuable to avoid hard forks when possible. A [hard fork](https://bitcoin.stackexchange.com/questions/9173/what-is-a-hard-fork) is a non-backwards compatible change. Downsides of hard forks include:

**分叉的能力显着减少了锁定并增加了多样性**，允许比现代政府，中央银行或Web 2.0公司所见到的[更多的途径](https://medium.com/@FEhrsam/accelerating-evolution-through-forking-6b0bba85a2ba)来尝试。和[企业衍生产品](https://www.investopedia.com/terms/s/spinoff.asp)一样，当两条链可以更有效地满足不同的需求时，分叉也是有利的，一条链无法满足这两套需求。

但是，尽可能避免硬分叉仍然是有价值的。一个[硬分叉](https://bitcoin.stackexchange.com/questions/9173/what-is-a-hard-fork)是一个非向后兼容式的改变。硬分叉的缺点包括：

1. Reducing network effects. Not everyone is speaking the same language anymore.

2. Creating work. Anyone who was using the forked protocol probably had their code broken. In a world that is increasingly interconnected through transparent and trustless code execution, these effects compound.

3. Reducing trust. Now that we’ve had a breaking change, those previously referencing the protocol must now go outside the blockchain and somehow figure out what the “right” new version is to use.

Because of the dramatically reduced friction for exit, the need for effective voice (governance) is more critical than ever. It is trivial to fork a blockchain and copy all of its code and state. So **the value isn’t in the chain of data, it’s in the community and social consensus around a chain**. Governance is what keeps communities together and, in turn, gives a token value.

1. 减少网络效应。不再是每个人都说同一种语言了。

2. 提高了工作量。任何使用分叉协议的人可能都会使他们的代码失效。在日益相互关联的世界中，通过执行透明和不可信的代码，这些效果将相互影响。

3. 减少信任。现在我们已经有了一个突破性的变化，那些以前引用的协议现在必须移出区块链，并且弄清楚“正确”的新版本需要使用哪些。

由于退出的阻力大大减少，对有效的发言权（治理）的需求比以往任何时候都显得更加重要。分叉区块链并复制其所有的代码和状态是平凡的。所以**价值不在数据链中，而在于围绕在链上的社区和社会共识**。治理就是让社区聚集在一起，并且反过来给予代币价值。

## Community Suggestions | 社区建议

**For users**: Spend more time looking at the governance system of your blockchain, less time on the issue of the day. **Current events are just a manifestation of the larger system that caused them**. So while it’s easy to get riled up by the news, the highest leverage point for change comes from designing or changing the system, not arguing about its current manifestations.

**For developers**: Try inflation funding. And if you are creating a new token using a simple 1 token = 1 vote system, **consider quadratic coin lock voting** as a low risk/high return alternative.

**For everyone**: Watch and learn from the experiments that will be run on the new on-chain governance systems.

对于用户来说：花更多时间看看区块链的治理体系，少花点时间在当前的问题上。
**当前事件只是一个引发它们的更大系统的体现**。所以虽然很容易受到新闻的冲击，但最大的变革力量来自于设计或改变系统，而不是争论它目前的表现。

对于开发人员：尝试通货膨胀。如果您使用简单的1币1票系统来创建新的代币，考虑**二次方锁定投票**作为低风险/高回报的选择。

对于每个人：对于将在新的线上治理系统上运行的实验多加观察和学习。

## Conclusion | 结论

Like organisms, the ability of a blockchain to succeed over time is based on its ability to evolve. This evolution will bring about many decisions on direction, and it is the governance around those decisions which most strongly determine the outcome of the system. **If programming in the system is important, the [metaprogramming](https://en.wikipedia.org/wiki/Metaprogramming) of the system itself is most important**.

像有机体一样，随着时间的推移，区块链成功的基础是其进化能力。这种演变会带来很多方向上的决策，而围绕这些决策的治理则是最强烈地决定了系统最终结果。**如果在系统中开发是重要的，则系统本身的[元编程](https://zh.wikipedia.org/wiki/%E5%85%83%E7%BC%96%E7%A8%8B)是最重要的**。

**I believe governance should be the primary focus of investors in the space**. The fundamentals of cryptoeconomics and overarching governance schemas of these networks are critical to survival, under-appreciated, and poorly understood. Investors can add significant value through the luxury of being able to observe and learn from multiple projects at one time. They should be active in the governance of the tokens they participate in and transparent with a community if they feel the design of the system can be improved.

**我相信治理应该成为投资者在这个领域的首要关注点**。密码经济学的基本原理和这些网络的总体治理模式对生存至关重要，但受到人们的重视和理解甚少。投资者可以通过在同一时间观察和学习多个项目的方式来增值。如果他们觉得系统的设计可以改进，他们应该积极参与他们支持的代币的治理和积极参与社区活动。

**We are birthing into existence systems which transcend us**. In the same way democracy and capitalism as systems determine so much of the emergent behavior around us, blockchains will do the same with even greater reach. These systems are organisms which take on [lives of their own](http://slatestarcodex.com/2014/07/30/meditations-on-moloch/) and are more concerned with [perpetuating themselves](https://en.wikipedia.org/wiki/Instrumental_convergence) than the individuals which comprise them. As technology stretches these systems to their limits, the implications become more pronounced. So we’d be wise to carefully consider the structure of these systems while we can. Like any new powerful technology, **blockchains are a tool that can go in many different directions. Used well, we can create a world with greater prosperity and freedom. Used poorly, we can create systems which lead us to places we [didn’t intend to go](https://www.youtube.com/watch?v=ST86JM1RPl0)**.

**我们是在超越我们的现实世界中诞生的**。以同样的方式，民主和资本主义体系决定了这么多在我们周围发生地行为，区块链同样如此，甚至范围更大。这些系统是[有自己的生活](http://slatestarcodex.com/2014/07/30/meditations-on-moloch/)的有机体，比包含它们的个体更关心延续自己。
随着技术发展，将这些系统发展到极限，其意义变得更加明显。所以我们必需明智地尽可能仔细考虑这些系统的结构。像任何新的强大技术一样，**区块链是一个可以沿着不同方向发展的工具。用得好，我们可以创造一个更加繁荣和自由的世界。用得不好，我们创建的系统将向着我们[不想去的方向](https://www.youtube.com/watch?v=ST86JM1RPl0)发展**。

Thanks to Vitalik Buterin, Buck Perley, Vlad Zamfir, Luke Duncan, Brian Armstrong, Ralph Merkle, Arthur Brietman, Julia Galef, Dominic Williams, Luis Iván Cuende, Matt Huang, Demian Brenier, Andy Coravos, Chris Burniske, Jim Posen, Balaji Srinivasan, Scott Nolan, Elad Gil, Chris Dixon, Maksim Stepanenko, Albert Wenger, Simon de la Rouviere, Sophia Cui, Lucas Ryan, Jay Graber, and Jeromy Johnson for conversations and ideas which contributed to this post.

感谢 Vitalik Buterin, Buck Perley, Vlad Zamfir, Luke Duncan, Brian Armstrong, Ralph Merkle, Arthur Brietman, Julia Galef, Dominic Williams, Luis Iván Cuende, Matt Huang, Demian Brenier, Andy Coravos, Chris Burniske, Jim Posen, Balaji Srinivasan, Scott Nolan, Elad Gil, Chris Dixon, Maksim Stepanenko, Albert Wenger, Simon de la Rouviere, Sophia Cui, Lucas Ryan,
Jay Graber 和 Jeromy Johnson 为这篇文章做出的贡献。

----------------------------------------------------

#### 区块链中文字幕组

致力于前沿区块链知识和信息的传播，为中国融入全球区块链世界贡献一份力量。

如果您懂一些技术、懂一些英文，欢迎加入我们，加微信号:w1791520555。

[点击查看项目GITHUB，及更多的译文...](https://github.com/BlockchainTranslator/EOS)

#### 本文译者简介

鱼 区块链技术爱好者，欢迎加微信号oscnet交流。

本文由币乎社区（bihu.com）内容支持计划赞助。

版权所有，转载需完整注明以上内容。

----------------------------------------------------
