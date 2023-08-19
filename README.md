# NFT Collection Deployment and Transfer to Polygon with Polygon Bridge and AI-Generated Images
Deploy an NFT collection on the Ethereum blockchain, map the collection to the Polygon network, for enhanced scalability and reduced gas fees, and transfer assets via the Polygon Bridge. Additionally, the project incorporates AI-generated images using DALL·E 2 or Midjourney.

## Prerequisites
Before you begin, ensure you have the following installed:
* Ethereum wallet (e.g., MetaMask)
* Node.js: https://nodejs.org/
* Git: https://git-scm.com/

## Project Setup
Install dependencies:
``` npm install ```

## Deploying NFT Collection
Steps to deploy your NFT collection on the Ethereum blockchain:

* Modify truffle-config.js to set your desired network configurations(rpc-mumbai and goerli network).
* Define your NFT contract using Solidity in the contracts directory.
* Compile and deploy the contract.
```
npx hardhat run scripts/deploy.js --network goerli
```
The contract address to which it is deployed will be shown in the terminal. Paste it in the required code snippets necessary.

## Integrating AI-Generated Images
Choose an AI image generation tool like DALL·E 2 or Midjourney.
Generate a set of images to be used as NFTs.
* Use the generated images to create metadata for your NFTs, including attributes and image URLs.
* Update the NFT contract with the metadata for each NFT.

## Mapping to Polygon
Follow these steps to map your NFT collection to the Polygon network:

* Deploy the Matic token on the Ethereum mainnet using the Matic PoS Bridge.
* Update your NFT contract to include the Matic token address and Polygon RPC endpoint.
* Test the contract on the Polygon Mumbai testnet.

To batch mint all NFTs, run:
```
npx haradhat run scripts/batchMint.js --network goerli
```
To get approval confirmation, deposit and check balance, run the file approvedDeposit.js using:
```
npx hardhat run scripts/approvedDeposit.js --network goerli
```

## Transferring via Polygon Bridge
To transfer NFTs between Ethereum and Polygon:
* Obtain test Goerli tokens on the Goerli faucet by mining.
* Use the Polygon Bridge to transfer Goerli tokens between Ethereum and Polygon.
* Update your NFT contract to enable smooth transfer of NFTs between networks.

## Result
You'll get the confirmative messages in the terminal at each stage, like confirmation of approval, Deposition and transfer, and the testnet balance can be displayed.
