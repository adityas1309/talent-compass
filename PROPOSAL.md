# TalentCompass Proposal

## What the product is and who uses it
TalentCompass is a bias-aware, privacy-first recruitment and candidate screening layer. It is used by job applicants who wish to prove their qualifications, medical history, or employment eligibility without unnecessarily disclosing underlying sensitive personal information. It is also used by employers and institutions who need verifiable proofs of candidate qualifications while complying with strict data privacy regulations.

## Why Midnight specifically
Midnight provides a Zero-Knowledge selective disclosure framework that perfectly aligns with our privacy-first recruitment model. Unlike traditional blockchains where all data is public, or traditional databases where privacy can be breached, Midnight allows candidates to keep their records off-chain and prove specific facts (e.g., "Candidate has >5 years of experience" or "Candidate passed background check") via zero-knowledge proofs. This minimizes data liability for employers while empowering candidates.

## Data Model
- **Public State (On-Chain Anchor):** Contract state commitments, Merkle roots, and update counters stored immutably on the Midnight Preprod network. This includes ZK proof verification tokens allowing anyone to verify valid operations independently.
- **Private Witness (Off-Chain Data):** Full medical details, exact identity attributes, detailed financial amounts, and internal policy rules remain local on the user's client device.
- **Disclosure:** Candidates generate single-use ZK proofs (with nullifiers) that are submitted to the network. These proofs attest to specific attributes without revealing the payload data itself.

## Scope feasibility for Mainnet by Level 6
The scope is highly feasible for Mainnet by Level 6. The core circuit logic (verifying basic candidate criteria) and ledger state transitions (registering proofs) are implemented. The Preprod testnet integration proves the end-to-end viability. Moving forward, the final mainnet scope will strictly focus on candidate proof submission and employer verification—avoiding overly complex multi-party computation to remain within performance budgets.
