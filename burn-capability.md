# Synth sETH Token – Contract Information

Network: Ethereum Mainnet  
Standard: ERC20  
Decimals: 18  

## Burn Function
The token supports a standard ERC20 burn mechanism.

Token holders can permanently destroy their own tokens by calling the burn function, which reduces both their balance and the total supply.

### Implementation
```solidity
function burn(uint256 amount) public {
    _burn(msg.sender, amount);
}
