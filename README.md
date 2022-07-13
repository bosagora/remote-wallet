# Remote Wallet

## Installation

This code contains the ability to access specific accounts remotely.  
This allows balance checks and transfers of specific accounts to be performed remotely.

### Download source code

```bash
git clone https://github.com/bosagora/remote-wallet.git
cd remote-wallet
```

### Install NodeJS modules

```bash
npm install
```

### Set environment variables.

```bash
cp env/.env.sample env/.env
```

### Modify a file `env/.env`

`ACCESS_SECRET` is the value that the client should present when requesting from the server.  
This is used to make it available only to authorized clients.  
`MANAGER_KEY` is the private key of the account to be accessed remotely.  
`Web3 Secret Storage` encrypts and stores the manager's private key.  
Sample `Web3 Secret Storage` are `./keystore/test_manager.key`.
Please refer to the following  
[https://github.com/ethereum/wiki/wiki/Web3-Secret-Storage-Definition](https://github.com/ethereum/wiki/wiki/Web3-Secret-Storage-Definition)  
[https://web3js.readthedocs.io/en/v1.2.11/web3-eth-accounts.html](https://web3js.readthedocs.io/en/v1.2.11/web3-eth-accounts.html)

### Run

In testnet

```bash
npm run tart:testnet
```

In mainnet

```bash
npm run start:mainnet
```

## Testing

```bash
npm run build
npm test
```

