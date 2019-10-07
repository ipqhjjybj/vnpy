# 后面会开源做市套利策略， 这个策略已经用了两年了，依旧有效。。

想做区块链开发或者做其他市去了，策略有点不太想写了，就当开源出来，分享下。

策略思路很简单， 多市场套利， 重点是在一个流动性差的市场进行挂单， 等到这个流动性差的市场成交之后， 在流动性好的市场 快速补单回来。

因为数字火币市场， 最主要要解决的问题是， 经常交易所断线，所以策略用python开发 远比c++好， 远没有到拼速度的时候， 稳定性更重要。

因为市场上总有人一次 吃N档单子， 这样的话，挂单依然是有机会成交的。

# python版本
python 2.7 only

# 目录结构
在 api同级目录新增 ConfigProduce 文件夹
在 trader/app/里 新增 MMTrading 文件夹

在 examples下新增 MMTrading_server 文件夹

# 如何运行
在一台 Linux服务器上 , 进入MMTrading_server, 配置好  MMCompleteSetting.json ，也就是要套利的交易对
之后运行

python main.py

nohup bash start_all.sh &

即可运行程序


# License
MIT License
