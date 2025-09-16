---
title: Account
weight: 2
---

An account is an entity that is identified by a unique [address](/protocol/blockchain/address),
which can send transactions on the blockchain.

## Account Structure

The account structure is 12 bytes long and consists the following fields:

| Field   | Size    |
| ------- | ------- |
| Number  | 4 bytes |
| Balance | 8 bytes |

- **Number** is a sequential and unique number assigned to each account when it is created for the first time.
  The account number is used to calculate the [state hash](/protocol/blockchain/state-hash) of the blockchain.
- **Balance** holds the balance of the account, which is the amount of Pactus coins held by the account.

## Treasury Account

The Treasury account is a special account in the Pactus blockchain that holds the block reward coins.
The Treasury address is defined as: `000000000000000000000000000000000000000000` and its Number is set to `0`.
The [address type](/protocol/blockchain/address/#address-type) is 0, and therefore,
it doesn't have any key pair associated with it.

Every time a block is created, one coin from the Treasury account is distributed as a block reward.
