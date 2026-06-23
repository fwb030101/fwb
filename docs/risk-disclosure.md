# Risk Disclosure

FWB is a managed fixed-yield protocol.

Users deposit supported assets into FWB contracts and receive on-chain positions with fixed terms and APR values.

## Asset Flow

Deposited assets are transferred to protocol payout wallets after deposit.

This means that assets do not necessarily remain inside the FWB contract after deposit. The contract stores user positions and active principal accounting on-chain.

## Withdrawal Liquidity

Withdrawals are paid from liquidity available in the FWB contract.

The contract includes an administrative funding function that allows the owner to provide liquidity for withdrawals.

If the contract does not have enough token balance for a withdrawal, the withdrawal may fail until sufficient liquidity is funded back into the contract.

## Trust Assumptions

Users should understand that FWB is not a fully trustless autonomous vault where all deposited assets remain locked in strategy contracts.

The protocol uses on-chain accounting for user positions and active principal, while asset management may be performed through protocol-controlled payout wallets.

## Admin Controls

The contract owner can configure protocol parameters, supported tokens, APR values, price feeds, payout wallet settings, and withdrawal liquidity.

Users should review the verified source code on the relevant block explorer before depositing.

## General DeFi Risk

DeFi protocols may involve smart contract risk, oracle risk, liquidity risk, operational risk, and market risk.

Users should only deposit funds after understanding the protocol mechanics and trust assumptions.
