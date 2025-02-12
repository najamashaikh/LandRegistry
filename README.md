Land Registry Smart Contract

Overview
This Solidity smart contract enables decentralized land registration and ownership transfer on the Ethereum blockchain. It ensures secure and transparent land management by allowing users to register land, transfer ownership, and retrieve land details.

Features
Register Land: Users can register land with a unique ID, location, and area.
Transfer Ownership: Landowners can transfer ownership to another address.
Retrieve Land Details: Anyone can fetch land details using a unique ID.
Check Registration Status: Verify if a land parcel is registered.
Event Logging: Emits events for registration and ownership transfer for transparency.

Smart Contract
The contract is written in Solidity and follows the MIT License.

Prerequisites
Solidity ^0.8.0

Ethereum development environment (Remix, Hardhat, or Truffle)

Deployment
Compile the contract using Remix or Hardhat.
Deploy it to an Ethereum-compatible blockchain.
Interact using a web3 provider (e.g., Metamask, Hardhat, or Truffle).

Functions

function registerLand(uint256 _id, string memory _location, uint256 _area) public;
function transferOwnership(uint256 _id, address _newOwner) public;
function getLand(uint256 _id) public view returns (uint256, string memory, uint256, address, bool);
function isLandRegistered(uint256 _id) public view returns (bool);

Events

event LandRegistered(uint256 indexed landId, string location, uint256 area, address indexed owner);
event OwnershipTransferred(uint256 indexed landId, address indexed oldOwner, address indexed newOwner);

