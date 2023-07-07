# Creating a Token 
Creating our own token using solidity.

## Description
In this project, we create a smart contract using solidity to create a token of our own kind with the mint and burn function to understand the simple working of a token.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
The following is the code of the contract :-

contract MyToken {
    string public tokenName="Metacrafters";
    string public tokenAbbrv="META";
    uint public totalSupply= 0;
    mapping(address=>uint) public balances;
    function mint(address _address,uint value) public{
        totalSupply += value;
        balances[_address] += value;
    }
    function burn(address _address,uint value) public{
        if(balances[_address]>= value ){
            balances[_address] -= value;
            totalSupply -= value;
        }
    }
}

## Authors

Arshpreet Singh
@Arshpreet07

