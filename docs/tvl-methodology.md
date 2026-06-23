# TVL Methodology

FWB TVL is calculated from active user principal tracked on-chain by each deployed FWB contract.

Each FWB contract exposes the following view function:

```solidity
function getProtocolTvlTokensAndAmounts()
  external
  view
  returns (address[] memory tokens, uint256[] memory amounts);
```

The function returns:

* `tokens`: supported deposit tokens on the selected network;
* `amounts`: active principal amounts for each token.

## Supported Networks

The current TVL adapter reads FWB contracts on:

* Ethereum
* Polygon
* Arbitrum
* Base
* BNB Smart Chain

## What Is Included

The adapter includes active user principal tracked by the FWB contracts.

This means the reported value is based on active user deposit principal stored in contract accounting.

## What Is Not Included

The adapter does not include:

* withdrawn positions;
* inactive principal;
* future interest;
* untracked off-chain assets;
* protocol treasury assets that are not represented as active user principal;
* balances that are not linked to active user principal.

## Important Methodology Note

FWB is a managed fixed-yield protocol.

User deposits are transferred to protocol payout wallets after deposit. The FWB contracts keep on-chain accounting of user positions and active principal per supported token.

Therefore, the reported amount represents active user principal tracked on-chain, not necessarily the current token balance held directly inside the FWB contracts.

## DeFiLlama Adapter

The DeFiLlama adapter reads `getProtocolTvlTokensAndAmounts()` on each supported chain and reports the returned token amounts as active user principal.
