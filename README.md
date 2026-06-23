# Finances Without Borders (FWB)

Finances Without Borders (FWB) is a multi-chain fixed-yield deposit protocol deployed on Ethereum, Polygon, Arbitrum, Base, and BNB Smart Chain.

The protocol allows users to deposit supported assets for a fixed term and receive an on-chain position with a fixed APR selected at the moment of deposit.

## Official Links

* Website: https://finwb.xyz
* Documentation: https://finwb.xyz/docs
* X / Twitter: https://x.com/fwb030101
* Telegram: https://t.me/finance_without_borders
* Support email: fwb030101@gmail.com

## Deployed Contracts

| Network         | Contract                                     |
| --------------- | -------------------------------------------- |
| Ethereum        | `0x1Ef96B8fad9aE983E60610C4ba13536606B5c477` |
| Polygon         | `0xd17127796D46c1588550Df783FCfE3D08ef8F6c0` |
| Arbitrum        | `0xF5d84413f2cd33d6d473BA9D0c665a73472d8fC7` |
| Base            | `0x199180dfbACEE5c204Db4E803A92a9D3A9Db4d1F` |
| BNB Smart Chain | `0x18A021d1c89Af87AaeD266B2C58dD16855Ad3702` |

## Block Explorers

| Network         | Explorer                                                                   |
| --------------- | -------------------------------------------------------------------------- |
| Ethereum        | https://etherscan.io/address/0x1Ef96B8fad9aE983E60610C4ba13536606B5c477    |
| Polygon         | https://polygonscan.com/address/0xd17127796D46c1588550Df783FCfE3D08ef8F6c0 |
| Arbitrum        | https://arbiscan.io/address/0xF5d84413f2cd33d6d473BA9D0c665a73472d8fC7     |
| Base            | https://basescan.org/address/0x199180dfbACEE5c204Db4E803A92a9D3A9Db4d1F    |
| BNB Smart Chain | https://bscscan.com/address/0x18A021d1c89Af87AaeD266B2C58dD16855Ad3702     |

## Supported Networks

FWB is currently deployed on:

* Ethereum
* Polygon
* Arbitrum
* Base
* BNB Smart Chain

## Supported Assets

FWB currently supports three assets on each deployed network:

* USDT / USDT0
* WETH / ETH
* WBTC / BTCB / cbBTC

The exact token addresses are listed in `docs/supported-tokens.md`.

## TVL Methodology

FWB exposes an on-chain view function:

```solidity
getProtocolTvlTokensAndAmounts()
```

This function returns supported tokens and active principal amounts tracked by each deployed FWB contract.

The DeFiLlama adapter reads this function on each supported network and reports active user principal.

More details: `docs/tvl-methodology.md`

## Important Risk Note

FWB is a managed fixed-yield protocol. Deposited assets are transferred to protocol payout wallets, while the contracts keep on-chain accounting of user positions and active principal.

This repository documents the deployed contracts, supported networks, TVL methodology, and known trust assumptions.

More details: `docs/risk-disclosure.md`

## Repository Structure

```text
contracts/      Solidity contract source code
abi/            Contract ABI
deployments/    Deployment metadata by network
docs/           Protocol methodology and risk documentation
```

## License

Apache License 2.0. See `LICENSE`.

Smart contract source files may include their own SPDX license identifiers.
