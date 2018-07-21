MicroBitcoin (MBC) is a decentralised currency involving Blockchain Technology.

MicroBitcoin development tree

MicroBitcoin is a PoW/PoS-based cryptocurrency based on Scrypt Alogrithm.


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

For any kind of installation issue email at : info@microbitcoin.co

Cheers...


Development process

Developers work in their own trees, then submit pull requests when they think their feature or bug fix is ready.

The patch will be accepted if there is broad consensus that it is a good thing. Developers should expect to rework and resubmit patches if they don't match the project's coding conventions (see coding.txt) or are controversial.

The master branch is regularly built and tested, but is not guaranteed to be completely stable. Tags are regularly created to indicate new stable release versions of MicroBitcoin.

Feature branches are created when there are major new features being worked on by several people.

From time to time a pull request will become outdated. If this occurs, and the pull is no longer automatically mergeable; a comment on the pull will be used to issue a warning of closure. The pull will be closed 15 days after the warning if action is not taken by the author. Pull requests closed in this manner will have their corresponding issue labeled 'stagnant'.

Issues with no commits will be given a similar warning, and closed after 15 days from their last activity. Issues closed in this manner will be labeled 'stale'.


