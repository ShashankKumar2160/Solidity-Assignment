Overview
MyToken is a simple token implemented in Solidity. This contract allows minting and burning of tokens, tracking the total supply, and maintaining individual balances for each address.

Requirements
Public Variables:

Tname (Token Name): The name of the token.
Tabbrv (Token Abbreviation): The abbreviation of the token.
TotalSupply: The total supply of the token.
Mappings:

balances: A mapping of addresses to their respective token balances.
Functions:

mint(address _address, uint amount): Increases the total supply of tokens and the balance of the specified address.
burn(address from, uint amount): Decreases the total supply of tokens and the balance of the specified address, ensuring the address has enough balance to burn.
Contract Details
Variables
Tname: A string representing the token's name. Default value is "____Accounts Department____".
Tabbrv: A string representing the token's abbreviation. Default value is "AD(B3)".
TotalSupply: An unsigned integer representing the total supply of tokens.
balances: A mapping from addresses to unsigned integers representing each address's balance.
Functions
mint(address _address, uint amount)
This function mints new tokens.

Parameters:

_address: The address to receive the minted tokens.
amount: The number of tokens to mint.
Functionality:

Increases TotalSupply by the specified amount.
Increases the balance of _address by the specified amount.
burn(address from, uint amount)
This function burns existing tokens.

Parameters:

from: The address from which tokens will be burned.
amount: The number of tokens to burn.
Functionality:

Checks if from has at least amount tokens.
If the condition is met, decreases TotalSupply by the specified amount.
Decreases the balance of from by the specified amount.
