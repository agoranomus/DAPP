DAPP - Decentralized Allspot Payment Platform

This repository contains a Solidity smart contract implementing a BEP-721 token for Allspot's decentralized application (DApp) on the Binance Smart Chain (BSC).
Overview
The Allspot Contract enables users to:

Sign a commission contract with Allspot
Mint a BEP-721 token representing their signed contract
Publish products on the Allspot platform

Key Features

BEP-721 token implementation
User contract signing with minimum ALT token balance requirement
Product publishing for users with signed contracts
Storage of user and product details on-chain

Contract Structure

AllspotContract: Main contract inheriting from ERC721 and implementing IBEP721
User: Struct storing user contract details
Product: Struct storing product information

Functions

signContract: Allows users to sign a contract and mint a BEP-721 token
publishProduct: Enables users with signed contracts to publish product details
safeMint: Mints new BEP-721 tokens (restricted to contract owner)
getUserDetails: Retrieves user contract information
getProductDetails: Fetches product information

Requirements

Solidity ^0.8.0
OpenZeppelin contracts library
BSC-compatible development environment (e.g., Truffle, Hardhat)

Deployment
To deploy this contract on the Binance Smart Chain:

Ensure your development environment is configured for BSC
Have sufficient BNB for gas fees in your deploying wallet
Set the address of the ALT token contract during deployment

Additional Components Needed
This contract covers on-chain functionality. To complete the DApp, you'll need to develop:

A front-end interface compatible with BSC wallets
Off-chain storage for media files and extensive product information
Integration with BSC wallet providers
A system to generate and store PDF contracts off-chain

Security Considerations

The contract uses OpenZeppelin's implementation of ERC721 for security
Only the contract owner can mint new tokens
Users must have a minimum ALT token balance to sign contracts

Testing
Thorough testing is recommended before mainnet deployment:

Test all functions with various inputs
Ensure proper access control
Verify token minting and transfer functionality
Test integration with ALT token contract

Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your proposed changes.
License
This project is licensed under the MIT License.
Disclaimer
This smart contract is provided as-is. Users and developers should perform their own security audits before using in a production environment.
