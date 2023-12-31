# Solidity Vault with ERC20 Token

This repository contains two Solidity smart contracts: `Vault.sol` and `ERC20.sol`. 

## Vault.sol

The `Vault.sol` contract implements a simple vault to deposit and withdraw ERC20 tokens. It interacts with an ERC20 token contract via an interface.

### Functions

- `deposit(uint _amount) external`: Deposits a specified amount of the ERC20 token into the vault, minting corresponding shares to the depositor.
- `withdraw(uint _shares) external`: Withdraws a specified amount of shares, burning them and returning the corresponding ERC20 tokens.

### Usage

1. Deploy an ERC20 token contract (You can use the `ERC20.sol` provided in this repository or any other ERC20 token).
2. Deploy the `Vault.sol` contract, passing the address of the deployed ERC20 token as a constructor argument.

The `ERC20.sol` contract is a basic implementation of an ERC20 token. It provides functionalities like transfer, approve, transferFrom, mint, and burn.

### Functions

- `transfer(address recipient, uint amount) external`: Transfers a specified amount of tokens from the sender to the recipient.
- `approve(address spender, uint amount) external`: Allows `spender` to spend `amount` tokens on behalf of the sender.
- `transferFrom(address sender, address recipient, uint amount) external`: Transfers tokens from `sender` to `recipient` if the caller has been approved by `sender`.
- `mint(uint amount) external`: Mints a specified amount of tokens and assigns them to the sender.
- `burn(uint amount) external`: Burns a specified amount of tokens from the sender's balance.
