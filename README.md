# Project Title
This Solidity project called "Create A Token"  its objective is to mint new tokens and burning new tokens. It keeps tracks different addresess using mapping.

## Description
This project is called "Create a token"  has an ability to mint new tokens and burn existing tokens. The contract provides the functionality of two main function mint and burn. This project provides of minting function that takes two parameters an address and a value and burn function enable the burning tokens by a particular address and decreasing the value from total supply and address. It maintains the balances of different addresses using a mapping.

## Getting Started

### Installing
* You can install the Remix Desktop IDE by using this link : https://remix-project.org/

### Executing program

* To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.
  
You can run this code by using Remix IDE that is provided in the link. To create a file you can click the "New File" save the file ".sol".
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
 Once your Remix IDE or Remix Website IDE you can copy and paste this code.
 To compile this code you can click the compiler and set it to "0.8.18" and click the "Compile.myToken.sol".
And then below it is the deploy and run transaction where you deploy the contract by clicking the button to execute. 

Finally, click the address in the account by clicking the clipboard, and paste it in the mint _address and set the value to 1000 tokens and check the totalSupply and paste the same address in the clipboard to balances. Then in the burn function when we will burn some tokens by 500 and check the totalSupply if it's been reduce by 500.

## Authors

Contributors names and contact info

Jan Mel Semaña

https://twitter.com/Jan_Mel_Sem



## License

This project is licensed under the MIT License - see the LICENSE.md file for details
