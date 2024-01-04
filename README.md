# degenToken 
## Overview

`degenToken` is a decentralized ERC-20 token smart contract written in Solidity. This contract extends the functionality of the standard ERC-20 token by incorporating features such as minting, burning, suit redemption, suit enhancement, and the ability to add new suits. The smart contract is designed to represent a unique digital asset with distinct "suits" that users can acquire, enhance, and trade.

## Table of Contents

- [Features](#features)
- [Token Details](#token-details)
- [Functions](#functions)
- [Usage](#usage)
- [Security Considerations](#security-considerations)
- [License](#license)

## Features

1. **ERC-20 Compliance:** Inherits from the OpenZeppelin ERC-20 implementation, providing standard token functionality.
2. **Ownable:** Implements the Ownable pattern to ensure that only the owner can perform certain administrative functions.
3. **Token Minting and Burning:** Allows the owner to mint new tokens and token holders to burn their tokens.
4. **Suit System:** Introduces a suit system where users can redeem and enhance different suits using the token.
5. **Suit Costs:** Each suit has an associated cost in the token required for redemption.
6. **Suit Enhancement:** Users can enhance their selected suit by burning additional tokens.
7. **Suit Addition:** Allows the owner to add new suits to the contract.

## Token Details

- **Name:** degenToken
- **Symbol:** DGN

## Functions

1. **`mintFunction(address to, uint256 weigh) external onlyOwner`**
   - Mints new tokens and assigns them to the specified address.

2. **`burnFunction(uint256 weigh) external`**
   - Burns a specified number of tokens, reducing the total supply.

3. **`redeemFunction(uint8 suitNumber) external`**
   - Allows users to redeem a specific suit by burning the required tokens.

4. **`transferFunction(address recipient, uint256 count) external`**
   - Transfers tokens from the sender to the specified recipient.

5. **`addSuit(uint8 suitNumber, uint256 suitCost) external onlyOwner`**
   - Adds a new suit to the contract with the specified suit number and cost.

6. **`enhanceSuit(uint8 suitNumber, uint256 enhancementCost) external`**
   - Enhances the user's selected suit by burning additional tokens.

## Usage

1. Deploy the `degenToken` contract to the Ethereum blockchain.
2. Mint initial tokens using the `mintFunction` function.
3. Users can redeem suits using the `redeemFunction` function, burning tokens to acquire suits.
4. Owners can add new suits using the `addSuit` function.
5. Users can enhance their selected suits with the `enhanceSuit` function.

## Author

Shashank S R

## License

This smart contract is licensed under the MIT License. See [LICENSE](./LICENSE) for more details.
