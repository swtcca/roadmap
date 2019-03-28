# Estimated Workloads (rough)

### 改进钱包支持所有联盟链
- 2 周/人
- 目标
  - 保证swtc-lib的兼容性
  - 统一井通和井畅钱包功能
  - 相关测试

### 独立swtc-transaction成包
- 1 周/人
- 内容
  - 交易签名
  - 需要实现非ws(api / service node)获取sequence
  - 相关测试

### 改进serializer
- 3-4 周/人
- 内容
  - 理解ripple的实现 -binary-codec
  - 理解井通的实现
  - 设计并且提供完整测试

### 增加 service node 的支持
- 1 周/人
  - 新成包

### 文档
- jingtum-lib pdf文档中的例子通走一遍, markdown格式或readthedocs
  - 2 天/人
- swtc-apps-examples 更新模版功能展示添加框架支持
  - 1 周/人

### 用typescript 实现钱包以上， 提供上下文关联的帮助
- 2 周/人
- 内容
  - 对钱包和lib中的所有的变量/函数/类提供类型声明

### 项目管理
- 3 周/人
- 内容
  - 格式化代码, 语法检查，集成测试
  - 代码评审
  - 测试及自动化
  - 发布新版本包
  - 追踪jingtum-lib和jcc_jingtum_lib更新及修订
  - 更新依赖包
  - 统筹协调
