# Case Study 01 — Bitcoin Transaction Reconstruction

## Research Question

What can be established from the public Bitcoin ledger about the structure, value flow, and historical context of transaction `f4184fc596403b9d638783cf57adfe4c75c605f6356fbc91338530e9831e9e16`, and what lessons does the transaction provide for blockchain analytics and AML-oriented investigation?

## Scope

- **Network:** Bitcoin mainnet
- **Transaction:** `f4184fc596403b9d638783cf57adfe4c75c605f6356fbc91338530e9831e9e16`
- **Block:** 170
- **Transaction type:** Legacy P2PK
- **Observed input count:** 1
- **Observed output count:** 2
- **Input value:** 50.00000000 BTC
- **Output value:** 50.00000000 BTC
- **Transaction fee:** 0 BTC
- **Transaction size:** 275 bytes / 275 vbytes
- **Locktime:** 0
- **Retrieval date:** 2026-08-20

## Data Sources

Primary explorer reference:

- Mempool.space transaction page: https://mempool.space/tx/f4184fc596403b9d638783cf57adfe4c75c605f6356fbc91338530e9831e9e16

Cross-check:

- Learn Me a Bitcoin transaction page: https://learnmeabitcoin.com/explorer/tx/f4184fc596403b9d638783cf57adfe4c75c605f6356fbc91338530e9831e9e16
- Bitcoin developer transaction documentation: https://developer.bitcoin.org/devguide/transactions.html

## Transaction Reconstruction

### Input

The transaction contains one input spending output 0 of the previous transaction:

`0437cd7f8525ceed2324359c2d0ba26006d92d856a9c20fa0241106ee5a597c9:0`

The input value is **50 BTC**, represented as **5,000,000,000 satoshis**.

The previous transaction is associated with an early Bitcoin block and provides the UTXO consumed by this transaction. This demonstrates the core UTXO relationship:

**previous TXID + vout → specific UTXO → new transaction input**

### Outputs

| Output | Value | Script Type | Analytical Observation |
|---|---:|---|---|
| 0 | 10.00000000 BTC | P2PK | 10 BTC transferred to the public key beginning `04ae1a62...` |
| 1 | 40.00000000 BTC | P2PK | 40 BTC transferred to the public key beginning `0411db93...` |

The two outputs total exactly 50 BTC. Therefore:

**50 BTC input − 50 BTC outputs = 0 BTC transaction fee.**

## Historical Context

This transaction is widely documented as the first Bitcoin transaction in which Satoshi Nakamoto sent 10 BTC to Hal Finney. The transaction was included in block 170 on January 12, 2009.

The historical attribution is supported by documented accounts and analysis of the early Bitcoin transaction graph. The blockchain itself, however, contains cryptographic keys and transaction relationships rather than names such as “Satoshi Nakamoto” or “Hal Finney.” The real-world attribution therefore depends on evidence outside the raw transaction data.

## Analytical Findings

### Finding 1 — The transaction has a simple one-input / two-output structure

The transaction consumes a single 50 BTC UTXO and creates two outputs of 10 BTC and 40 BTC. This is straightforward to reconstruct from the ledger.

### Finding 2 — The transaction has no fee

The input and output totals are equal. The observed miner fee is therefore 0 BTC. This reflects the conditions of the very early Bitcoin network and should not be treated as representative of modern Bitcoin fee behavior.

### Finding 3 — The transaction uses P2PK rather than modern address formats

Both outputs use Pay-to-Public-Key (P2PK) scripts. This is historically significant because early Bitcoin transactions often used public keys directly rather than the address/script patterns common in later periods.

### Finding 4 — The 40 BTC output may be interpreted as a change-like return, but ownership is not proven by the transaction alone

A common analytical interpretation is that the 10 BTC output represents the transfer and the 40 BTC output represents the remainder returned to the sender. That interpretation is consistent with the historical narrative, but the transaction structure alone does not cryptographically label either output as “payment” or “change.”

This distinction is important in blockchain investigations: **a plausible behavioral interpretation is not automatically a proven ownership relationship.**

### Finding 5 — Public-ledger transparency supports transaction reconstruction but not automatic identity attribution

The transaction makes the value flow, inputs, outputs, scripts, and transaction lineage observable. It does not independently establish the legal identity, intent, or beneficial ownership of the parties.

## AML / Transaction-Monitoring Relevance

Although this historical transaction is not an AML alert, it provides a useful training example for the mechanics of transaction-level investigation.

An analyst reviewing a modern transaction would use the same basic process:

1. Identify the TXID and confirm the network.
2. Reconstruct the input UTXOs.
3. Calculate input and output totals.
4. Calculate the transaction fee.
5. Identify output script/address types.
6. Trace relevant prior and subsequent transactions.
7. Examine counterparty and service exposure where reliable attribution data exists.
8. Separate directly observed evidence from analytical interpretation.
9. Record uncertainty and limitations.

Potential AML indicators in a modern case could include unusual transaction size, rapid movement through multiple addresses, repeated counterparties, structuring, exposure to known high-risk services, or behavior inconsistent with a customer's expected activity. **None of these indicators alone establishes illicit conduct.**

## Evidence vs. Inference

| Statement | Classification |
|---|---|
| One input spends a specific previous output | Observed on-chain evidence |
| Input value is 50 BTC | Observed on-chain evidence |
| Outputs are 10 BTC and 40 BTC | Observed on-chain evidence |
| Fee is 0 BTC | Calculated from observed values |
| Outputs use P2PK scripts | Observed on-chain evidence |
| 10 BTC was sent to Hal Finney | Historical attribution supported by external evidence |
| 40 BTC was “change” | Analytical interpretation consistent with context, not a protocol label |
| The transaction proves a person's identity | **Not established by the transaction alone** |

## Limitations

- Bitcoin addresses/public keys do not inherently contain verified real-world identities.
- Historical attribution requires evidence outside the raw transaction.
- A single transaction provides limited behavioral context.
- Change-output identification is heuristic unless supported by additional evidence.
- Early Bitcoin transactions used script conventions that differ from current wallet behavior.
- AML conclusions require broader customer, transaction, counterparty, and risk-context information.

## Reproducibility Notes

Another researcher should be able to reproduce the core analysis by entering the TXID into a Bitcoin explorer and verifying:

- block height
- timestamp
- input count and value
- previous outpoint
- output count and values
- script types
- transaction size/weight
- fee

The calculations in this case study require no private keys and use only publicly observable blockchain data.

## Conclusion

This transaction is a compact demonstration of why Bitcoin's UTXO model is useful for forensic and compliance-oriented analysis. The ledger allows an analyst to reconstruct exactly which previous output was spent, how much value entered the transaction, how that value was divided among outputs, and what fee was paid.

The more important analytical lesson is the boundary between **what the blockchain proves and what an analyst infers**. Strong blockchain intelligence requires both technical reconstruction and disciplined handling of attribution, intent, uncertainty, and evidence quality.

---

**Author:** Bonita Head  
**Portfolio:** Digital Asset Analysis | Blockchain Analytics | AML/KYC Risk Research | Cybersecurity
