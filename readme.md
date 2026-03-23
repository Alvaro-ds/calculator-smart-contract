# Smart Contract Calculator

## Overview

This project implements a basic calculator smart contract in Solidity.
It demonstrates fundamental concepts of smart contract development, including state variables, modifiers, events, and internal function logic.

The contract allows performing arithmetic operations on-chain while showcasing how logic and state changes are handled in Solidity.


## How It Works

The contract provides several arithmetic operations:

* Addition of two numbers
* Subtraction using internal logic
* Multiplication affecting a stored state variable

Additionally, it includes validation mechanisms and event emission to track operations.


## Core Features

* Arithmetic operations implemented on-chain
* Use of modifiers for input validation
* Event emission for tracking function execution
* Separation of logic using internal functions
* State management through a persistent variable


## State Variables

* **resultado**: Stores a persistent value initialized to 10 and updated through multiplication functions.


## Functions

### addition(uint256 num1_, uint256 num2_)

Performs addition between two numbers.

* Returns the result
* Emits an `Addition` event


### substraction(uint256 num1_, uint256 num2_)

Performs subtraction using an internal function.

* Returns the result
* Emits a `Substraction` event


### substraction2(int256 num1_, int256 num2_)

Handles subtraction with signed integers.

* Pure function
* Demonstrates handling of negative values


### multiplier(uint256 num1_)

Multiplies the stored `resultado` by the input value.

* Updates contract state


### multiplier2(uint256 num1_)

Same as `multiplier`, but with validation.

* Uses a modifier to enforce a condition
* Only executes if input equals a specific value


## Modifiers

### checkNumber(uint256 num1_)

Ensures that the input meets a predefined condition before executing the function.

* Reverts if the condition is not satisfied


## Events

* **Addition** → emitted when an addition is performed
* **Substraction** → emitted when a subtraction is performed

These events allow tracking contract activity off-chain.


## Smart Contract Concepts Demonstrated

* State vs pure functions
* Internal function usage
* Modifiers for validation
* Event-driven architecture
* Basic arithmetic logic on-chain


## Tech Stack

* Solidity ^0.8.24
* Remix IDE


## Possible Improvements

* Add division with validation (avoid division by zero)
* Improve modifier logic for more realistic conditions
* Store operation history on-chain
* Add access control for specific operations


## Author

Developed as part of a hands-on blockchain learning process, focusing on understanding Solidity fundamentals and contract structure.


## License

LGPL-3.0-only