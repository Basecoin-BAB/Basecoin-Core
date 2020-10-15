# Basecoin-Core
⭐Basecoin is a decentralized cryptocurrency, intended for day-to-day adoption and usability and designed with independent development. Its main objective is to be an alternative means of payment in companies and businesses, physical and online. And also for payment of bank slips, recharge for cell phone, phone bills, and other types of services. One of Basecoin's peculiar characteristics is to provide convenience, reliability, speed, and security when making your transactions.

![Official Repository - PoS/MN](https://github.com/Basecoin-BAB/Basecoin-Core/blob/master/Sem%20Título-1.png)
# How to install and configure the BAB/BaseCoin Wallet
[![How to install and configure the BAB/BaseCoin Wallet](http://img.youtube.com/vi/-HglCvikwDw/0.jpg)](http://www.youtube.com/watch?v=-HglCvikwDw "How to install and configure the BAB/BaseCoin Wallet")

# Add Nodes
```
# basecoin.conf
addnode = 72.19.15.173
addnode = 173.249.39.84
addnode = 173.249.34.236
addnode = 144.91.87.7
addnode = 136.144.171.201
addnode = 207.180.245.239
addnode = 5.189.162.110
addnode = 72.19.15.174
addnode = 187.14.249.145
addnode = 177.66.147.35
addnode = 144.91.75.15
addnode = 191.30.221.134
addnode = 86.57.193.186
addnode = 72.19.15.173
addnode = 72.19.15.95
addnode = 179.199.118.147
addnode = 45.169.28.19
addnode = 187.24.231.218
addnode = 73.60.248.106
addnode = 72.19.15.94
addnode = 170.254.144.247
whitelist = 173.249.39.84
whitelist = 173.249.34.236
whitelist = 144.91.87.7
```
# Staking
Enable
```
# basecoin.conf
staking=1
```
Disable
```
# basecoin.conf
staking=0
```

# Specifications
```
Name                   Basecoin
Ticker                 BAB
Algorithm              Quark
Type                   PoS/MN
Total Supply           21,000,000
Masternode Collateral  5,000 BAB
Stake Min Age          2 Hours
Blocks per Day         1440
Block Time             1 Minute
Port                   70916
Protocol               Zerocoin
```
# How to Create Your Basecoin Masternodes
Ubuntu Server 18.04 on a VPS. 
Desktop CONSOLE WALLET commands
1st - createmasternodekey
2nd - getmasternodeoutputs

VPS command line
```
wget https://raw.githubusercontent.com/ViniciusBitnoob/Bitnodes/master/MnBasecoin_Ubunto18.sh && bash MnBasecoin_Ubunto18.sh
```
Stop Masternode (VPS)
```
~ / bab /./ basecoin-cli stop
```
Start Masternode (VPS)
```
~ / bab /./ basecoind &
```
Verify Synchronization (VPS)
```
~ / bab /./ basecoin-cli mnsync status
```
Check Masternode Status (VPS)
```
~ / bab /./ basecoin-cli getmasternodestatus
```
Check blocks and network information. (VPS)
```
~ / bab /./ basecoin-cli getinfo
```
Consult disk memory. (VPS)
```
df -mh
```
Consult swap memory. (VPS)
```
free -mh
```
Consult Processor usage. (VPS)
```
htop
```
Start Masternode (DESKTOP)
```
startmasternode alias false mn1
```

# Licence
Basecoin is released under the terms of the MIT license. See COPYING for more information or see https://opensource.org/licenses/MIT.
