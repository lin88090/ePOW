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

輸入指令找到私鑰路徑
```
solana config get
```

複製Keypair Path後面那段路徑，接著輸入cat(空格)剛剛複製的，會出現一段數字那是你的私鑰，連同括號複製下來導入錢包


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

7.運行挖礦(後面的8可以更改成你cpu的核心數，但要預留一點)

```
./bitz collect --cores 8     
```

8.查詢挖了多少

```
./bitz account
```

9.將挖到的幣提取到錢包

```
./bitz claim
```
