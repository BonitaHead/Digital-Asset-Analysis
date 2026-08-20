# AML Transaction-Monitoring Alert — Synthetic Case Study

> **Synthetic case study:** This exercise uses fictional customer and transaction facts for portfolio demonstration. It does not describe a real customer or allege real-world misconduct.

## Research Question

How should an analyst document and assess a hypothetical digital-asset transaction-monitoring alert while separating observable facts from assumptions?

## Alert Scenario

A fictional customer profile indicates expected monthly digital-asset activity below USD 10,000. During a 72-hour period, the account receives several inbound transfers totaling approximately USD 42,000, routes value through multiple self-controlled wallets, and then sends funds to a newly observed external address.

The alert is generated because the activity is materially different from the expected customer profile and involves rapid movement across multiple addresses.

## Initial Observations

| Observation | Analytical significance |
|---|---|
| Activity materially exceeds expected profile | Potential behavioral anomaly |
| Multiple inbound transfers | Requires source-of-funds/context review |
| Rapid movement between wallets | May warrant transaction-flow analysis |
| Newly observed external address | Counterparty/attribution review may be appropriate |

## Investigation Plan

1. Confirm customer profile and expected activity.
2. Reconstruct the relevant transaction sequence.
3. Identify addresses controlled by the customer where evidence supports that conclusion.
4. Review counterparties and available external intelligence.
5. Compare timing, value, frequency, and routing against historical activity.
6. Determine whether a reasonable explanation is available from customer or business context.
7. Document unresolved questions and escalation rationale.

## Risk Assessment

The described activity contains **potential risk indicators**, particularly a material deviation from expected activity and rapid movement through multiple wallets. These facts alone do **not** establish money laundering, fraud, sanctions evasion, or criminal intent.

A defensible analyst conclusion would therefore be framed as: **the alert warrants additional review based on observed transaction behavior and deviation from the expected customer profile.**

## Evidence vs. Inference

**Observed:** transaction amounts, timestamps, addresses, and movement patterns available from the relevant records.

**Inference:** an address may be controlled by the same customer based on supporting behavioral or attribution evidence.

**Not established without additional evidence:** the customer's intent, ultimate beneficial owner of an external address, or illicit purpose of the transactions.

## Limitations

- The scenario is synthetic.
- No real customer information is used.
- No sanctions, law-enforcement, or proprietary exchange datasets are assumed.
- Real investigations require institution-specific procedures, applicable law, reliable data sources, and appropriate escalation processes.

## Portfolio Value

This exercise demonstrates a structured approach to digital-asset transaction monitoring: establish facts, identify risk indicators, investigate context, communicate uncertainty, and avoid unsupported conclusions.
