# 第一章：走进 Web3 世界

1. 简单描述一下本地开发、部署合约的流程
   
   1. 环境的搭建，常用选择hardhat框架，或者foundry框架进行开发
   2. 搭建项目：foundry框架为例，使用`forge init `脚手架指令快速搭建项目, 
   3. `src`文件夹下进行合约相关开发 ,`script` 文件夹下进行脚本开发，`test`文件夹下进行测试代码编写
   4. 本地可以使用`anvil` 快速起一个本地测试链，或者通过指令指定rpc-url 将合约部署到指定网络
   
2. 简单描述一下用户在使用一个 DApp 时与合约交互的流程
   1. Dapp连接区块链钱包
   2. 用户在Dapp上进行各种操作，前端通过各种用户操作调用对应的abi接口。
   2. 钱包收到通知，用户同意后链上发起交易

   4. 交易签名并广播

   3. 合约执行
   4. 交易若失败则回滚，并抛出异常
   5. 交易确认，可在对应区块链网络上验证交易

3. 通读[「区块链黑暗森林自救手册」](https://github.com/slowmist/Blockchain-dark-forest-selfguard-handbook/blob/main/README_CN.md)，列出你觉得最重要的三个安全技巧

-  保护好私钥和助记词，不可以泄露给任何人，必要情况下可以使用冷处理，手写之类保存
-  发生交易的时候要第一时间验证信息，不要随意授权签名
-  陌生不安全的插件，软件等一定要核实清楚再安装
- 测试钱包和个人钱包分离，个人钱包如果担心的话可以尽量少放资金，有存储需求可以使用冷钱包等
