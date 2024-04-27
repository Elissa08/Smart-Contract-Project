# Smart-Contract-Project

This program is for creating tokens that demonstrate the functionality of the Solidity programming language. The purpose of this program is to serve to create a contract and how execute the token by interacting, exchanging, destroying, and creating the token contract.

## Description

Solidity is an object-oriented programming language that operates smart contracts. These contracts oversee the conduct of Ethereum state accounts. The contract includes a feature that generates and terminates the token value of the contract. This software functions as an uncomplicated introduction to Solidity programming and can serve as a foundation for more intricate undertakings later on.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;


contract MyToken {

    // public variables here
    string public tokenName = "CRUZ TOKEN";
    string public tokenAbbrv = "CTK";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }
    // burn function
    function burn (address _address, uint _value) public {
        if(balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;
        }
    }
}

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract has been deployed, you can interact with it through various functions such as tokenName, tokenAbbrv, totalSupply, balances of the address, mint function for increasing the value, and burn function for decreasing the value of the totalSupply. Finally, execute the function of the total amount of tokens in the mint and burn function by clicking on the "transact" button.

## Authors

Contributors names and contact info

Elissa Mae Cruz


## License

This project is unlicensed.
