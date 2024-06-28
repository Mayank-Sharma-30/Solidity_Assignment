# Token Creation for ETH Proof Begineer Course

We are creating a smart contract with public variables for Token Name, Token Abbrv., and Total Supply, along with a mapping of addresses to balances. Then we are implementing  a mint function to increase total supply and address balances, and a burn function to decrease them, ensuring the address balance is sufficient before burning tokens.

## Description

First, the program has a contract with public variables storing the details about coins, which have variables such as Token Name and Token Abbrv. and Token Supply.

After that, we are mapping addresses to unsigned integers.

Then there are two functions mint and burn.
Mint function has two parameters address and value . Mint function increases the total supply by the number and then it increases the sender's balance by a similar amount.

Burn function is opposite to Mint function, Burn function decreases the total supply by the number and then decreases the sender's ;  balance by a similar amount.
It should follow the condition that balance of sender should be greater than the amount that is burned.



## Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension . Copy and paste the  code into the file and then execute it.


## Authors
Mayank Sharma 

