[保持软件库对上游的更新](update.md)

# Estimated Workloads (rough)
> ## 工作量估计
> ## 数据
> > - 相关github代码仓库 **35**个
> > - 相关npm包/版本超过 **250**个

### 改进钱包对所有联盟链的支持
- 2 周/人
- 高优先级
- 目标
  - 保证swtc-lib的兼容性
  - 统一井通和井畅钱包功能
  - 相关测试
> #### 两人天 研究改进ripple-address-codec x-address-codec, 创建并重构swtc-address-codec
> #### 两人天 研究改进ripple-keypairs, 创建并重构swtc-keypairs
> #### 两人天 创建swtc-wallet, swtc-base-lib, 修改兼容jingtum-base-lib.
> #### 两人天 创建swtc-factory, 修改兼容jcc_jingtum_base_lib
> #### 两人天 确保最佳兼容性, 所有包支持零配置webpack
> #### 一人天 重构swtc-wallet, 支持所有联盟链
> #### 三人天 反复测试

### 独立swtc-transaction成包
- 1-2 周/人
- 高优先级
- 内容
  - 交易签名
  - 需要实现非ws(api / service node)获取sequence
  - 相关测试
> #### 一人天 创建swtc-utils包
> #### 一人天 独立swtc-transaction包
> #### 二人天 创建swtc-lib包
> #### 三人天 从swtc-lib中迁移所有transation相关的方法到swtc-transaction包中
> > ##### buildPaymentTx buildAccountSetTx buildRelationTx buildOfferCreateTx buildOfferCancelTx
> > ##### deployContractTx callContractTx
> > ##### 相关的所有_xxxYYY
> #### 一人天 增加基于jingtum-api服务的签名和submit()
> #### 二人天 增加基于jingtum-api服务的setSequencePromise(), signPromise(), submitPromise()及相应的私有方法
> #### 五人天 测试调试修改
> > ##### 添加基于jingtum-api服务的test_transaction_additional.js
> > ##### 添加基于swtc-lib服务的test_transaction_additional.js test_remote_additional.js

### 改进serializer
- 3-4 周/人
- 低优先级
- 内容
  - 理解ripple的实现 -binary-codec
  - 理解井通的实现
  - 设计并且提供完整测试
> #### 五人天 研究ripple-binary-codec的代码
> #### 三人天 研究jingtum-lib的lib/代码
> #### 二人天 研究jcc_jingtum_lib的lib/代码
> #### 二人天 基于swtc-factory创建swtc-serializer包
> #### 一人天 基于swtc-wallet创建swtc-serializer包
> #### 二人天 格式化，语法检查, 清理
> #### 三人天 测试

### 增加 service node 的支持
- 1 周/人
- 低优先级
- 内容
  - 新成包
> #### 改为对jingtum-api rest服务的支持
> #### 二人天 所有的jingtum-api方法作出包装
> #### 一人天 屏蔽所有不安全的操作
> #### 三人天 实现本地签名, 增加所有缺失的操作，功能上趋同swtc-lib
> #### 三人天 测试调试修改

### 文档
- jingtum-lib pdf文档中的例子通走一遍, markdown格式或readthedocs
  - 3 天/人
- swtc-apps-examples 更新模版功能展示添加框架支持
  - 2 周/人
> #### [github](https://github.com/swtcca/swtcdoc)
> #### [website](http://swtc.daszichan.com)
> #### 三人天 swtc-lib文档， 涵盖所有jingtum-lib中的内容，针对性的做出更新
> #### 三人天 WEB应用(常规，打包，vuejs, react, angular)实例
> #### 两人天 移动应用nativescript实例
> #### 一人天 桌面应用electron实例
> #### 持续更新

### code refactor (实现钱包以上， 提供上下文关联的帮助)
- 5 周/人
- 低优先级
- 内容
  - class替代function constructor
  - typescript包装
  - 对钱包和lib中的所有的变量/函数/类提供类型声明
> #### 三人天 格式化，语法, 清理
> #### 五人天 class替代 swtc-wallet, swtc-transaction, swtc-lib, swtc-x-lib
> #### 五人天 typescript学习 规划
> #### 四人天 typescript实现swtc-wallet, swtc-transaction, swtc-lib, swtc-api, swtc-x-lib
> #### 三人天 type定义
> #### 七人天 测试调试修改

### 保持上游更新的修订
- 1 周/人
- 高优先级
- 内容
  - 追踪ripple-xyz, jingtum-lib和jcc_jingtum_lib更新及修订
> #### 更新到 jingtum-lib v2.x
> #### 含solidity合约支持

### 项目管理
- 2 周/人
- 高优先级
- 内容
  - 格式化代码, 语法检查，集成测试
  - 代码评审
  - 测试及自动化
  - 发布新版本包
  - 更新依赖包
  - 统筹协调
> #### 三人天 设置调试更新prettier, eslint, tslint
> #### 三人天 发布包 - 目前在npmjs上手工发布的相关的包版本已经超过250个
> #### 三人天 采用lerna集中管理 

### 对于新功能或者特性，基本上以适配jingtum-lib为主
- 特殊要求，工作量不定

-------------------------------------------------------------

## 计划外工作

### swtc-api 实现及文档
- 1 周/人
- 内容
   - 实现 - 已完成
   - swtc-api所有包装和实例文档
   - jingtum-api对应文档

### 支持井通联盟连
- 3 周/人
- 内容
   - 新包 x-swtc-lib (同等支持jingtum, bizain, call, stm, guirentong ...)
   - refactor swtc-serializer swtc-utils swtc-transactions swtc-lib/*
   - adjustment and cleaning
   - test
   - readme
> #### 三人天 创建swtc-x-lib
> #### 五人天 重构swtc-serializer swtc-utils swtc-transactions swtc-lib/*
> #### 三人天 基于类实现，优于井畅基于实例的实现
> #### 五人天 测试调试修改
> #### 一人天 文档

### javascript现代化改进
- 2 周/人
> - 零配置webpack 和 browserify支持, 为几乎所有的web应用框架打开大门
> - swtc-toolset 探索对jingtum-lib的现代化改造
> - swtc-xyz 直接内置server.submitPromise() request.submitPromise() remote.connectPromise(), remote.makeAmount(), remote.makeCurrency()
> - 相应的test_xyz_additional.js测试

### solidity合约支持
- 1 周/人
> - 新包swtc-tum3
> - 添加相应的方法到现有包中
>   - initContract() invokeContract()到swtc-transaction包
>   - initContract() invokeContract() buildContractInitTx() buildContractInvokeTx()到swtc-lib
>   - initContract() invokeContract() buildContractInitTx() buildContractInvokeTx()到swtc-x-lib
>   - initContract() invokeContract() buildContractInitTx() buildContractInvokeTx()到swtc-api
> - 更新contructor(), 加入solidity参数，精心实现以保证程序包的最佳兼容性
> - 测试调试修改，反馈井通

### 移动应用(nativescript到目前为止独家原生支持, react native)
- 六周/人
> - 四十人天 基于jingtum-lib的探索，使用nativescript-nodeify. (持续时间跨度超过一年，历经大小版本，试验数百上千次)
> > - 产品尝试已在八个月以上，未尝停止 https://github.com/swtc-ca/dasswtc , 深切感受jingtum-lib糟糕的兼容性耽误尝试者光阴
> - 五人天 成果简化为swtc-nativescript (含swtc-brorand, swtc-lib@nativescript, 测试，调试，文档) 并融合内置于开发库中
