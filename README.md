Schilling Coin (SCH) integration/staging repository
======================================


Quick installation of the Schilling Coin daemon under linux.

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://gitlab.com/schillingcoin/SCH.git
    cd SCH
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip schillingcoind
    sudo strip schillingcoin-cli
    sudo strip schillingcoin-tx
    cd ..

Running the daemon:

    schillingcoind 

Stopping the daemon:

    schillingcoin-cli stop

Demon status:

    schillingcoin-cli getinfo
    schillingcoin-cli mnsync status



### Coin Specs
<table>
<tr><td>Algo</td><td>Quark</td></tr>
<tr><td>Block Time</td><td>60 Seconds</td></tr>
<tr><td>Max Coin Supply</td><td>200.000.000 SCH</td></tr>
<tr><td>Premine</td><td>22.000.000 SCH</td></tr>
<tr><td>Maturity</td><td>50</td></tr>
<tr><td>Port</td><td>9070</td></tr>
<tr><td>RPCPort</td><td>9071</td></tr>
<tr><td>Reward pro block</td><td>32,3</td></tr>
<tr><td>Reward split</td><td>80%(MN) / 20%(POS)</td></tr>
</table>


### Masternode's collateral

<table>
<th>Block Height</th><th>Collateral</th>
<tr><td>0-260000</td><td>40.000 SCH</td></tr>
<tr><td>260000-520000</td><td>60.000 SCH</td></tr>
<tr><td>520000-780000</td><td>80.000 SCH</td></tr>
<tr><td>780000-1040000/td><td>90.000 SCH</td></tr>
<tr><td>1040000+</td><td>100.000 SCH</td></tr>
</table>


More information at [SchillingCoin.org](http://www.schillingcoin.org/)
---
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.