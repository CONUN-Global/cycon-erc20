# CYCON - ERC20 Token Smart Contract

This is smart contract source code deployed on the Klaytn network as CYCON Ttoken.
Here is token smart contract url: https://klaytnscope.com/account/0xe4a1bd45cddbbd5d9f605b08ed13a94b6b6ab5aa?tabId=txList

## Description

This smart contract provides an implementation of the ERC20 standard, widely used for creating and managing tokens on the EVM based blockchain. It includes the basic functionality necessary for a compliant ERC20 token, such as managing balances, transferring tokens, and handling allowances.

### Components

1. **Context:** An abstract contract providing information about the transaction context, particularly the sender. It's essential for handling meta-transactions.

2. **IERC20 Interface:** Defines the standard functions and events according to the ERC20 specification.

3. **IERC20Metadata Interface:** An extension of IERC20, including additional functions to retrieve token metadata like name, symbol, and decimals.

4. **ERC20 Contract:** The main contract implementing the ERC20 standard. It provides the functionality to transfer tokens, approve spending, and other typical ERC20 actions.

### Key Features

- **Flexible Token Creation:** Doesn't enforce a specific mechanism for token creation, allowing for a variety of supply mechanisms.
- **Standard Compliant:** Adheres to the ERC20 standard, ensuring compatibility with a wide range of services and wallets.
- **Safe Approve Mechanism:** Addresses potential issues in token allowances with functions like `increaseAllowance` and `decreaseAllowance`.
- **Event Emission:** Emits events on critical actions, facilitating tracking and transparency.

### Constructor Parameters

The ERC20 contract constructor requires two parameters:

- `name_`: The name of the token.
- `symbol_`: The symbol of the token, usually a shorter version of the name.

### Usage

1. **Deployment:** Deploy the contract on the Ethereum blockchain, providing the token's name and symbol.

2. **Token Management:** Use the functions provided to transfer tokens, approve allowances, and check balances.

3. **Events:** Listen to the `Transfer` and `Approval` events for tracking token movements and changes in allowances.

### Functions Overview

- `name()`: Returns the token's name.
- `symbol()`: Returns the token's symbol.
- `decimals()`: Returns the number of decimals the token uses.
- `totalSupply()`: Returns the total token supply.
- `balanceOf(account)`: Returns the token balance of an account.
- `transfer(to, amount)`: Transfers tokens to a specified address.
- `allowance(owner, spender)`: Returns the remaining number of tokens that the spender can spend.
- `approve(spender, amount)`: Sets the amount of allowance the spender is allowed.
- `transferFrom(from, to, amount)`: Transfers tokens from one address to another using the allowance mechanism.
- `increaseAllowance(spender, addedValue)`: Increases the allowance for a spender.
- `decreaseAllowance(spender, subtractedValue)`: Decreases the allowance for a spender.
