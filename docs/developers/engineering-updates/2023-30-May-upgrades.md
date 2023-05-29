---
title: 2023-30-05 Smart contract upgrades
sidebar_position: 1
---

:::note

Smart contract upgrades are being deployed to:

- Linea devnet on May 30, 2023
- Linea testnet on June 6, 2023

This will cause some downtime. Continue reading to prepare your dapp for the new changes.

:::

## Context

As part of the Alpha testnet upgrade, we are deploying new smart contracts (verifier, rollup, messaging service and token bridge).

- There will be a new proxy/timelock setup, so the addresses will be different.
- Storage/data layouts and the contract code is completely different, so we cannot keep the old addresses, as an upgrade will corrupt data.
- The new contracts have the ability to Pause.
- In the future, we will be using an upgrade pattern that does not cause downtime.

## Order of operations

1. Before the upgrade, finish all bridging transactions, and no new bridging transactions will be initiated.
2. Stop the prover.
3. Upgrade the system.
4. Resume Layer 2.
5. Resume prover.
6. Resume bridging.

## Key differences

### ABI

**Old ABI**

```json
abi
```

**New ABI**

```json
abi
```

### Input data

**Old input data**

**New input data**

### Addresses

<table>
  <tbody>
    <tr>
      <th>Contract</th>
      <th>Old L1 Address</th>
      <th>New L1 Address</th>
      <th>Old L2 Address</th>
      <th>New L2 Address</th>
    </tr>
    <tr>
      <td>Rollup</td>
      <td>0x....</td>
      <td>0x...</td>
      <td>0x...</td>
      <td>0x...</td>
    </tr>
  </tbody>
</table>

## Action items
