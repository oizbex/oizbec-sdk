# oizbec-sdk
## 🔹 Security Comparison: Ethereum vs P-256 Wallet

| Feature                  | Ethereum Wallet (secp256k1)               | Your Chain Wallet (P-256)                 |
|--------------------------|-------------------------------------------|------------------------------------------|
| **Elliptic Curve**       | secp256k1                                  | P-256 / secp256r1                        |
| **Key Size**             | 256-bit                                    | 256-bit                                   |
| **Key Generation**       | Fast, optimized for blockchain            | Strong, NIST-approved, slightly slower   |
| **Address Generation**   | Keccak256(pubKey), last 20 bytes (`0x`)  | Keccak256(pubKey), last 20 bytes (`0x`) |
| **Private Key Encryption**| AES-128-GCM / AES-256-CBC                 | AES-256-GCM                               |
| **KDF (Password-based)** | scrypt (N=262144, r=8, p=1)               | scrypt (N=262144, r=8, p=1)             |
| **MAC / Integrity**      | Keccak256(derivedKey + ciphertext)        | Keccak256(derivedKey + ciphertext)       |
| **Signing Speed**        | Faster                                     | Slightly slower                           |
| **Verification Speed**   | Faster                                     | Slightly slower                           |
| **Ecosystem / Support**  | Extensive wallets, tools, DApps, libraries| Custom chain, integration required        |
| **Security Level**       | Very high, battle-tested                   | Very high, equivalent to Ethereum        |

**✅ Notes:**  
- Both wallets are cryptographically strong.  
- Encryption + KDF in your chain is at least as secure as Ethereum.  
- Main difference: curve choice & ecosystem maturity, not raw security.
