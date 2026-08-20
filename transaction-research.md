# Transaction Research

## Purpose

This section documents transaction-level blockchain research using publicly observable ledger data. The objective is to demonstrate how a transaction can be reconstructed, analyzed, documented, and evaluated for potential risk indicators without overstating what blockchain evidence can prove.

## Analytical Workflow

**Research Question → Data/Evidence → Reconstruction → Pattern Analysis → Risk Interpretation → Limitations → Sources**

### Evidence to Capture

- Transaction ID and network
- Block height and timestamp
- Inputs and outputs
- Amounts and transaction fee
- Address relationships
- Relevant prior/subsequent transactions
- Explorer/data source and retrieval date

## Case Study 01 — Bitcoin Transaction Reconstruction

### Research Question

What can be established from the public ledger about the structure and flow of a Bitcoin transaction, and which observations could be relevant to transaction-monitoring or AML-oriented analysis?

### Method

1. Identify the transaction hash and confirm the network.
2. Reconstruct inputs, outputs, values, and fee.
3. Examine UTXO relationships and address reuse where observable.
4. Review surrounding transactions for additional context.
5. Separate direct ledger evidence from analytical inference.
6. Document limitations before drawing conclusions.

### AML / Risk Relevance

Transaction-level analysis can support investigative workflows by identifying patterns that may warrant additional review, including unusual value movement, rapid movement through multiple addresses, or exposure to reliable external risk intelligence. A risk indicator is not equivalent to a finding of illicit activity.

### Limitations

- A blockchain address is not inherently a verified real-world identity.
- Exchange custody, batching, change addresses, and shared infrastructure can complicate interpretation.
- A single transaction rarely provides sufficient context for a compliance conclusion.
- External attribution and sanctions/risk datasets must be evaluated for source quality and date.

## Planned Case Studies

- Bitcoin UTXO transaction reconstruction
- Ethereum account-model transaction analysis
- Cardano eUTXO transaction analysis
- Cross-chain transaction-flow comparison
- Public-data exchange deposit/withdrawal pattern analysis

## Reproducibility Standard

Each completed case study should identify the transaction or dataset, source, retrieval date, analytical steps, calculations, findings, and limitations so another researcher can reproduce the analysis.
