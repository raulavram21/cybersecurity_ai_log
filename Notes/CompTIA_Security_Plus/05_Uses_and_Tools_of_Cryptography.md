# Uses and Tools of Cryptography

## Overview

Cryptography does more than protect data in transit. It also proves where data came from, confirms it has not been altered, and relies on dedicated tools to manage the keys behind it.

## Code Signing

Code signing lets users verify that software came from the publisher and has not been changed since.

```mermaid
flowchart LR
    A[Original code] ==> B[Hash function] ==> C[Hash digest]
    C ==> D[Encrypt with private key] ==> E[Signature]
    E ==> F[Signed code]
```

| Step | What happens |
|---|---|
| **Hash** | A hash function creates a digest of the original code |
| **Sign** | The publisher encrypts the digest with its private key, along with a timestamp |
| **Attach** | The signature is attached to the code |
| **Verify** | The user decrypts the signature with the publisher's public key and compares the digests |

> **Analogy:** It is like a wax seal on a letter. Only the sender has the seal, and any change to the letter breaks the match.

> [!IMPORTANT]
> **Non-repudiation:** Because only the private key can produce the signature, the publisher cannot later deny having signed the code.

## Blockchain

A blockchain is a decentralized ledger. No single authority controls it, and each record links to the one before it.

> **Analogy:** Land registry records kept at county courthouses. Every transfer of a plot is recorded, so you can trace its full history back to the start.

| Feature | How it works |
|---|---|
| **Decentralized** | Every node holds a copy of the ledger |
| **Verification** | Nodes create hash digests of new transactions and compare them |
| **Consensus** | A transaction is accepted only when the nodes agree |
| **Tamper resistance** | Changing one record would require taking over most of the network |

## Cryptographic Tools

Cryptographic tools handle keys and cryptographic operations, so the main computer does not have to do all the work or hold every secret itself.

### Key Management

Key management covers the full life of a key, including generation, storage, and rotation. Rotating keys regularly limits the damage if one is compromised, just as with certificates.

> **Analogy:** Changing the locks on a building at regular intervals, so an old key stops working.

### Secure Enclave

A secure enclave is a protected area inside a device's processor that stores cryptographic material separately from the main operating system.

- Found in most modern mobile devices
- Often unlocked with biometrics, such as a fingerprint or face scan
- Keeps keys isolated, even if the main system is compromised

> **Analogy:** A safe inside a locked room. Even someone who gets into the room cannot open the safe without the right fingerprint.

### Trusted Platform Module (TPM)

A TPM is a chip either on the motherboard or soldered onto it. It stores cryptographic keys in memory and in read only storage.

> **Real world:** BitLocker on Windows uses a TPM to protect the key that encrypts the disk, so the drive cannot be read if it is moved to another machine.

### Hardware Security Module (HSM)

An HSM is a dedicated, tamper resistant device for generating, storing, and using keys. It offloads heavy cryptographic work from the main computer.

> **Analogy:** An HSM is a bank's vault for keys. The main computer asks it to perform operations, but the keys never leave the vault.

> [!IMPORTANT]
> **TPM vs HSM:** A TPM is a small chip built into one device, mainly protecting that device. An HSM is a larger, separate appliance that serves many systems and handles heavy cryptographic workloads.
