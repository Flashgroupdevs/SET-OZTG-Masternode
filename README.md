# OZTG-masternopde

RUN YOUR OZTG MASTERNODE ON YOUR VPS

# OZEETY-masternode

Set up your OZTG Masternode on your VPS

##### connect to vps1 and vps2 (ubuntu 18.04) ssh root@ip (that you have created)

##### download ozeety-cli and ozeetyd (vps1 & vps2) HERE

https://github.com/Flashgroupdevs/New_Ozeety.wallet-ubuntu18.04/raw/master/ozeety-cli

https://github.com/Flashgroupdevs/New_Ozeety.wallet-ubuntu18.04/raw/master/ozeetyd

##### copy ozeety-cli and ozeetyd to /usr/bin (vps1 & vps2)



##### run ozeetyd (vps1 & vps2)

ozeetyd -daemon -deprecatedrpc=accounts

##### get account-address (vps1)

ozeety-cli getaccountaddress MN... 

##### send 10000 oztg (vps1)

##### get masternodekey (vps1)

> ozeety-cli createmasternodekey

(example) 3DHK81dxZXdbsnPtVVyS9kAeS7zj8XQpp3caPp8MkCNbgBdfSvU

##### get masternode outputs
> ozeety-cli getmasternodeoutputs
**Example**
[
  {
    "txhash": "31c96a231be6a4871540add1gfd3b1ebe351a0395d13e317ad8e0474e8df9e4",
    "outputidx": 1
  }
]

##### stop (vps1)

**ozeety-cli stop**

##### configure ozeety.conf (vps1)

- rpcuser=user5
- rpcpassword=pass5
- deprecatedrpc=accounts
- server=1
- daemon=1

##### configure masternode.conf (vps1)

**Example** MN1 178.45.243.107:37701 3DHK81dxZXdbsnPtVVyS9kAeS7zj8XQpp3caPp8MkCNbgBdfSvU 31c96a231be6a4871540add1c0d2bb2dbe351a0395d13e317ad8e0474e8df9e4 1

##### run ozeety (vps1)

**ozeetyd**

**stop (vps2)**

**ozeety-cli stop**

###### configure ozeety.conf (vps2)

-r pcuser=user6
- rpcpassword=choose your password
- deprecatedrpc=accounts
- server=1
- daemon=1
- listen=1
- masternode=1
- masternodeprivkey=  **Example** 345hgfdZXdbsnPtVVyS9kAeS7zj8XQpp3caPp8MkCNbgBdfSvU

###### run ozeety (vps2)

**ozeetyd**

**please wait confirm 20**

**start masternode (vps1)**

**ozeety-cli startmasternode "alias" "0" "MN1"**


Done enjoy !!!
