# IERC 多核挖矿程序


[联系作者](https://twitter.com/chenmin22998595)


生成10笔ierc-m5交易耗时2分钟 (8核cpu)

![](./img.png)

测试地址

https://holesky.etherscan.io/address/0xd19162560690227c8f71a21b76129e1eb05575a9


### 使用方式

1. 在[这里](https://github.com/minchenzz/ierc-miner/releases)下载对应操作系统的版本,解压缩程序

2. 修改目录下的config.txt文件,改成你自己的配置

3. 双击ierc_miner_windows.exe运行

```toml
# 你的私钥 带0x前缀
# 你要改这个
private_key = "0x440d58ea9c07ab873295a71f24d41f58776b3732000643178dd351c991b53e48"
# rpc  主网: https://1rpc.io/eth  holesky测试网: https://1rpc.io/holesky
# 你可以不改这个
rpc = "https://1rpc.io/eth"
# token
# 你要改这个
tick = "ierc-m5"
# 数量
# 你要改这个
amt = 1000
# 难度
# 你要改这个
prefix = "0x00000"
# mint数量
# 你要改这个
count = 10
# gas优先费用
# 你可以不改这个
gas_tip = 3
# 最大gas费用
# 你可以不改这个 这个值必须要比ethgas高
gas_max = 50
```

注意: 
1. 先1张测试成功后再加数量, 或者使用其他gas低的链rpc先测试使用
2. 有时因为算力过高或者难度过低,会连续挖到两个,两笔交易在同一区块内打包时,官方只会认第一个,因此有时会打到无效的,如介意gas损失可以把count设置为1,一次一次打