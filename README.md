# NewToken Contract 

## Overview

The `NewToken` contract is a Solidity smart contract that implements a basic ERC20 token with additional functionalities. This contract allows for the creation, transfer, and burning of tokens, with specific access control mechanisms and features for the originator and founder.

## Features

1. **ERC20 Compliance**: The contract extends the ERC20 standard, providing basic token functionalities such as transferring, minting, and burning tokens.

2. **Access Control**: Two types of access control modifiers are implemented:
    - `onlyOriginator`: Restricts certain functions to be called only by the originator.
    - `onlyFounder`: Restricts certain functions to be called only by the founder.

3. **Token Initialization**: Tokens can only be initialized once by calling the `initializeToken` function. After initialization, token transfer functionality becomes enabled.

4. **Minting and Burning**: The contract allows the minting of tokens by the originator and burning of tokens by any token holder.

5. **Transfer Control**: Functionality to transfer tokens between addresses is provided through the `TransferTokens` function.

6. **Disable Amount Transfer**: The originator has the ability to disable token transfers by calling the `disableAmountTransfer` function.

## Installation and Usage

To deploy and interact with the `NewToken` contract:

1. **Deployment**: Deploy the contract to a supported blockchain network such as Ethereum.

2. **Initialization**: After deployment, the originator should call the `initializeToken` function to initialize the token. This function can only be called once.

3. **Token Management**: Once initialized, the contract allows for token minting, burning, and transfer functionalities as described above.

4. **Access Control**: Ensure that only authorized parties (originator or founder) are calling the functions restricted by access control modifiers.

## Example Usage

Here's a basic example of how to use the `NewToken` contract:

```solidity
// Deploy the contract
NewToken token = new NewToken();

// Initialize the token
token.initializeToken();

// Mint tokens to an address
token.MintTokens(address recipient, uint256 sendSum);

// Burn tokens
token.BurnTokens(uint256 burnedSum);

// Transfer tokens to another address
token.TransferTokens(address recipient, uint256 transferredSum);

// Disable token transfers
token.disableAmountTransfer();
```

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

## Author 

Chethan Kumar L J 
