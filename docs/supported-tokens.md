# Supported Tokens

FWB currently supports three assets on each deployed network.

The token list below is based on the deployed FWB contracts and the result returned by `getSupportedTokens()`.

## Ethereum

| Symbol | Token Address                                |
| ------ | -------------------------------------------- |
| USDT   | `0xdAC17F958D2ee523a2206206994597C13D831ec7` |
| WETH   | `0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2` |
| WBTC   | `0x2260FAC5E5542a773Aa44fBCfeDf7C193bc2C599` |

## Polygon

| Symbol | Token Address                                |
| ------ | -------------------------------------------- |
| USDT0  | `0xc2132D05D31c914a87C6611C10748AEb04B58e8F` |
| WETH   | `0x7ceB23fD6bC0adD59E62ac25578270cFf1b9f619` |
| WBTC   | `0x1BFD67037B42Cf73acF2047067bd4F2C47D9BfD6` |

## Arbitrum

| Symbol | Token Address                                |
| ------ | -------------------------------------------- |
| USD₮0  | `0xFd086bC7CD5C481DCC9C85ebE478A1C0b69FCbb9` |
| WETH   | `0x82aF49447D8a07e3bd95BD0d56f35241523fBab1` |
| WBTC   | `0x2f2a2543B76A4166549F7aaB2e75Bef0aefC5B0f` |

## Base

| Symbol | Token Address                                |
| ------ | -------------------------------------------- |
| USDT   | `0xfde4C96c8593536E31F229EA8f37b2ADa2699bb2` |
| WETH   | `0x4200000000000000000000000000000000000006` |
| cbBTC  | `0xcbB7C0000aB88B473b1f5aFd9ef808440eed33Bf` |

## BNB Smart Chain

| Symbol | Token Address                                |
| ------ | -------------------------------------------- |
| USDT   | `0x55d398326f99059fF775485246999027B3197955` |
| ETH    | `0x2170Ed0880ac9A755fd29B2688956BD959F933F8` |
| BTCB   | `0x7130d2A12B9BCbFAe4f2634d864A1Ee1Ce3Ead9c` |

## Notes

Token symbols may differ slightly between wallets, explorers, and data providers.

For TVL calculation, the DeFiLlama adapter uses token addresses and raw amounts returned directly by the deployed FWB contracts.
