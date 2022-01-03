# Solidity Notes + Code

## get started

* install npm + node.js `npm install -g npm`
* `npm install -g truffle`
* `npm install ganache-cli@latest --global`

go to your project folder and run:
`truffle init`

you'll find various directories:
* `contracts`: where your .sol files are located - the contracts directory
* `migrations`: deploy your contracts
* `test`: to test the system

`truffle-config.js`: specity all versions and blockchain configuration

## run and connect to the blockchain
Open `ganache` and start it: it creates a fake blockchain on your machine.
Copy `host:port` from ganache and pase it into `truffle-config.js`

```
    development: {
    host: "127.0.0.1",     // Localhost (default: none)
    port: 7545,            // Standard Ethereum port (default: none)
    network_id: "*",       // Any network (default: none)
    },
```

## create + deploy + test a contract
* create a new contract file .sol as: `contracts/MyContract.sol`
* create a new migration file as: `migrations/2_deploy_contracts.js`
* run `truffle migrate`

## interact with the smart contract via truffle

```
truffle console
MyFirstContract.deployed().then(function(i) {contract=i;})
contract.address // call contract functions
```