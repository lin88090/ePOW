# ePOW

```
https://github.com/lin88090/ePOW.git && cd ePOW
```

1.Install Solana

```
curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash
```

2.添加環境變量

```
export PATH="$HOME/.local/share/solana/install/active_release/bin:$PATH"
```

3.創建新錢包，會有助記詞以及創建的id.json 這個檔案裡面的就是私鑰一定要存，因為助記詞導入不一定能找回原來這個地址

```
solana-keygen new
```

4.修改RPC

```
solana config set --url https://eclipse.helius-rpc.com/
```

5.掛後台

```
screen -S eclipse
```

6.附加執行權限

```
chmod +x bitz
```

7.運行挖礦

```
./bitz collect --cores 8     你服务器多少核就填多少，当然别把cpu全跑满了不然卡
```

8.查詢挖了多少

```
./bitz account
```

9.將挖到的幣提取到錢包

```
./bitz claim
```
