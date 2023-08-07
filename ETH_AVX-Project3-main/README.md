# HardHat Token Project

This project is a simple example of creating a custom ERC20 token on a local HardHat network. The smart contract allows the contract owner to mint new tokens, and any user can transfer and burn their tokens.

## Smart Contract (Token.sol)

The `Token.sol` file contains the implementation of the custom ERC20 token contract. The contract inherits from the OpenZeppelin `ERC20` contract, which provides the standard ERC20 token functionality.

### Functionality

- `constructor`: Initializes the token with the name "Brick" and the symbol "BRK".

- `mint`: The contract owner can use this function to mint new tokens and distribute them to any provided address.

- `burn`: Any user can burn their own tokens if they no longer need them.

- `transfer`: Allows users to transfer their tokens to another address.

## Deployment Script (deploy.js)

The `deploy.js` script is used to deploy the `Token.sol` smart contract to the local HardHat network. It uses HardHat's `ethers` library to interact with the blockchain.

## Package.json

The `package.json` file includes the list of dependencies used in this project. The required packages are as follows:

- `@ethersproject/abi`: Provides tools to work with Ethereum contract ABI (Application Binary Interface).
- `@ethersproject/providers`: Provides Ethereum JSON-RPC providers for different networks.
- `@nomicfoundation/hardhat-chai-matchers`: Chai matchers for HardHat to simplify writing tests.
- `@nomicfoundation/hardhat-network-helpers`: Helper functions for working with Ethereum networks in HardHat.
- `@nomiclabs/hardhat-ethers`: Integration between HardHat and ethers.js library.
- `@nomiclabs/hardhat-etherscan`: HardHat plugin for Etherscan verification.
- `chai`: An assertion library for tests.
- `ethers`: A library for interacting with Ethereum blockchain and smart contracts.
- `hardhat`: Development environment and task runner for Ethereum development.
- `hardhat-gas-reporter`: Gas usage reporter for HardHat tests.
- `solidity-coverage`: Code coverage tool for Solidity.

## How to Run the Project

1. Install the required dependencies:

```bash
npm install
```

2. Deploy the token contract to the local HardHat network:

```bash
npx hardhat node 
```
3. Connect the contract to remix ide by running this command in terminal
```bash
remixd -s ./ --remix-ide https://remix.ethereum.org
 ```

4. Interact with the token contract using Remix or compatible wallets.
a. Open remix IDE.
b. Switch to connect to localhost
c. Compile and Deploy the contract

## Additional Notes

- The contract owner is the one who initially deploys the contract and can mint new tokens.
- Any user can transfer their tokens to another address using the `transfer` function.
- Any user can burn their own tokens using the `burn` function.

Additionally, feel free to modify the `Token.sol` contract or add more functionalities as per your specific use case.
