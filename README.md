# Creating a Blockchain using Proof of Authority


![alt text](https://github.com/dtcosta/Blockchain-Development/blob/main/screenshots/header.jpg)

For this project, I will take on the role of a new developer at a small bank. My mission will be to set up a testnet blockchain for our organization. To do this, I will create and submit four deliverables:

* Set up a custom testnet blockchain.

* Send a test transaction.

* Create a repository.

* Write instructions on how to use the chain for the rest of the team.

## Background

I have just landed a new job at ZBank, a small, innovative bank that is interested in exploring what
blockchain technology can do for them and their customers. My first project at the company is to set up a private testnet that the team of developers
can use to explore potentials for blockchain at ZBank. We have decided on setting up a testnet because there is no real money involved, which will give the team of developers the freedom to experiment and Testnets allow for offline development.

In order to set up a testnet, it is advised that you have a general knowledge of:

* Puppeth, to generate genesis block.
* Geth, a command-line tool, to create keys, initialize nodes, and connect the nodes together.
* The Clique Proof of Authority algorithm.

Tokens inherently have no value here, so we will provide pre-configured accounts and nodes for easy setup.

## Instructions

# Create Nodes 
1. Start by downloading Go Ethereum Tools from https://geth.ethereum.org/downloads/
2. Navigate to the folder Go Ethereum
3. With proof of authority verification we will need to create nodes first
4. ./geth account new --datadir node1
5. ./geth account new --datadir node2
    
![alt text](https://github.com/dtcosta/Blockchain-Development/blob/main/screenshots/1.png)

# Create Genesis Block
1. launch puppeth private network manager with command ./puppeth
2. name of the newtwork, for our project we selected bankingnet
3. create a genenis block using the following steps
4. launch puppeth private network manager with command ./puppeth
5. name of the newtwork, for our project we selected bankingnet
6. confure new genesis
7. create new genesis from scratch 
8. clique - proof of authority
9. 7 second blocks 
10. input adresses fron node1 and node2 into allowed seal accounts 
11. input addresses from node 1 and node2 into prefunded account
  
![alt text](https://github.com/dtcosta/Blockchain-Development/blob/main/screenshots/2.png)
 
12. precompile address will result in a new genesis block being configured, couple more steps 
13. manage existing gensis
14. export gensis configuration
15. default folder to save will result in a new native gensis chain bankingnet.json 
  

![alt text](https://github.com/dtcosta/Blockchain-Development/blob/main/screenshots/3.png)

# Iniate our nodes with json files
1. ./geth init bankingnet.json --datadir node1
2. ./geth init bankingnet.json --datadir node2
  
![alt text](https://github.com/dtcosta/Blockchain-Development/blob/main/screenshots/4.png)

# Mining time using the following commands 
1. ./geth --datadir node1 --unlock "sealer one address" --mine --rpc --allow-insecure-unlock
2. capture enode from Started P2P Networking line: enode://numbers and letters @127.0.0.1:30303
3. ./geth --datadir node2 --unlock "sealer two address" --mine --port 30304 --bootnodes "enode from last step" --ipcdisable --allow-insecure-unlock
4. capture enode from Started P2P Networking line: enode://numbers and letters @127.0.0.1:30303
5. Now the 2 nodes will start looking for peers & matching other peers, a successful minning will look like screenshot below:


![alt text](https://github.com/dtcosta/Blockchain-Development/blob/main/screenshots/5.png)

# Launch My Crypto for the remaining steps 
1. change netwrok to custom and fill in all fields
2. enter node name 
3. network name is bankingnet
4. currency is ethereum
5. chain ID is the network ID we selected
6. url is  "http://127.0.0.1:8545"
7. click save & use custom node
8. launch wallet via keystore file
9. transact 50 ETH from address for node1 to address for node2
10. Your're done when you to see the screen below
 

![alt text](https://github.com/dtcosta/Blockchain-Development/blob/main/screenshots/9.png)

# Congratulations!


