# BIOTS-hackaton
Collection of lectures material from BIOTS hackaton

## Smart contracts

### [Remix](http://remix.ethereum.org) 
Online IDE for writing Ethereum smart contracts.

You can write, compile, test, deploy on test nets and main net (interacting with [MetaMask](https://metamask.io/)) Solidity smart contracts.

### [Solidity documentation](https://solidity.readthedocs.io/en/develop/)
Documentation for solidity.

### [Etherisc](https://etherisc.com/)
Smart contract examples - implementation of a Token, and of a Token Staking system (used for insurance in this case).

[Token Payments](https://docs.google.com/document/d/1mRRQIuJlebQeAKBxjgtrQcqi39N9wCyDuU8neo-u31U/edit?usp=sharing)

[Token Staking](https://docs.google.com/document/d/1SY-3CJSdAlnXx_uLHzCpW_NOTYmBWYS2eIW3ST0Qu_A/edit?usp=sharing)

## Web development

### [Web3.js](http://web3js.readthedocs.io/en/1.0/index.html)
Ethereum javascript API.

Used by [MetaMask](https://metamask.io/) (try to open the web console in your browser: CTRL+SHIFT+K when you are logged in MetaMask. You will be able to access to the injected javascript object: web3, through which all the blockchain interaction is made.

For example, type: `web3` or `web3.eth.getAcccounts()`

With these and other similar commands you will be able to access the web3 object's properties and methods. (See the [documentation](http://web3js.readthedocs.io/en/1.0/index.html) for a full description of the available js properties).


### [Web3.py](https://web3py.readthedocs.io/en/stable/)
Ethereum python API.

### [Visual Studio Code](https://code.visualstudio.com/)
Free IDE, optimized for web applications. It supports syntax highlighting for Solidity, and has an integrated Solidity compiler (solc).

### [A minimal frontend dapp](https://github.com/validitylabs/EthDapp-Boilerplate)
A simple web application (that can be run as a static website). It has a simple form (in `index.html`) through which you can submit some text, that will be handled by a js script (`custom.js`, which uses jQuery) and will be written on the blockchain (on an Ethereum testnet. We don't want to spend real money for such a stupid task!) by using smart contract's functions (in `Hello.sol`) through the use of web3. Before running the application, be sure to compile and deploy the smart contract! (For example using remix and MetaMask for deploying on a testnet, and for retrieving the contract's address to be put in the js script).

## Decentralized data storage

### [IPFS](https://ipfs.io/)
IPFS is a decentralized data layer. Saving data on the blockchain is really expensive! A common workaround is to save contents in the decentralized IPFS storage system, and only write the contents' hashes on the Ethereum blockchain (for validation purposes). IPFS uses a content-address indexing, meaning that you access the files saved on IPFS directly by using their hashes as their address.

No free lunch, though! Unless you pay for your storage on ipfs, or you run your own ipfs node(s), you have no guarantee that your data will be kept somewhere forever. [Filecoin](https://filecoin.io/) is a cryptocurrency associated with ipfs, which is used to fuel incentives for keeping the contents up.

You can install ipfs cli and iteract with ipfs network.
For example, to save a file on ipfs:
```
ipfs init
ipfs add <FILE>
```
you will receive the hash (HASH) of your stored file. To access your file: go to gateway.ipfs.io/ipfs/HASH
Or, for example, using the cli:
```
ipfs cat <HASH>
```
To ensure that your contents stay up, you can run a deamon:
```
ipfs daemon
```
and anybody will be able to access your contents until your daemon is running.

### [Other solutions]
Other possible alternatives are:

[Storj](https://storj.io/)

[MaidSafe](https://maidsafe.net/)

[Sia](https://sia.tech/)

## Security
