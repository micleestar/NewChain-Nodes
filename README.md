## NewChain-Nodes Testnet deploy instructions/测试网接入指南

1. Purchase Elastic Compute Service(ECS), you may refer to folowing link/购买云服务器，购买云服务器可参考:

https://aws.amazon.com/ec2/

https://www.aliyun.com/product/ecs?spm=5176.12825654.eofdhaal5.2.36722c4aSDIOpf

2. Deploy testnet as per following instructions to launch block synchronizing/按照下面链接代码操作部署测试网，启动区块同步：

https://github.com/newtonproject/newchain-deploy

3. Check the progress of block synchronizing/查看区块同步进度：

3.1 Execute following command to check the synchronized block height/执行命令查看同步好的区块高度（number字段对应值）；

sudo supervisorctl tail -f newchain stderr

3.2 Make sure synchronization block is completed and same to the latest testnet block height at below link/确保已同步好的区块链高度与下面连接中的测试网最新区块高度一致；

https://explorer.testnet.newtonproject.org

4. Fill in and submitt following info./填写提交如下内容:

4.1 Node name(public)/对外显示名称 （公开）：

4.2 Minner address(public)/进行打包出块的miner地址 （公开）：

4.3 RPC Url(public)/对外RPC Url（可以是服务器地址加端口）（公开）：

4.4 Node operator name(public)/运行节点主体（个人、社群、组织）名称（公开）：

4.5 Contacts such as email, telegram account(public)/节点负责人及联系方式（手机、邮箱、微信、telegram等等均可）：

4.6 NewPay/NewMask Mainnet NEW address/用于接收测试网矿工纪念币的主网NEW地址(NewPay或者NewMask)：

5. Execute codes as per following instructions to upgrade to acchount node/按照下列链接中说明操作将只读节点升级为记账节点：

https://github.com/newtonproject/newchain-deploy/wiki/NewChain-TestNet-mine

6. Copy minner address and replace 000 in following command to request other node to execute it and approve your upgrade/使用Minner地址粘贴替代下列代码中的000，请求其他节点执行代码:

/data/newchain/testnet/bin/geth attach /data/newchain/testnet/nodedata/geth.ipc --exec 'clique.propose("000", true)'

7. Wait for the approval and executing codes from other nodes operators/等待其他节点执行代码批准加入
