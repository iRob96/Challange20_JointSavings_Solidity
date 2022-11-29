# Challange20_JointSavings_Solidity


## Goal

Create a Solidity smart contract that accepts two user addresses.


## Overview of the project 

A fintech startup company has recently hired you. This company is disrupting the finance industry with its own cross-border, Ethereum-compatible blockchain that connects financial institutions. Currently, the team is building smart contracts to automate many of the institutions’ financial processes and features, such as hosting joint savings accounts.

Your smart contract will use ether management functions to implement a financial institution’s requirements for providing the features of the joint savings account. These features will consist of the ability to deposit and withdraw funds from the account.

## Task

Create a Joint Savings Account Contract in Solidity

Compile and Deploy Your Contract in the JavaScript VM

Interact with Your Deployed Smart Contract


## Breakdown

Open the Solidity file named joint_savings.sol in the Remix IDE.

Define a new contract named JointSavings.

Define Two variables of type address payable named accountOne and accountTwo

A variable of type address public named lastToWithdraw

Two variables of type uint public named lastWithdrawAmount and contractBalance

Define a function named withdraw that accepts two arguments: amount of type uint and recipient of type payable address. In this function, code the following:

Define a require statement that checks if recipient is equal to either accountOne or accountTwo. If it isn’t, the require statement returns the “You don't own this account!” text.

Define a require statement that checks if balance is sufficient for accomplishing the withdrawal operation. If there are insufficient funds, it returns the “Insufficient funds!” text.

Add an if statement to check if lastToWithdraw is not equal (!=) to recipient. If it’s not equal, set it to the current value of recipient.

Call the transfer function of the recipient, and pass it the amount to transfer as an argument.

Set lastWithdrawAmount equal to amount.

Set the contractBalance variable equal to the balance of the contract by using address(this).balance to reflect the new balance of the contract.

Define a public payable function named deposit. In this function, code the following:

Set the contractBalance variable equal to the balance of the contract by using address(this).balance.

Define a public function named setAccounts that takes two address payable arguments, named account1 and account2. In the body of the function, set the values of accountOne and accountTwo to account1 and account2, respectively.

Add a fallback function so that your contract can store ether that’s sent from outside the deposit function.


<img width="1440" alt="Screen Shot 2022-11-28 at 11 44 16 PM" src="https://user-images.githubusercontent.com/107821891/204447581-920abd7e-50b5-48a6-a6ce-62d69080a90e.png">
<img width="1440" alt="Screen Shot 2022-11-28 at 11 46 15 PM" src="https://user-images.githubusercontent.com/107821891/204447515-8f61fb62-24d7-43b7-9b35-5722383cd2e4.png">
<img width="1440" alt="Screen Shot 2022-11-28 at 11 47 02 PM" src="https://user-images.githubusercontent.com/107821891/204447521-3f314c80-9966-49d7-9db2-4fe4b3cfa75b.png">
<img width="1440" alt="Screen Shot 2022-11-28 at 11 47 24 PM" src="https://user-images.githubusercontent.com/107821891/204447539-8b1c8a4f-5f04-42c8-b356-a2ae66025571.png">
<img width="1440" alt="Screen Shot 2022-11-28 at 11 54 17 PM" src="https://user-images.githubusercontent.com/107821891/204448525-bbc10da0-dcaf-4ac7-9188-576e6aac5d45.png">
<img width="1440" alt="Screen Shot 2022-11-28 at 11 55 06 PM" src="https://user-images.githubusercontent.com/107821891/204448577-266ec979-7972-4a05-9ee4-29aeea7addc8.png">


