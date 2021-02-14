# 1. 下载polio
wget https://www.irif.fr/~jch/software/files/polipo/polipo-1.1.1.tar.gz
tar -xvf polipo-1.1.1.tar.gz

# 2. 编译安装
cd polipo-1.1.1  
make

# 3. 配置
mkdir -p /etc/polipo  
cp config.sample  /etc/polipo/config  

```bash
proxyAddress = "0.0.0.0"
proxyPort =  5993
daemonise = true
pidFile = /etc/polipo/pid
logFile = /etc/polipo/log
logLevel = 99
socksParentProxy = 127.0.0.1:10080
socksProxyType = socks5
proxyName = "polipo"
```

# 4. 启动
polipo  

```bash
export http_proxy=http://127.0.0.1:5993
export https_proxy=$http_proxy  
```

# 5. ssr客户端
git clone https://github.com/shadowsocks/shadowsocks.git  
git checkout master  
