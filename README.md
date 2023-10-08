# Supply Chain Management Smart Contracts

These Solidity smart contracts are designed to manage a supply chain, tracking the creation, payment, and delivery status of items in the supply chain. The contracts consist of two main components: `ItemManager` and `Item`.

## Contracts Overview

### ItemManager

- `ItemManager` is the main contract responsible for managing items in the supply chain.
- It is owned by the contract deployer (the owner).
- It defines different states (steps) an item can be in: Created, Paid, and Delivered.
- It allows the owner to create new items in the supply chain.
- It provides a function to trigger payment for an item when the required payment is made.
- It allows the owner to trigger the delivery of an item once it has been paid for.

### Item

- `Item` is a separate contract representing individual items in the supply chain.
- Each item has a unique address.
- It stores information about the item's price, the amount paid, and its index in the supply chain.
- It includes a `receive` function to accept payments and trigger payment confirmation.
- It can receive and handle Ether payments for the item.
- It interacts with its parent contract, `ItemManager`, to update the item's payment and delivery status.

## Getting Started

1. Deploy the `ItemManager` contract, which will serve as the main controller for the supply chain.

2. As the owner of the `ItemManager` contract, you can create new items in the supply chain using the `createItem` function. Provide an identifier and the price in Wei for each item.

3. Once an item is created, it starts in the "Created" state. Customers can then send payment to the corresponding `Item` contract address. When the payment amount matches the item's price, the item's state will change to "Paid."

4. As the owner, you can trigger the delivery of an item by calling the `triggerDelivery` function once the item is in the "Paid" state.

## Events

The contracts emit events to track the progress of items in the supply chain:

- `SupplyChainStep(uint _index, uint step, address _address)` is emitted when an item's state changes. It logs the item's index, the new state, and the item's address.

## Notes

- Ensure that you have sufficient Ether to make payments and trigger deliveries.
- Make sure to keep track of item indices to manage the supply chain effectively.

Feel free to customize and extend these contracts to meet your specific supply chain management needs.
