# Estimated Workloads (rough)

### 改进钱包对所有联盟链的支持
- 2 周/人
- 高优先级
- 目标
  - 保证swtc-lib的兼容性
  - 统一井通和井畅钱包功能
  - 相关测试

### 独立swtc-transaction成包
- 1-2 周/人
- 高优先级
- 内容
  - 交易签名
  - 需要实现非ws(api / service node)获取sequence
  - 相关测试

### 改进serializer
- 3-4 周/人
- 低优先级
- 内容
  - 理解ripple的实现 -binary-codec
  - 理解井通的实现
  - 设计并且提供完整测试

### 增加 service node 的支持
- 1 周/人
- 低优先级
- 内容
  - 新成包

### 文档
- jingtum-lib pdf文档中的例子通走一遍, markdown格式或readthedocs
  - 3 天/人
- swtc-apps-examples 更新模版功能展示添加框架支持
  - 2 周/人

### code refactor (实现钱包以上， 提供上下文关联的帮助)
- 5 周/人
- 低优先级
- 内容
  - class替代function constructor
  - typescript包装
  - 对钱包和lib中的所有的变量/函数/类提供类型声明

### 保持上游更新的修订
- 1 周/人
- 高优先级
- 内容
  - 追踪ripple-xyz, jingtum-lib和jcc_jingtum_lib更新及修订

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
