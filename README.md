# Post-Quantum Cryptography for Blockchain

**Connect the quantum threat model to the mechanics of a small lattice-based encryption example.**

This repository combines explanatory writing and hands-on notebooks about post-quantum cryptography in a blockchain context. Its practical core is a toy Learning With Errors (LWE) construction: generate keys, encrypt bits, decrypt them and apply the same process to a transaction-shaped message.

## Materials

| File | Purpose |
|---|---|
| [post_quantum_crypto_blockchain.ipynb](post_quantum_crypto_blockchain.ipynb) | Guided explanation and worked encryption examples |
| [pqc_blockchain_lab.ipynb](pqc_blockchain_lab.ipynb) | Exercise-oriented version with helper-function tasks and checks |
| [Lab instructions](pqc_blockchain_lab_instructions.pdf) | Companion worksheet |
| [article.md](article.md) | Longer explanatory article |
| [Publication draft](hackernoon_pqc_blockchain_publish.md) | Alternative article presentation |

## What to explore

- How a blockchain's cryptographic dependencies shape its quantum threat model.
- Modular matrix/vector arithmetic and small error terms in a toy LWE system.
- Public/secret key generation, bit encryption and decryption.
- Conversion of a transaction-like text message into encrypted bits and back.
- The difference between demonstrating an encryption primitive and designing a complete wallet or transaction-signature system.

The exercise notebook includes unfinished tasks; work through those cells in order rather than treating every cell as a finished library implementation.

## Open the lab

Use a Python Jupyter environment. The toy arithmetic uses standard Python modules; consult each notebook's setup cells for any plotting dependencies.

```bash
python -m pip install jupyterlab
python -m jupyter lab
```

Start with the explanatory notebook, then complete the corresponding helpers in the lab version. All examples operate locally; they do not require a wallet, blockchain transaction or real funds.

## Scope

The deliberately small parameters and educational randomness are unsuitable for protecting information. The code is not an implementation of a standardized post-quantum KEM or signature scheme, and encrypting a transaction message does not authenticate or submit it.

The articles contain time-dependent discussion of cryptographic standards. Check current primary standards before making an implementation choice; the executable toy example is intended to explain the underlying arithmetic.
