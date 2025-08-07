# OpenIAG-Core (Seed v1.0)
*Open, mayeutic-aligned general-AI seed* — licensed **AGPL-3.0**.

Reference implementation of a **Mayeutic, Open-Source, Loosely-Coupled General-AI** architecture.

---

## 1 · Quick start
git clone https://github.com/SomewhatFreeman/OpenIAG-Core.git
cd openiag-core
pip install -r requirements.txt
python src/main.py --question "Which local law would cut litter without harming small businesses?"

The script:
Loads Axioms v1.0.
Generates alternatives → parallel critics → synthesis.
Prints the best option and a ticket M,J,R,B.
Saves the full debate in logs/debate_<timestamp>.json and computes its SHA-256.

2. Seal the hash on Sepolia testnet
python tools/send_hash.py logs/debate_202508071530.json
Release	Axioms hash	Debate hash	Tx-ID

| Release | Axioms hash | Debate hash | Tx-ID |
| ------- | ----------- | ----------- | ----- |
| v1.0    | `0x…`       | `0x…`       | `0x…` |


3. Repository layout
axioms/     – canonical axioms text
paper/      – white-paper drafts
src/
 ├ agents.py      # Tesis, Explorer, Critics, DomainExpert, Synthesis
 ├ evaluator.py   # Moral-Justice-Risk-Benefit calc
 ├ hashing.py     # hash-and-seal helpers
 └ main.py        # Fast vs Deep router
logs/     – signed debates

4. Contributing
Open issues / PRs.
Bug-bounty: any exploit that violates A1–A5 earns a stablecoin reward.
Join the discussion: 
