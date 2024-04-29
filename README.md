# Smart-Contract-Project

This program is for creating a smart contract project that implements the require(), assert() and revert() statements.

## Description

Avalanche is a blockchain platform that provides decentralized apps and blockchain networks. Avalanche is designed to address the scalability issues that have conventional blockchain systems. The platform offers exceptional transaction speed and finality in milliseconds because of the consensus protocol, Avalanche. The adaptable architecture of Avalanche complements this scalability by enabling developers to design customized blockchain networks, or subnets, that satisfy particular needs and use cases. 

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., project.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: GPL-3.0
pragma solidity 0.8.13;

    contract Smart_Contract_Project {
    address public Elissa;
    uint public amount;
    
    constructor() {
        Elissa = msg.sender;
        amount = 200;
    }

   
    function setAmount(uint _newAmount) public {
        require(msg.sender == Elissa, "Only the Owner can set the amount");
        amount = _newAmount;
    }

    
    function doubleAmount() public {
        uint newAmount = amount * 100;
        assert(newAmount >= amount); 
        amount = newAmount;
    }


    function withdraw(uint _amount) public {
        require(_amount <= address(this).balance, "Sorry, Insufficient Balance!");
        payable(msg.sender).transfer(_amount);
    }
}


To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.13" (or another compatible version), and then click on the "Compile + name of file(.sol)" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "project" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract has been deployed, you can interact with it through various functions such as require(), assert() and revert() statements.

## Authors

Contributors names and contact info

Elissa Mae Cruz


## License

This project is unlicensed.
