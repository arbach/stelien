# Stellar Conditional Ownership and Rental Smart Contract

## Overview
This repository contains the implementation of a smart contract on the Stellar blockchain, designed to enable conditional ownership and rental agreements. With this contract, developers can build decentralized applications (DApps) for managing asset ownership and rental using the Stellar network.

## Features
Conditional Ownership: 
Establish conditional ownership rights by defining specific conditions that must be met for ownership to transfer from one party to another. Conditions can include time-based triggers, payment confirmations, or custom criteria.

## Rental Agreements: 
Create rental agreements with customizable terms and conditions, including rental duration, payment amounts, and late payment penalties. Rental transactions are executed automatically based on predefined conditions.

## Stellar Blockchain: 

Built on the Stellar blockchain, the contract offers fast, secure, and cost-effective transactions. Leveraging Stellar's smart contract capabilities ensures transparency, immutability, and decentralized execution of ownership and rental agreements.

# Getting Started
To use this smart contract, follow these steps:

Clone the Repository: Clone this repository to your local machine using the command 

`git clone https://github.com/arbach/stelien/`

Setup: 
https://plutus-3.gitbook.io/plutus-docs/basic-stellar-fundamentals/account-creation 

## Build and Deploy: 
Build and deploy the smart contract to the Stellar network using the Stellar SDK or compatible tools. Configure and set the necessary contract parameters as per your requirements.

### Build

`cargo build --target wasm32-unknown-unknown --release`

### Deploy
`soroban contract deploy \
      --wasm target/wasm32-unknown-unknown/release/setlien.wasm \
      --rpc-url https://rpc-futurenet.stellar.org:443 \
      --network-passphrase 'Test SDF Future Network ; October 2022'`

## Integrate with DApp: 
Integrate the deployed smart contract with your DApp to enable conditional ownership and rental functionality. Utilize the contract's methods and events to handle ownership transfers and rental agreement executions.

### 1. Rent:
This function allows a renter to rent an NFT token for a specific duration.

### 2. End Lease:
This function allows a leaser to delist their NFT token from leasing.

### 3. End Rent:
This function allows a renter to return their rented NFT token.

### 4. Claim Token:
This function allows a leaser to claim their NFT token that was rented and wasn't returned on time.


# Contributions

Contributions to this project are welcome. If you encounter issues or have ideas for improvements, open an issue or submit a pull request. Follow the code of conduct and provide detailed information to help us understand and address your concerns.

# License
This project is licensed under the MIT License. You are free to use, modify, and distribute the code for both commercial and non-commercial purposes.

# Disclaimer

This smart contract and associated code are provided as-is, without any warranty or guarantee of any kind. Use it at your own risk. The developers and contributors of this project shall not be liable for any damages or losses arising from the use or misuse of this code. It is recommended to thoroughly review and test the contract before deploying it to a production environment.
