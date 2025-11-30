# solidity_fullstack_kit (TODO)

Minimal Solidity smart contract patterns with TypeScript integration.

## Structure (TODO)

```
├── fundme/          # Crowdfunding pattern
│   └── FundMe.sol
├── token/           # ERC20 token
│   └── ERC20Token.sol
├── exchange/        # AMM swap (x*y=k)
│   └── SimpleSwap.sol
├── dao/             # Governance voting
│   └── SimpleDAO.sol
├── oracle/          # Price feed
│   └── PriceOracle.sol
└── app/             # TypeScript client
    └── src/index.ts
```

## Contracts (TODO)

| Contract | Description |
|----------|-------------|
| `FundMe` | Accept ETH donations, owner withdraws |
| `ERC20Token` | Standard ERC20 implementation |
| `SimpleSwap` | Constant product AMM (0.3% fee) |
| `SimpleDAO` | Proposal & voting system |
| `PriceOracle` | Price feed with staleness check |

## TypeScript App (TODO)

Uses [viem](https://viem.sh) - lightweight EVM client.

```bash
cd app
npm install
npm run build
```

```typescript (TO DO)
import { readContract, writeContract } from './index.js';

// Read contract state
const balance = await readContract(address, abi, 'balanceOf', [wallet]);

// Send transaction
const receipt = await writeContract(privateKey, address, abi, 'transfer', [to, amount]);
```

## Requirements

- Solidity ^0.8.24
- Node.js 18+
- TypeScript 5+
