# SupplyChainSolution

<h3>Overview</h3>
<p>
This repository contains Solidity smart contracts for implementing a blockchain-based supply chain system. The system is designed to manage items through different stages of the supply chain, including creation, payment, and delivery. Each item is represented by a unique contract, and the overall supply chain management is handled by the ItemManager contract.
</p>

<h3>Contracts</h3>
<h4>Item.sol</h4>
<p>
  This contract represents an individual item in the supply chain. It has the following state variables and functions:
  <ul>
    <li><span>`priceInWei`</span> : The price of the item in Wei (a unit of Ethereum cryptocurrency)</li>
    <li><span>`paidWei`</span> :  The amount of Wei paid for the item.</li>
    <li><span>`index`</span> : A unique identifier for the item.</li>
    <li><span>`parentContract`</span> :  A reference to the `ItemManager` contract managing this item.</li>
  </ul>
</p>
