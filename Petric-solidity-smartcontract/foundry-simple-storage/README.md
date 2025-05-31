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



after the all install and check make folder 
- forge init --force  
  so make all the folders and file 
-after remove sample thing and add contract in src file after write this command 
-forge compile 
so made new folders out
-after command 
anvil 
so you can see sample wallets with keys
-aftter start anvil in oter terminal start the command this 
- forge create SimpleStorage --rpc-url http://127.0.0.1:8545 --interactive
- or like this in terminal 
-forge create SimpleStorage  --interactive 
-forge create SimpleStorage --rpc-url http://127.0.0.1:8545 --private-key 0x59c6995e998f97a5a0044966f0945389dc9e86dae88c7a8412f4603b6b78690d
-if you want to remove your key from history then write the -history -c


-after run script 
 forge script script/DeploySimpleStorage.s.sol
[⠊] Compiling...
[⠑] Compiling 16 files with Solc 0.8.19
[⠘] Solc 0.8.19 finished in 634.22ms
Compiler run successful!
Script ran successfully.
Gas used: 530599

== Return ==
0: contract SimpleStorage 0x7FA9385bE102ac3EAc297483Dd6233D62b3e1496

If you wish to simulate on-chain transactions pass a RPC URL.

-with anvil chain so running that chian in other terminal and write this command 
-forge script script/DeploySimpleStorage.s.sol --rpc-url 127.0.0.1:8545
-forge script script/DeploySimpleStorage.s.sol --rpc-url 127.0.0.1:8545 --broadcast --private-key 0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80

-cast to hex value to decimal value with this kind of command yu can put here gas and know how much decimal this amount you get in brodcast /run-latest.json folder  "gasUsed": "0x89603",
- cast --to-base 0x89603 dec 


-insted we put key on terminal we have to make.env file for that and in terminal write the command 
-source.env
-after you can write -echo $PRIVATE_KEY than you can see private key also

-for more security
-do this in your macbook terminal not in vscode also i can do with anvil key and insted cast you put any name of that also 
-cast  wallet import defaultKey --interactive
Enter private key:
Enter password: 
`defaultKey` keystore was saved successfully. Address: 0xf39fd6e51aad88f6f4ce6ab8827279cfffb92266
-after in your vscode terminal you write this command then you get 
-cast wallet list
defaultKey (Local)
-after this insted private key you can write this 
-forge script script/DeploySimpleStorage.s.sol --rpc-url 127.0.0.1:8545 --account defaultKey --sender 0xf39fd6e51aad88f6f4ce6ab8827279cfffb92266  --brodcast -vvvv
-after you find key then you get giant string 
ankitakapadiya@Ankitas-MacBook-Pro foundry-simple-storage % cast wallet list 
defaultKey (Local)
ankitakapadiya@Ankitas-MacBook-Pro foundry-simple-storage % cd
ankitakapadiya@Ankitas-MacBook-Pro ~ % cd .foundry/keystores 
ankitakapadiya@Ankitas-MacBook-Pro keystores % ls
defaultKey
ankitakapadiya@Ankitas-MacBook-Pro keystores % cat defaultKey 
{"crypto":{"cipher":"aes-128-ctr","cipherparams":{"iv":"ee4a7fe7444b0065fc6c824ee77b6893"},"ciphertext":"992f9d9e7d4aa83f91aafc649bfcf563448c01004c1d7ee887461efed365c770","kdf":"scrypt","kdfparams":{"dklen":32,"n":8192,"p":1,"r":8,"salt":"00644a12bbfa381d7d695be41a4022039f80e4dd6e0371a52da89fc11b22da58"},"mac":"d42f50d302cde146eff7e3e81cf720cc615c329fe19a9969fe2884d6cf9dc9ae"},"id":"b00303b5-d494-43a3-aee4-375fe56aa9a6","version":3}%   
ankitakapadiya@Ankitas-MacBook-Pro keystores % 




1151  npx zksync-cli dev config 
 1152  docker ps
 1153  open -a Docker
 1154  docker ps
 1155  npx zksync-cli dev start
 1158  docker ps
 1159  forge create src/SimpleStorage.sol:SimpleStorage --rpc-url http://127.0.0.1:8011 --private-key 0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80 --legacy --zksync
 
 