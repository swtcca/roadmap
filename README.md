# roadmap 路线图

---

## [SWTCAPLAN A计划](https://github.com/swtcca/aplan)

### 目标 - 改进公链生态
> #### 提供可靠的基于公开节点的websocket公共访问服务
> #### 提供可靠的基于公开节点的non-websocket公共访问服务
> #### 提供基于生态节点的定制访问服务

### 背景 - 问题
> #### 井通的api服务存在安全性问题 而且不稳定不可靠
> #### 井畅的rpc服务作为公司的服务 有些应用不期望依赖
> #### 井通的节点历来没有开放的意愿
> #### [开放的公链生态节点可靠性非常低 < 50%](http://www.swtcdocs.org/zh_CN/latest/wiki/node/) 公链印象差 开发体验差

### 方案
> #### 基于生态节点，动态更新可用的websocket节点列表并且以固定的方式提供
> #### 开发安全的公共访问服务及对应的客户端库，部署至部分公共生态节点 (可以随负载调整规模)
> #### 基于生态节点，动态更新可用的non-websocket节点列表并且以固定的方式提供
> #### 集成到swtc-xxx开发库可以默认提供分布式中大型应用访问支持
> #### 额外: 节点的管理可以按需提供有意义的公链交易数量

### 支出
> #### 合适的激励，按照管理收集的数据给予部分节点
> #### 设计 2人天， 开发 15人天(服务端/客户端/管理), 测试 3人天 文档 5人天
> #### 管理 2人天/月

---

## [SWTCLIB 开发库 - 已完成](swtclib)

