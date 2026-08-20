# Wallet Analysis

## Purpose

Wallet analysis examines observable blockchain activity at the address level to identify transaction patterns, relationships, and behaviors that may be relevant to risk assessment. The work emphasizes evidence-based analysis and avoids treating an address as a confirmed real-world identity without independent attribution evidence.

## Analytical Workflow

**Address/Entity Question → Transaction History → Counterparty Mapping → Behavioral Patterning → Risk Indicators → Attribution Assessment → Limitations**

### Core Questions

- What assets and networks are associated with the address?
- What are the major inbound and outbound counterparties?
- Is activity concentrated, dispersed, repetitive, or rapidly moving?
- Are there observable relationships among addresses?
- Does the address interact with exchanges, DEXs, bridges, mixers, protocols, or other risk-relevant infrastructure?
- What evidence supports attribution, and what remains uncertain?

## Attribution Methodology

Attribution should be treated as an evidence-ranking exercise rather than an assumption. Useful evidence can include publicly documented exchange addresses, protocol contracts, known service infrastructure, transaction patterns, and reputable third-party intelligence. Confidence should be stated explicitly.

### Attribution Levels

| Level | Meaning |
|---|---|
| Observed | Directly visible on-chain relationship |
| Supported | Multiple independent indicators support the relationship |
| Probable | Strong evidence exists but identity is not independently verified |
| Unconfirmed | Plausible hypothesis requiring additional evidence |

## AML / Risk Relevance

Wallet analysis can contribute to transaction monitoring and investigations by identifying concentration of activity, rapid movement, repeated counterparties, unusual routing, and exposure to known risk categories. These observations are investigative signals—not automatic determinations of illicit conduct.

## Privacy & Limitations

Research should use public blockchain data and avoid publishing unnecessary personal information. Wallet ownership may change, addresses may be controlled by custodians, and common infrastructure can create misleading apparent relationships.

## Planned Case Studies

- Bitcoin wallet behavior
- Ethereum address relationship analysis
- Cardano address/eUTXO behavior
- Exchange-related wallet patterns
- Multi-address behavioral clustering
