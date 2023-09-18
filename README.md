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
    <li><b>`priceInWei`</b> : The price of the item in Wei (a unit of Ethereum cryptocurrency)</li>
    <li><b>`paidWei`</b> :  The amount of Wei paid for the item.</li>
    <li><b>`index`</b> : A unique identifier for the item.</li>
    <li><b>`parentContract`</b> :  A reference to the `ItemManager` contract managing this item.</li>
  </ul>
</p>
<p>
  Functions
  <ul>
    <li><b>constructor :</b> Initializes the item with the provided values</li>
    <li><b>receive: </b>Allows users to make payments for the item and triggers the payment process.</li>
    <li><b>fallback : </b> An empty fallback function. </li>
  </ul>
</p>

