# Project Title
This Solidity project called "Create A Token" 

## Description
In this project we will create a token in Solidity. The contract provides the two functionality of two main function mint and burn. This project provides the function of minting that takes two parameters an address and a value and burn function enable the burning tokens by a particular address and decreasing the value from total supply and address. It maintains the balances of different addresses using a mapping.

## Getting Started

### Installing
* You can install the Remix Desktop IDE by using this link : https://remix-project.org/

### Executing program

* To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract Mytoken {

    string public tokenName = "Meta";
    string public tokenAbbrv = "MTA";
    uint public totalSupply = 0;
    
    mapping (address => uint) public balances;

    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

     function burn (address _address, uint _value) public {
   if (balances[_address] >= _value)
     totalSupply -= _value;
     balances[_address] -= _value;
}

} 


```

## Authors

Contributors names and contact info

Jan Mel Semaña

https://twitter.com/Jan_Mel_Sem



## License

This project is licensed under the [NAME HERE] License - see the LICENSE.md file for details
