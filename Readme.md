# Crowdfunding Smart Contract
## Overview
This is a simple crowdfunding smart contract written in Solidity, designed to facilitate fundraising campaigns on the Ethereum blockchain. The contract allows contributors to send Ether and participate in the campaign, while the campaign manager can create spending requests that require approval from contributors.

## Smart Contract Details
### Contract Features
* Contributors Mapping: Keeps track of contributors and their contributions.
* Manager: The address of the campaign manager who has control over creating spending requests and finalizing the campaign.
* Minimum Contribution: Minimum amount required for a contribution (set to 100 wei by default).
* Deadline: The timestamp when the campaign will end.
* Target: The fundraising goal for the campaign.
* Raised: The total amount raised so far.
* Number of Contributors: Total number of contributors in the campaign.

### Request Struct
* Description: Description of the spending request.
* Recipient: Address to which the funds will be sent if the request is approved.
* Value: Amount of Ether to be sent in the spending request.
* Completed: Flag indicating whether the request has been completed.
* Number of Voters: Number of contributors who have voted for the request.
* Voters Mapping: Keeps track of contributors who have already voted for the request.

### Functions
* Constructor: Initializes the crowdfunding campaign with a target amount and a deadline.

* createRequest: Allows the manager to create a spending request.

* contribution: Enables contributors to send Ether to the campaign.

* getBalance: Retrieves the current balance of the contract.

* refund: Allows contributors to request a refund if the campaign deadline has passed and the target is not reached.

* voteRequest: Allows contributors to vote for a spending request.

* makePayment: Allows the manager to finalize a spending request and transfer funds if it has sufficient approval votes.

## Usage
Deploy the smart contract on the Ethereum blockchain.
Set the fundraising target and deadline during deployment.
Contributors can use the contribution function to contribute funds.
The manager can create spending requests using the createRequest function.
Contributors can vote for spending requests using the voteRequest function.
After the deadline, contributors can request a refund if the target is not reached.
The manager can use the makePayment function to finalize spending requests and transfer funds.

## License
This smart contract is open-source and licensed under GPL-3.0.
