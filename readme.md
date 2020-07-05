Explorer u18

______1________________________________________________
sudo apt-get update -y

sudo apt-get upgrade -y

sudo apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils python3 libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-test-dev libboost-thread-dev libboost-all-dev libboost-program-options-dev -y

sudo apt-get install libminiupnpc-dev libzmq3-dev libprotobuf-dev protobuf-compiler unzip software-properties-common libkrb5-dev mongodb nodejs npm git nano screen -y

sudo add-apt-repository ppa:bitcoin/bitcoin -y

sudo apt-get update

sudo apt-get install libdb4.8-dev libdb4.8++-dev

______2________________________________________________

Run coin Daemon

rpcuser=passexamplecoin

rpcpassword=7vKuAvYWRXqr24EfCkdjz

rpcallowip=127.0.0.1

listen=1

server=1

txindex=1

daemon=1

______3________________________________________________

Open mongodb.
________________________________________________


mongo

use explorerdb

db.createUser( { user: "iquidus", pwd: "854uq3EhKVFC76f7DZIMszvHrOKytCnzGevSgtWv", roles: [ "readWrite" ] } )

Close mongodb.

exit

git clone https://github.com/allforminers/Explorer.git explorer

cd explorer && npm install --production

Create the settings file.

cp ./settings.json.template ./settings.json

Original settings.json.


![Explorer](https://i.imgur.com/Vc2bCZW.png)











