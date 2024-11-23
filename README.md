## Example commands

### Deploy contracts using `forge`

#### Deploy a contract using forge cli

```
forge create SimpleStorage --interactive
```

#### Simulate the deploy of a contract using a script

```
forge script script/DeploySimpleStorage.s.sol --rpc-url http://127.0.0.1:8545
```

#### Deploy a contract using script
```
forge script script/DeploySimpleStorage.s.sol --broadcast --rpc-url http://127.0.0.1:8545 --private-key 0xabcd1234
```

### Call contract methods using `cast`

#### Call a contract method, with param, that creates a tx
```
cast send 0xe7f1725E7734CE288F8367e1Bb143E90bb3F0512 "store(uint256)" 123
```

#### Call a contract method without param that dont creates a tx

```
cast call 0xe7f1725E7734CE288F8367e1Bb143E90bb3F0512 "retrieve()"
```

#### Convert to decimal a hex value returned from a function call
```
cast --to-base 0x000000000000000000000000000000000000000000000000000000000000007b dec
```


## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

-   **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
-   **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
-   **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
-   **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
