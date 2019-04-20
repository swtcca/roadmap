# roadmap

### 目标
> #### 试验swtc-lib, 提高开发体验
> #### 反馈促进官方库
> #### 创建合适的样例和效率工具

### 可视
- ![图示](https://raw.githubusercontent.com/swtcca/roadmap/master/images/swtclib.png)

### 关系
- jingtum-lib == **swtc-lib** == jcc_jingtum_lib
- jingtum-base-lib == **swtc-wallet**
- jcc_jingtum_base_lib == **swtc-factory**
- 主要包 
  - swtc-lib
  - **swtc-transaction** with local sign and submit functionality
  - swtc-serializer
  - **swtc-utils**, **swtc-api** **swtc-toolset**
  - swtc-factory (includes swtc-wallet swtc-base-lib)
  - swtc-keypairs
  - swtc-address-codec
  - swtc-chains

### 增强
1. 格式化代码 - finished
2. 净化serializer - finished
3. 分离transaction - finished
4. 用class实现 - factory api toolset 
5. 效率工具 swtc-toolset
6. 用typescript 实现， 提供上下文关联的帮助 - swtc-api
7. 完善示例 - in progress
8. 添加测试及测试自动化 - in progress

### 开源参与
- 所有swtc-xxyyzz代码仓库遵循统一要求
  - 通过PR提交代码更改 - clone push
  - 提交时强制代码格式化 - prettier
  - travis集成 - test lint on submit and daily cron
- 默认发布es6标准的库
- 测试node版本 - 钱包以下v6, 钱包 钱包以上v8
- 选择支持库时要求零配置webpack和browserify
- 建议步骤
  - fork代码仓库
  - clone到本地
  - checkout工作分支
  - [可选]启用travis
  - 工作
  - 提交 测试
  - 同步 PR (尽量提供相对完整的功能实现, 尽量提供相应的测试)
  - 同步
  - 从第三步再开始
