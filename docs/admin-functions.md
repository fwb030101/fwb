# Admin Functions

FWB contracts include owner-controlled administrative functions.

These functions are used to configure protocol parameters, supported assets, APR values, payout wallet settings, oracle settings, and withdrawal liquidity.

## Token Configuration

The contract owner can configure supported deposit assets.

Relevant functions:

```solidity
setSupportedToken(address token, bool supported)
setTokenDecimals(address token, uint8 decimals)
```

These functions define which tokens can be used for deposits and how token amounts are interpreted.

## Oracle Configuration

The contract owner can configure price feeds used by the protocol.

Relevant function:

```solidity
setPriceFeed(address token, address feed)
```

Price feeds are used for deposit value checks and protocol accounting.

## APR and Term Configuration

The contract owner can configure available deposit terms and APR values.

Relevant functions:

```solidity
setAllowedTerm(uint32 termDays, bool allowed)
setAprBps(address token, uint32 termDays, uint16 aprBps)
```

Rates can be updated for new deposits. Already opened positions keep the APR fixed at the moment of deposit.

## Payout Wallet

The contract owner can configure the payout wallet.

Relevant function:

```solidity
setPayoutWallet(address newPayoutWallet)
```

The payout wallet is used as the destination for deposited assets after deposit.

## Deposit and Oracle Limits

The contract owner can configure minimum deposit value and maximum price feed age.

Relevant functions:

```solidity
setMinDepositUsd18(uint256 newMinDepositUsd18)
setMaxPriceAge(uint256 newMaxPriceAge)
```

## Withdrawal Liquidity

Withdrawals are paid from liquidity available inside the FWB contract.

The owner can fund the contract with tokens for withdrawals.

Relevant function:

```solidity
adminFund(address token, uint256 amount)
```

If the contract does not have enough token balance for a withdrawal, the withdrawal may fail until sufficient liquidity is funded.

## Token Sweep

The contract includes an owner-controlled token sweep function.

Relevant function:

```solidity
adminSweep(address token, uint256 amount)
```

Users should review the verified source code on the relevant block explorer to understand the exact permissions and limitations.

## Trust Assumptions

FWB is a managed fixed-yield protocol.

The owner has administrative control over key protocol parameters. Users should understand these trust assumptions before depositing funds.
