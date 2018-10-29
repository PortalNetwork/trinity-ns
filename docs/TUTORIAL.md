# Tutorial

## Install

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

![install](../assets/install.png)

#### Setting config
```
vi gateway/config.py
```

![config](../assets/config.png)

#### Start Trinity gateway

![gateway](../assets/gateway.png)

#### Create wallet
```
python3 prompt.py
```

![wallet](../assets/wallet.png)

#### Trinity commands
```
channel show uri
channel depoist_limit
```

![commands](../assets/commands.png)
