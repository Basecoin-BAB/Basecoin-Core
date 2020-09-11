# Basecoin-Core
⭐Basecoin is a decentralized token, intended for day-to-day adoption and usability and designed with independent development. Its main objective is to be an alternative means of payment in companies and businesses, physical and online. And also for payment of bank slips, recharge for cell phone, phone bills, and other types of services. One of Basecoin's peculiar characteristics is to provide convenience, reliability, speed, and security when making your transactions.

![Official Repository - PoS/MN](https://github.com/Basecoin-BAB/Basecoin-Core/blob/master/Sem%20Título-1.png)
# How to install and configure the BAB/BaseCoin Wallet
[![How to install and configure the BAB/BaseCoin Wallet](http://img.youtube.com/vi/-HglCvikwDw/0.jpg)](http://www.youtube.com/watch?v=-HglCvikwDw "How to install and configure the BAB/BaseCoin Wallet")

# Add Nodes
basecoin.conf
```
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
Prepare your VPS 
Install Ubuntu Server 18.04 on a VPS. 
Update your Ubuntu machine. 
```
sudo apt-get update
sudo apt-get upgrade
```
Install the necessary dependencies.
```
sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils python3 libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-test-dev libboost-thread-dev libboost -all-dev libboost-program-options-dev

sudo apt-get install libminiupnpc-dev libzmq3-dev libprotobuf-dev protobuf-compiler unzip software-properties-common
```
Install Berkeley DB. 
```
sudo add-apt-repository ppa: bitcoin / bitcoin
sudo apt-get update
sudo apt-get install libdb4.8-dev libdb4.8 ++ - dev
```
Download the daemon. 
```
wget "https://github.com/Basecoin-BAB/Basecoin-Core/releases/download/V1.0.0.0/basecoin-daemon-linux.tar.gz" -The basecoin-daemon-linux.tar.gz

wget "https://github.com/Basecoin-BAB/Basecoin-Core/releases/download/V1.0.0.0/basecoin-qt-linux.tar.gz" -The basecoin-qt-linux.tar.gz
```


Extract the tar files. 
```
tar -xzvf basecoin-daemon-linux.tar.gz
tar -xzvf basecoin-qt-linux.tar.gz
```
Install the daemon and tools.
```
sudo mv basecoin basecoin-cli basecoin-tx / usr / bin /
```
Create the configuration file. 
```
mkdir $ HOME / .basecoin
nano $ HOME / .basecoin / basecoin.conf
```
Paste the following lines into basecoin.conf. 
```
# ----
rpcuser = rpc_basecoin
rpcpassword = kuw05sqio7bcm8z96o7redv17xws1lw6xpd1qf33
rpcallowip = 127.0.0.1
# ----
listen = 1
server = 1
daemon = 1
maxconnections = 64
# ----
# masternode = 1
# masternodeprivkey =
externalip = REPLACE_WITH_EXTERNAL_IP_OF_VPS
# ----
```
Leave the "masternode" and "masternodeprivkey" fields commented out.

Replace the text "REPLACE_WITH_EXTERNAL_IP_OF_VPS" with your VPS external IP address.

EXAMPLE externalip = 136.144.171.201

Start your node with the following command.

basecoind

Wait until the daemon finishes downloading the blockchain.

Send warranty (5000 BAB)
Open your desktop wallet and wait for your wallet to download the blockchain.

Go to "Tools".

Click on "Debug console".

This is the console where you will run all commands.

Create a new masternode private key.

createmasternodekey
```
Sample output

7VatfYVk5fFMTymPDhgSURAESDACJhWpd89WHGohPj5
```
Show your warranty address.

getaccountaddress “MN1” (when placing it remove the quotes)
```
Sample output

B5XBXknpQnVEbYsiL8cBRfPv22cqcsCF7W
```
Transfer the required amount of coins (5000 BAB) to the "guarantee address" you created using the "getaccountaddress" MN1 "" command.

Wait until the transaction has the required 15 master code confirmations.

Go to "Tools".

Click on "Debug console".

Enter the following command.

getmasternodeoutputs
```
Sample output

[
{
"txhash":
"506a242ccbfd2555bcd9cff5f40417acc83ccfe0cf8808df9",
"outputidx": 1
}
]
```

Go to "Tools".

Click "Open masternode configuration file".

Modify the following line and paste it into the notepad.
```
MN1 136.144.171.201:21392 7VatfYVk5fFMTymPDhgSURAESDACJhWpd89WHGoh35d9fbLQPj5 506a242ccbfd2555bcd9cff5f4041752c911f39cb2905acc83ccdf0cf8808
```

Save the file and close the notepad.

Close your wallet.

Register your masternode
Place the masternode private key in your masternode's configuration file and uncomment the “masternode” and “masternodeprivkey” values.

Configuration example 
```
# ----
rpcuser = rpc_nioshares
rpcpassword = kuw05sqio7bcm8z96o7redv17xws1lw6xpd1qf33
rpcallowip = 127.0.0.1
# ----
listen = 1
server = 1
daemon = 1
maxconnections = 64
# ---- masternode = 1
masternodeprivkey = 7VatfYVk5fFMTymPDhgSURAESDACJhWpd89WHGoh3j5 externalip = 136.144.171.201
# ----
```
Restart your masternode using the following commands. 
```
basecoin-cli stop
basecoind
```
Now open your desktop wallet.

Go to settings ".

Click "Unlock wallet".

Enter your wallet password and unlock it.

Go to "Tools".

Click on "Debug console".

Start your masternode using the command
```
startmasternode alias false MN1
```
Your masternode is now registered and will appear in the masternode list.

You can check the status of your masternode using the "getmasternodestatus" command.

Basecoin-cli getmasternodestatus
```
Sample output 
{
"txhash":
"506a242ccbfd2555bcd9cff5f4041752c911f39cb2905acc83ccfe0cf8808df9",
"outputidx": 1,
"netaddr": "136.144.171.201:9999",
"addr": "TDC99hZmSmYEcBu4WcxA2TCT6KBqHB6Hos",
"status": 4,
"message": "Masternode successfully started"
```
# Licence
Basecoin is released under the terms of the MIT license. See COPYING for more information or see https://opensource.org/licenses/MIT.
