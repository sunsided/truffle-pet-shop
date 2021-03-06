# Truffle Pet Shop Tutorial

This simply follows the [Truffle Suite Pet Shop](https://trufflesuite.com/tutorial/index.html)
Tutorial for EVM smart contracts written in Solidity.

![Ganache: Adoption contract after two interactions](docs/ganache-adoption-contract.png)

Changes from the tutorial:

- The Solidity compiler was upgraded to 0.8.11 from the default ~0.5.0.
- Added a script to extract ABI and bytecode from truffle's build outputs.

## Interesting reads

- [Is it safe to commit truffle build files to Github (open source)?](https://ethereum.stackexchange.com/questions/66284/is-it-safe-to-commit-truffle-build-files-to-github-open-source)
- [Solidity and Truffle Continuous Integration Setup with GitHub Actions](https://limcheekin.medium.com/solidity-and-truffle-continuous-integration-setup-with-github-actions-221149eabcca)

## Compilation and testing

```console
# truffle compile
$ npm run build
```

To test, run

```console
# truffle test
$ npm run test
```

## Migration

Use [Ganache] to run a local Ethereum blockchain (e.g. via Quickstart),
then migrate the contract by running

```console
# truffle migrate
$ npm run deploy:migrate
```

This should output something like to following:

```
Compiling your contracts...
===========================
> Everything is up to date, there is nothing to compile.



Starting migrations...
======================
> Network name:    'development'
> Network id:      5777
> Block gas limit: 6721975 (0x6691b7)


1_initial_migration.js
======================

   Deploying 'Migrations'
   ----------------------
   > transaction hash:    0x72bbc2f3743bf77abcb2bc31e1b26810955d381196fc87961efb7074ebaee165
   > Blocks: 0            Seconds: 0
   > contract address:    0x45051ea120CfD610a3e36758EEA02E8B18216A0b
   > block number:        1
   > block timestamp:     1643840547
   > account:             0x335EB94319a2413e91F42028417e1e2C6401a747
   > balance:             99.99616114
   > gas used:            191943 (0x2edc7)
   > gas price:           20 gwei
   > value sent:          0 ETH
   > total cost:          0.00383886 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.00383886 ETH


2_deploy_contracts.js
=====================

   Deploying 'Adoption'
   --------------------
   > transaction hash:    0x30e064bff5c90c395e49c3c43283c42890d8506eaf0e6ca3ff0d63f35689c6f2
   > Blocks: 0            Seconds: 0
   > contract address:    0x4d4DD43500b5946FCd4E311B42a91156568c492D
   > block number:        3
   > block timestamp:     1643840547
   > account:             0x335EB94319a2413e91F42028417e1e2C6401a747
   > balance:             99.99123784
   > gas used:            203827 (0x31c33)
   > gas price:           20 gwei
   > value sent:          0 ETH
   > total cost:          0.00407654 ETH


   > Saving migration to chain.
   > Saving artifacts
   -------------------------------------
   > Total cost:          0.00407654 ETH


Summary
=======
> Total deployments:   2
> Final cost:          0.0079154 ETH
```

## Running the Website

To start the webserver, run

```console
$ npm run dev
```

This should automatically open a browser at [https://localhost:3000](https://localhost:3000). 
When visiting the page, you will be asked to connect your
Web3 wallet to the page. You can then interact with the contract.

Here's an example for an `Adoption` call transaction logged by Ganache. 

![Ganache: Adoption wallet transaction](docs/ganache-transaction.png)

## Setting up a Web3 wallet with Ganache

In order to use MetaMask, Brave Wallet or similar
with Ganache, switch to the Localhost environment.

Test wallets can be imported by inspecting the private key
within Ganache.

[Ganache]: https://trufflesuite.com/ganache