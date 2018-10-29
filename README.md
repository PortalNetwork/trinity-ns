![Trinity Name Service](./assets/title.jpg)

> 📖🔍 Documents of the Trinity Name Service.

# Overview

## 💡 What is Trinity?
Trinity is a state channel that is an offchain scaling scheme for NEO, and it applicable to NEP-5 standard tokens and NEO UTXO assets. It is a NEO version lighting network.
State channels can be seen as exclusive trade channels to participants, complicated processing data will be offchain, only the final balance will be settled on NEO mainnet.

## 📚 Documents

#### Table of Contents
- [Introduction](./docs/INTRODUCTION.md)
- [Tutorial](./docs/TUTORIAL.md)

## 📝 Trinity in Web3.0
Trinity plays an connecting and entry layer in Web3.0 services. It connects with Trinity wallet, state channels and decentralized resources.

![web3](./assets/web3.png)

# Introduction

## Install Trinity

#### Clone source code
```
git clone https://github.com/trinity-project/trinity.git
cd trinity
```

#### Using python 3.6+ 
```
// find path for python 3.6+ path
which python3

// using python for the virtual environment
virtualenv -p /Library/Frameworks/Python.framework/Versions/3.6/bin/python3 venv
```

#### Install dependency
```
pip install -r requirements
```

![install](./assets/install.png)

#### Setting config
```
vi gateway/config.py
```

![config](./assets/config.png)

#### Start Trinity gateway

![gateway](./assets/gateway.png)

#### Create wallet
```
python3 prompt.py
```

![wallet](./assets/wallet.png)

#### Trinity commands
```
channel show uri
channel depoist_limit
```

![commands](./assets/commands.png)

## 🔗 Links
- [Official Website](https://trinity.tech/)

## 📣 Contributing
See [CONTRIBUTING.md](./CONTRIBUTING.md) for how to help out.

## 🗒 Licence
See [LICENSE](./LICENSE) for details.
