# Token Creation for ETH Proof Begineer Course

We are creating a smart contract with public variables for Token Name, Token Abbrv., and Total Supply, along with a mapping of addresses to balances. Then we are implementing  a mint function to increase total supply and address balances, and a burn function to decrease them, ensuring the address balance is sufficient before burning tokens.


## Description

First, the program has a contract with public variables storing the details about coins, which have variables such as Token Name and Token Abbrv. and Token Supply.

After that, we are mapping addresses to unsigned integers.

Then there are two functions mint and burn.

Mint Function :- Mint function has two parameters address and value . Mint function increases the total supply by the number and then it increases the sender's balance by a similar amount.

Burn Function :- Burn function is opposite to Mint function.It takes an address and value just like the mint functions. Burn function decreases the total supply by the number and then decreases the sender's ;  balance by a similar amount.
It should follow the condition that balance of sender should be greater than the amount that is burned.

As we see the complete functionality of the code depends on Mint and Burn function which are increasing and decreasing the total supply respectively.




## Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (example Token.sol). Copy and paste the  code into the file and then execute it.

```javascript
pragma solidity ^0.8.18;

contract MyToken {
  string public Token_Name="HEYA";
  string public Token_Abbrv="hyr";
  uint public Token_TotalSupply=0;

mapping (address => uint) public Balance;

function mint (address Addr,uint Val) public {
      Token_TotalSupply += Val;
      Balance[Addr] +=Val;
}

function burn (address Addr,uint Val) public {
     if(Balance[Addr]>=Val){
      Token_TotalSupply -= Val;
      Balance[Addr] -= Val;
     }
}
  
}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile Token.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Token" contract from the dropdown menu, and then click on the "Deploy" button.




## Authors
Mayank Sharma 

