# ePOW

1.Install Solana

```
curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash
```

2.添加环境变量

```
export PATH="$HOME/.local/share/solana/install/active_release/bin:$PATH"
```

3.创建新钱包，会有助记词以及创建的id.json 这个文件里面的就是私钥一定要存，因为助记词导入不一定能找回原来这个地址

```
solana-keygen new
```

4.修改RPC

```
solana config set --url https://eclipse.helius-rpc.com/
```

5.挂后台

```
screen -S eclipse
```

6.附加执行权限

```
chmod +x bitz
```

7.运行挖矿

```
./bitz collect --cores 8     你服务器多少核就填多少，当然别把cpu全跑满了不然卡
```

8.查询挖了多少

```
./bitz account
```

9.将挖到的币提取到钱包

```
./bitz claim
```
