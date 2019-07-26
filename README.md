# Supply chain & data auditing

This repository containts an Ethereum DApp that demonstrates a basic Supply Chain flow between Farmer, Distributor, Retailer and Consumer.

## User Interface

### Farmer

The app allows a **farmer** to:
1. Harvest/add new items to the system.
2. Process, pack and sale these goods.

![farmerApp](images/app_farmer.png)

### Distributor/Retailer/Customer

3. The **distributor** can buy and ship these items.
4. The **retailer** can mark items as received.
5. The **customer** can purchase them.

![distributorApp](images/app_distributor_retailer_consumer.png)

### Viewer

Search items by UPC:

![searchItems](images/app_search.png)

### Transaction History

A transaction history will be available to show the record of every transaction performed.

![history](images/ftc_transaction_history.png)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Please make sure you've already installed ganache-cli, Truffle and enabled MetaMask extension in your browser.

- ganache-cli: 6.4.4
- ganache-core: 2.5.6
- truffle: v4.1.14 (core: 4.1.14)
- Solidity: v0.4.24 (solc-js)
- Metamask: 6.7.3
- node: 8.9.4
- npm: 6.9.0
- lite-server: 2.4.0 
- web3: 6.9.0

Checking versions in your command line:
```
$ ganache-cli --version
Ganache CLI v6.4.4 (ganache-core: 2.5.6)

$ truffle version
Truffle v4.1.14 (core: 4.1.14)
Solidity v0.4.24 (solc-js)

$ npm version
npm: '6.9.0',
node: '8.9.4',

$ npm web3 --version
6.9.0

```

### Installing

A step by step series of examples that tell you have to get a development env running

Clone this repository:

```
git clone https://github.com/jgongil/nautilus.git
```

Change directory to ```project-6``` folder and install all requisite npm packages (as listed in ```package.json```):

```
cd project-6
npm install
```

Launch Ganache:

```
ganache-cli -m "spirit supply whale amount human item harsh scare congress discover talent hamster"
```

Your terminal should look something like this:

![truffle test](images/ganache-cli.png)

In a separate terminal window, Compile smart contracts:

```
truffle compile
```

Your terminal should look something like this:

![truffle test](images/truffle_compile.png)

This will create the smart contract artifacts in folder ```build\contracts```.

Migrate smart contracts to the locally running blockchain, ganache-cli:

```
truffle migrate
```

Your terminal should look something like this:

![truffle test](images/truffle_migrate.png)

Test smart contracts:

```
truffle test
```

All 11 tests should pass.

![truffle test](images/truffle_OwnTest.png)

In a separate terminal window, launch the DApp:

```
npm run dev
```
## Deployment in Rinkeby

The document below shows the transaction ID´s associated to every contract deployment along with the contract adress.

- [Deployment in Rinkeby](deployedRinkeby.txt)

- Main supply chain contract can be found in the Etherscan explorer for Rinkeby https://rinkeby.etherscan.io/address/0x077f338c32407528ed064fa30e905fe41e556f44#code



## Design & Architecture

[write-up-UML](write-up-UML/write-up-UML.md)


## Built With

* [Ethereum](https://www.ethereum.org/) - Ethereum is a decentralized platform that runs smart contracts
* [IPFS](https://ipfs.io/) - IPFS is the Distributed Web | A peer-to-peer hypermedia protocol
to make the web faster, safer, and more open. [**Currently not used!!**]
* [Truffle Framework](http://truffleframework.com/) - Truffle is the most popular development framework for Ethereum with a mission to make your life a whole lot easier.


## Authors

See also the list of [contributors](https://github.com/your/project/contributors.md) who participated in this project.

## Acknowledgments

* Solidity
* Ganache-cli
* Truffle
* IPFS
