MicroBitcoin (MBC) is a decentralised currency involving Blockchain Technology.


INFO
===========================

Coin Site : https://www.microbitcoinico.co

Block Explorer : https://blockexplorer.microbitcoin.co

Algorithm : Scrypt

Type : PoW/PoS

Coin name : MicroBitcoin

Coin abbreviation : MBC

Coin Supply : 25200000 MBC

Premine : 1260000 MBC

Address letter : M

RPC port : 33014

P2P port : 33013

PoS percentage : 10% per year

Block reward : 57 coins

Coinbase maturity : 20 blocks

Target spacing : 64 seconds

Target timespan : 1 block

Transaction confirmations : 6 blocks

Seednode 1 : 207.148.77.109

Seednode 2 : 207.148.77.122



Installation
===========================

The installation requires at least a VPS having 2 GB OF RAM, 2 CORE CPU AND 40GB HDD with UBUNTU 16.04 installed on it. 


Steps:

 
1) Update your Ubuntu 16.04 machine.

sudo apt-get update

sudo apt-get upgrade



2) Install the dependencies to compile from source code.

sudo apt-get install build-essential libssl-dev libdb++-dev git libssl1.0.0-dbg libdb-dev libboost-all-dev libminiupnpc-dev libevent-dev libcrypto++-dev libgmp3-dev 



3) Download source code from repository.

git clone https://github.com/microbitcoinco/MicroBitcoin.git



4) Go to the src directory of your coin.

cd MicroBitcoin/src



5)  Now Run the following commands

chmod +x leveldb/build_detect_platform



6) Execute the following command to compile the daemon.

make -f makefile.unix RELEASE=1


NOTE:

If you see any fatal error while compiling 

RUN : -

a. mkdir obj

b. mkdir -p obj/zerocoin

Again do step 6.


7) Run the Coin Server using ./microbitcoind command

You will see message to create username and password



8) Create a new configuration file.

sudo nano /root/.microbitcoin/microbitcoin.conf



9) Paste the following lines in microbitcoin.conf file and save it.

rpcuser=rpc_microbitcoin

rpcpassword=yourrandompassword

rpcallowip=127.0.0.1

listen=1

server=1

txindex=1

daemon=1



10) Run the Coin Server using ./microbitcoind command


List of API call list can be found here : https://en.bitcoin.it/wiki/Original_Bitcoin_client/API_calls_list

For any kind of installation issue email at : info@microbitcoin.org

Cheers...
