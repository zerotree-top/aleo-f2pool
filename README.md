# f2pool鱼池拦截抽水 aleo-f2pool

#### 介绍
鱼池锄头抽水非常之多 给你100m的算力其实额外抽了你50m左右的算力，本软件可以让你拦截到这50m的算力给自己分配或者额外两个账号按比列分配
目前测试期间 自行测试收益是否稳定再跑 
服务器拦截软件ubantu下载地址：wget 154.205.9.27/aleo/aleo-f2pool或者https://github.com/zerotree-top/aleo-f2pool/blob/main/aleo-f2pool.zip 自行解压出来即可

windows版本154.205.9.27/aleo/aleo-f2pool.exe
##########说明############
windows使用需要开代理翻墙、
建议全用ubantu系统香港服务器  机器少随便买个便宜几十的就行 机器多则买配置高的 我购买服务器的地址为https://www.diyvm.com/page.aspx?c=referral&u=90876
windows使用需要开代理翻墙、
备用软件下载地址linux版本：https://wwoz.lanzouk.com/iPPXG2a7qahi https://github.com/zerotree-top/aleo-f2pool/blob/main/aleo-f2pool.zip
windows版本：https://wwoz.lanzouk.com/isw522a7qluh 
鱼池miner锄头使用11.49后缀的版本我上传到仓库（https://gitee.com/aleo-f2pool/proxy/raw/master/aleominer-2.11.49.tar.gz）

#########教程##########

全部比例给自己的配置如下 （网页格式不对建议在本仓库下载配置文件进行编辑）
  1.在你的软件存放目录里创建一个config.json文件填入一以下内容修改你的账号保存：

{
    "host": "aleo-asia.f2pool.com",
    "port": 4400,
    "localPort": 1572,
    "commissionAccounts": ["鱼池挖矿账号"],
    "commissionRates": [1]
}


 再同一个目录下./aleo-f2pool运行即可-如果无法运行请给软件权限
给权限命令为chmod 777 aleo-f2pool   
随后./软件名称运行   （Rates默认1就是百分百给自己账号只需要修改账号即可）

2.把软件挂后台运行步骤：配置json文件配置后在软件目录下输入：nohup ./aleo-f2pool > aleo.log 2>&1 &

查询运行状态输入tail -f aleo.log 即可查询 
运行以下命令来检查程序是否在后台运行：ps aux | grep aleo-f2pool
日志显示正在监听就是运行成功！
第二种方式也是在目录下输入screen -S aleo 进入到窗口 输入./aleo-f2pool 即可运行随后键盘ctrl +同时按键盘a和d返回
后续查看状态只需要输入：screen -r aleo 即可进入运行窗口
3.中转配置后 矿机飞行表矿池地址填写你的服务器ip和端口例子：130.250.133.5:1572(鱼池miner锄头使用11.49后缀的版本）好了奔放把！


如果想两个账号分配的具体配置 在下载好的同级目录下，创建一个config.json文件，填入以下内容：
{
    "host": "aleo-asia.f2pool.com",
    "port": 4400,
    "localPort": 1572,
    "commissionAccounts": ["鱼池账号1", "鱼池账号2"],
    "commissionRates": [0.9, 0.1]
}

host为鱼池挖矿地址（默认不动如果鱼池有更新则替换）

port为鱼池端口（鱼池有更新则替换

localPort内的1572为你自己设置的本地监听端口服务器（自己修改自己想要的端口，记得设置的什么就开放防火墙安全组的这个端口）

Accounts 和 Rates 是配对使用的，Accounts 鱼池账号的数量和 Rates 的数量需要保持一致。

Rates 表示对应账号的分成比例，假如 0.9 表示 commissionAccounts 的第一个账号的佣金为 90%，第二个账号的0.1佣金为 10%。·分成比列Rates 内的数字相加不能超过 1。
