# Trinity Tutorial

## How to start Trinity from Zero



### Build Up Envirment

First step is to clone the trinity project from github:

```
git clone https://github.com/trinity-project/trinity.git
```

After finished cloning, lets begin from source code

```
cd trinity
```

Create and activate virtual environment

```
virtualenv -p  venv

source venv/bin/activate
```

Before start anything we need to Install trinity node requirement package

```
pip3 install -r requirements
```



### Start Trinity Routing Node Gateway

Run the Gateway service

```
cd gateway
```

```
python3 start.py
```



If Success, your terminal should looks like this:

```
(venv) johnnyhsieh@Johnnyde-MacBook-Pro-3:~/desktop/trinity/trinity$ ls

Configure.json  TX/             contract/       exception/      log/            tokenswap/      wallet/

LICENSE         api.py          docker/         gateway/        model/          trinity.py

README.md*      blockchain/     docs/           lightwallet/    requirements*   venv/

(venv) johnnyhsieh@Johnnyde-MacBook-Pro-3:~/desktop/trinity/trinity$ cd gateway

(venv) johnnyhsieh@Johnnyde-MacBook-Pro-3:~/desktop/trinity/trinity/gateway$ ls

Pipfile         _wallet.py      ctest/          gateway.py*     message.py*     requirements    spvtable.py*    statistics.py   topo.py

Pipfile.lock    config.py*      discarded/      glog.py         network/        routergraph.py  start.py        t.json          utils.py*

(venv) johnnyhsieh@Johnnyde-MacBook-Pro-3:~/desktop/trinity/trinity/gateway$ python3 config.py

(venv) johnnyhsieh@Johnnyde-MacBook-Pro-3:~/desktop/trinity/trinity/gateway$ screen -S TrinityGateway



(venv) johnnyhsieh@Johnnyde-MacBook-Pro-3:~/desktop/trinity/trinity/gateway$ python3 start.py

[RPC]: 2018-11-09 13:20:38,798 INFO    : RPC server is serving on ('0.0.0.0', 8077)

[TCP]: 2018-11-09 13:20:38,798 INFO    : TCP server is serving on ('0.0.0.0', 8089)

[WST]: 2018-11-09 13:20:38,798 INFO    : WST server is serving on ('0.0.0.0', 8766)

###### Trinity Gateway Start Successfully! ######
```



### Start A Wallet

Start Trinity CLI

- Testnet Wallet

```
python3 prompt.py
```



Lets check the CLi command a little bit

```
Connect the Gateway
trinity>help
help
quit
create wallet {path}
open wallet {path}
close
wallet
send {asset} {address} {amount}
export wif {address}
export nep2 {address}
import token {token symbol}, {script hash}tx {txid}
channel enable
channel create {partner} {asset_type} {deposit}
channel tx {payment_link}/{receiver} {asset_type} {count}
channel close {channel}
channel peer
channel payment {asset}, {count}, [{comments}]
channel qrcode {on/off}
channel show uri
channel show trans_history {channel}
channel depoist_limit
```



Trinity is a side chain of NEO so their CLI are very similar

So they are using the same command to open a wallet

```
trinity>create wallet test.wallet
[Password 1]> ***********
[Password 2]> ***********
Wallet {
    "path": "test.wallet",
    "accounts": [
        {
            "address": "AGEK5WnbMGrz8eyST7JWYCoPazqx56VBdP",
            "pubkey": "03d72b324b586c03be0dbcdc0f5516d4954e22030727155b1bed8f0e0c93c31107",
            "assets": {
                "NEO": 0,
                "GAS": 0,
                "TNC": 0
            }
        }
    ]
} 
Channel Function Enabled

```



As soon as you open up a wallet you can go to trinity faucet to request so testnet token

<http://tfaucet.trinity.ink:8033/>

paste you address on it.

And you can gain 10 TCN each time you request.



Before you can start a channel you need two things

One 80000 TNC token



Second your own uri

```
trinity> channel uri
03d72b324b586c03be0dbcdc0f5516d4954e22030727155b1bed8f0e0c93c31107@127.0.0.1:8089
```

So 03d72b324b586c03be0dbcdc0f5516d4954e22030727155b1bed8f0e0c93c31107@127.0.0.1:8089 is the parameter that you need inorder to open a channel

```
trinity> channel create xxxxxxxxxxxxx@xx.xx.xx.xx:xxxx TNC 80000
```



Now you have open up a trinity channel !
