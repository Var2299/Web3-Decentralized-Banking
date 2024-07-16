## Web3 Decentralized Banking: DBank on IC Blockchain
**DBank** is a decentralized banking application built on the Internet Computer (IC) blockchain. It allows users to manage their finances through a web interface, enabling actions such as checking balances, topping up accounts, and withdrawing funds. The application also supports compounding interest, demonstrating its functionality as a DeFi app.


![a1](https://github.com/user-attachments/assets/a0799ebc-790a-44bc-93fd-2eaec2bf3663)
![1](https://github.com/user-attachments/assets/6f1479fa-17bb-4ab9-9f7b-1dfc316cda9d)



## Features and Functions

### Balance Inquiry
- **Function**: `checkBalance`
- **Purpose**: To allow users to check their current balance in the account.
- **Implementation**: This is a query function that returns the current balance stored in a stable variable `currentValue`.

### Top-Up Account
- **Function**: `topUp`
- **Purpose**: To enable users to add funds to their account.
- **Implementation**: This function accepts a float amount as input and increments the `currentValue` by this amount.

### Withdraw Funds
- **Function**: `withdraw`
- **Purpose**: To allow users to withdraw funds from their account.
- **Implementation**: This function accepts a float amount as input, checks if the resulting balance would be non-negative, and decrements the `currentValue` by this amount if the check passes. Otherwise, it logs an error.

### Compound Interest
- **Function**: `compound`
- **Purpose**: To apply compounding interest to the current balance based on the time elapsed since the last compounding.
- **Implementation**: This function calculates the time elapsed since the last update, applies a compounding formula to the `currentValue`, and updates the `startTime` to the current time.

## Technical Components

- DBank leverages the Internet Computer (IC) blockchain, which is built on distributed systems principles. The blockchain ensures that the application relies on a decentralized network of nodes for consensus, transaction validation, and data storage.

-  The project employs core networking principles essential to blockchain technology, including peer-to-peer communication, consensus protocols, and secure data transmission. The communication between nodes and the overall network setup are critical to the functioning of the application.

-  Developing DBank involves full-stack development, integrating both front-end and back-end technologies. The application interacts with the blockchain, handling complex transactions and maintaining a user-friendly interface. This demonstrates the ability to work on large-scale software systems.

-  Security is a fundamental aspect of blockchain applications. DBank ensures secure transactions, proper authentication, and robust error handling. These security measures are crucial for maintaining user trust and the integrity of the financial application.

## Web Interface
- **HTML/CSS/JS**: The front end is built using standard web technologies. The HTML form includes fields for entering amounts to top up or withdraw, and a button to finalize transactions.
- **Candid UI**: A visual interface for testing API endpoints provided by the Internet Computer.

## Backend (Motoko)
- **Actor Model**: The backend logic is written in Motoko, a programming language for the Internet Computer. The DBank actor handles the core functionalities like top-up, withdraw, and compound.
- **Stable Variables**: The `currentValue` and `startTime` are stored as stable variables, ensuring their values persist across upgrades.

## Integration with Internet Computer
- **Canister**: The project uses canisters (smart contracts on the Internet Computer) to handle the backend logic.
- **Agent and Actor**: The `@dfinity/agent` package is used to interact with the canisters. The `createActor` function initializes the actor with the appropriate canister ID and options.

## Example Usage
- **Check Balance**: A user can query their current balance using the `checkBalance` function.
- **Top-Up**: A user can add funds by entering an amount in the "Amount to Top Up" field and submitting the form. This triggers the `topUp` function.
- **Withdraw**: A user can withdraw funds by entering an amount in the "Amount to Withdraw" field and submitting the form. This triggers the `withdraw` function.
- **Compound Interest**: The `compound` function can be called to apply interest based on the time elapsed since the last compounding.

## User Interface
- **Current Balance Display**: Shows the user's current balance.
- **Top-Up and Withdraw Forms**: Input fields for entering amounts to top up or withdraw.
- **Transaction Button**: Submits the form to finalize the transaction.


