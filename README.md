# Zapster testnet Smart contracts
![image](https://res.cloudinary.com/dnsborxy7/image/upload/v1722431638/Zapster/oypi6zdoot2apv4m11ay.png)
This repository contains the smart contracts for the Zapster Protocol, designed to operate on the Binance Smart Chain Testnet.
## Features
- **ZapsterScore**: ZapsterScore is a smart contract designed to evaluate user activity and user score within the Zapster, based on various financial activity metrics.
- **LendingPool**: A lending pool is a contract which can be use to lend and borrow funds, tokenize debt and track interest earned or due.
- **PriceFeed**: Using Chainlink, Data Feeds provide data that is aggregated from many data sources by a decentralized set of independent node operators. The Decentralized Data Model describes this in detail. However, there are some exceptions where data for a feed can come only from a single data source or where data values are calculated.
- **Other**: You can see other Smart Contracts on `contracts` folder.
## Deployment
The contracts in this repository are currently deployed on the Binance Smart Chain Testnet using [Truffle](https://archive.trufflesuite.com/) tools, providing a demo testing environment for developers to interact with the Zapster Protocol without risking real assets.

**Mock Token**: Mock-token Address can be found [here](https://github.com/zapsterfinance/zapster-mock-token)
## Installation
To interact with these contracts locally, clone this repository and follow the setup instructions:

1. **Clone this Repository**: Clone this repo using `git`
```
git clone https://github.com/zapsterfinance/zapster-testnet-contracts.git
```
2. **Install Dependencies**: Install required packages using `npm`
``` npm install ``` or ``` npm i ```
3. **Setup .env file**: make manually `.env` or edit `.env.example` file and put your *Metamask MNEMONIC* to `"MNEMONIC"`, also copy your Etherscan API key and paste it to `"BSCSCAN"` for verifying your contracts address. *(optional)*
4. **Setup Truffle Config**: Edit `truffle-config.js` with your Config code, example:
```
module.exports = {
  networks: {
    development: {
      host: "127.0.0.1",
      port: 8545,
      network_id: "*" // Match any network id
    }
  },
  compilers: {
    solc: {
      version: "^0.8.0"
    }
  }
};
```
5. **Compile**: Run `npx truffle compile` or use `truffle compile` if using -global install to Compile your contract address.
6. **Migrate**: Migrate your contracts using
   ```
   npx truffle migrate --network=localhost
   ```
   or using this for mainnet or testnet    deployment
   ```
   npx truffle migrate --network=mainnet/testnet
   ```
7. **Testing contracts**: Run using
 ```
   npx truffle test --network=loc/main/test --compile-none
```
## Contributing
We welcome contributions to improve the functionality, security, and performance of the Zapster Finance. Please read our [Contributing Guide](https://github.com/ZapsterFinance/.github/blob/main/CONTRIBUTING.md) for more information.
## License
This project is licensed under the MIT License - [see the LICENSE file for details.](https://github.com/ZapsterFinance/.github/blob/main/LICENSE)

This description provides a clear and concise overview of the project, its features, deployment, and contribution guidelines, making it accessible for developers and users interested in the Zapster Finance.
