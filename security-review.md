# Security Review – Synth sETH Token

## 1️⃣ Contract Overview
- **Token Name:** Synth sETH
- **Symbol:** sETH
- **Network:** BNB Smart Chain
- **Standard:** ERC20, OpenZeppelin compliant
- **Total Supply:** 2,500,000,000 SETH
- **Decimals:** 18
- **Contract Type:** Standard ERC20 with burn capability
- **Owner-Controlled Functions:** Burn only (after deploy, mint is not available)

---

## 2️⃣ Key Functions
| Function | Visibility | Description |
|----------|------------|-------------|
| `balanceOf(address)` | public | Returns the token balance of an address |
| `transfer(address,uint256)` | public | Transfers tokens to another address |
| `approve(address,uint256)` | public | Allows spender to spend tokens on behalf of owner |
| `transferFrom(address,address,uint256)` | public | Transfers tokens on behalf of another address |
| `totalSupply()` | public | Returns total token supply |
| `burn(uint256)` | public | Burns tokens from sender’s balance |

> ✅ All functions are ERC20 compliant and follow OpenZeppelin standards. No mint function is available post-deploy.

---

## 3️⃣ Risk Assessment
- No external calls to unknown contracts.  
- Burn is irreversible but safe.  
- No hardcoded sensitive addresses.  
- No proxy or upgradeable pattern; contract is immutable.  
- Price display is external/test environment only (no oracle used).  

---

## 4️⃣ Limitations
- Burn reduces total supply permanently.  
- No mint function after deployment.  
- Price shown in dApp/test interface is only for testing purposes; no real impact on token economics.  

---

## 5️⃣ Testing & Verification
- All ERC20 functions tested on BSC Testnet.  
- Burn function tested successfully.  
- Transaction history visible on BscScan: [link to contract transactions]  
- Contract source verified and published on BscScan: [link to verified contract]  

---

## 6️⃣ References
- OpenZeppelin ERC20 Standard: https://docs.openzeppelin.com/contracts/4.x/erc20  
- BscScan Contract: [link to your contract]  
- Project GitHub repository: https://github.com/mehditk-hash/assets
