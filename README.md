// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
# Etherium Solidity

This Solidity program is a program that creates a token in which it has a mint and burn function. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Token 
**This solidity program for a smart contract that creates a new cryptocurrency token. 
The code has two functions: mint and burn.**

## Mint Function 
**An address and a value are both valid inputs for the mint function. 
The function then multiplies that figure by the total supply.
and multiplies it by the remainder of the sender address.**.

## Burn Function

**The burn function destroys tokens, making it the opposite of the mint function.
Similar to how the mint does it, it will accept an address and a value.**

## Starting the Program

## Executing Program 
To run this program, you can use Remix, an online Solidity IDE. make 
To get started, go to the Remix website at https://remix.ethereum.org/.
**Make sure your compiler is pragma solidity 0.8.18; to complike the Script.**

contract Tokens {

    // public variables here
string public tokenName = "Quilao";
string public tokenAbbrv = "NJQ";
uint public totalSupply = 0;
    // mapping variable here
 mapping(address =>uint) public balances;
    // mint function
function mint (address _address, uint _value) public {
    totalSupply += _value;
    balances [_address] += _value;
}
    // burn function
function burn (address _address, uint _value) public {
    if (balances[_address] >= _value) {
    totalSupply -= _value;
    balances [_address] -= _value;
    }
}

## Adding and Burning 

Make sure the burn method has conditionals when it comes to adding tokens and burning to ensure 
The sender's balance is larger than or equal to the amount intended for burning.

To Do the Adding and Burning on the Left side Navigation you will see a Deploy & Run Transactions Click it then 
You can add and burn items by clicking the Deploy & Run Transactions link in the left-side navigation. 
When you click the Deployed Contract below, you will see Burn, Mint, Balances, TokenAbbvr, TokenName, and Total Supply. You can add Token to your Total Supply by copying your Account Number, which is located underneath the Environment. To add tokens, paste the account number you copied earlier into your account, followed by the mint address. If you want to add a large number of tokens, try entering 5000. Click Transact when you see the check logo at the bottom of your compiler. Now click the Total Supply button. You will see your uint256 balances, which are the 5000 tokens you entered into your mint.

To Do the Burning just like what you did earlier Copy again your Account then paste it in the Burn Adress then it depends on you if how many tokens you want to burn  just like what i said earlier the **the burn function should have conditionals to make sure the balance of “sender” is greater than or equal to the amount that is supposed to be burned** 

That's all Thank you.
