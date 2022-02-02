# Truffle Pet Shop Tutorial

```console
$ truffle compile
```

Use [Ganache] to run a local Ethereum blockchain (e.g. via Quickstart),
then migrate the contract by running

```console
$ truffle migrate
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

[Ganache]: https://trufflesuite.com/ganache