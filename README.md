# 游戏信息
EOS挖矿游戏是ejc.cash团队开发的一款挖矿类游戏。玩家的每一份投入除了很少的一部分(5%)奖励给开发者外，其余的将全部进入奖池,作为达成目标矿工的奖励。矿工奖励规则完全透明（详见矿工奖励规则)。除此之外矿工还会以５:1的比例获得平台代币EJC,矿池资金最终归全体矿工所有（开发团队完全靠5%的奖励维持），当未来某天由于某种不可抗力，或由全体矿工达成共识需要结束游戏时，所有矿工将根据持有EJC量的多少瓜分所有矿池资金。

# 矿工奖励规则
矿工的每一次挖矿（发送至少0.1000EOS至合约地址）后都会得到一个交易ID,该交易ID为一个16进制的64位数字（或称字符串）。定义该字符串开头‘０’的个数即为本次挖矿的难度。例如"00057bbfb72640471fd910bcb67639c22df9f92470936cddc1ade0e2f2e7dc4f" 的难度是３，但"ea5220cef45dda6b11c677b86bcd5e00bc66b4898644acee91b2ae36f09dace6" 的难度是０。只有难度至少达到１才能得到相应的
挖矿难度与挖矿奖励之前的关系如下表所示

| 挖矿难度 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 大于或等于8 |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 挖矿奖励 | 10X | 100X | 1000X | 10000X | 矿池50% | 矿池60% | 矿池70% | 矿池80% |


当挖矿难度为1、２、３、４时，矿工奖励的多少将与其投入的Power有关，最低得到10倍奖励，最高可得到10000倍奖励。
当挖矿难度大于4时,矿工的奖励将由当前矿池内的资金量决定，最低可获得矿池资金的50%，最高可获得矿池资金的80%

# 游戏公平性
- 游戏过程中，仅开发团队获得矿工投入的5%作为游戏维护开发成本，其余95%全部进入奖池。后期投入的矿工不会分配任何EOS给前期投入的矿工，所以不存在“先手优势”

- 矿工每次挖矿至少投入0.1000 EOS,不设上限，交易ID(transaction_id)完全由EOS网络生成，就像BTC挖矿一样，矿工只能通过不断的尝试使得产生的交易ID符合相应的难度规则才可以得到相应奖励，没有矿工可以控制自己产生的交易ID,这完全保证了挖矿结果的公开和公平性。广大矿可以通过下面命令查看所有矿工奖励数据
```
cleos get table eosejcminers eosejcminers rewards
```

- 由于矿工的每次交易都仅能产生一个交易ID(transaction_id)，所以无论矿工投入的多少，仅能影响低难度情况下的奖励数量(奖励规则见"游戏规则")
为了最大限度的保证公平性，合约对每个矿工的memo内容进行了限制（具体内容见合约），请广大矿工通过本站进行挖矿
- 游戏过程中矿工将会得到ejc.cash空投的糖果(EJC)，矿池内所有的EOS为全体矿工所有，如果游戏结束，广大矿工将会根据持有EJC的数量平分矿池内所有EOS
- 合约代码已开源，并通过开源验证，大家可以通过以下两个链接进行查看
  - [GitHub](https://github.com/ejccash/eosejcminers)
  - [慢雾验证](https://eos.slowmist.io/contract/eosejcminers)
- EJC.CASH 至力于打造成为开源、公平、区块链游戏平台，平台将会陆续推出新的更好玩的玩法

# 游戏阶段
- 由于游戏规则限制，不会出现"先手优势"，早期参与的玩家，和后期参与的玩家得到奖励的机会是均等的，所以游戏不设定起始时间，以推广日期为准。


# 关于ejc.cash

ejc.cash 团队致力于打造去中心化的娱乐平台，虽然现阶段还需要团队账户参与游戏的开奖环节，（这是由于EOS交易模式限制造成，只有交易完成后才能得到交易ID,在合约中无法得到交易ID），所以现阶段该游戏属于半中心化产品（但这并不影响公开、公平、公正），但随着EOS的发展，我们也会提出自已的建议，在将来可以将本游戏改成真正的去中心化产品。

# 相关帐户

- eosjoycenter    ejc.cash官方账户(也是本游戏中开发奖励账户)
- eosejcminers    本游戏合约账户
- ejcoinstoken　　　EJC token帐户
