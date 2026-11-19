# Virtual Private Networks (VPNs)

## Overview

A VPN protects data in transit across an untrusted network, such as the public Internet. It creates an encrypted tunnel between two endpoints, so anyone intercepting the traffic on the way sees only ciphertext.

> **Analogy:** A sealed, armoured tunnel through a busy public street. Traffic on the street can see the tunnel, but not what is being carried through it.

## Types of VPN

| Type | Connects | Typical use |
|---|---|---|
| **Remote access VPN** | An individual device to a network | An employee working from home or travelling |
| **Site-to-site VPN** | One network to another network | Connecting a branch office to headquarters |

For a remote access VPN, the user authenticates as themselves to set up the link. In the diagram, a remote client connects over the Internet to a security gateway, which protects the internal hosts behind it.

> [!IMPORTANT]
> **Exam clue:** Remote access VPNs connect one user device. Site-to-site VPNs connect entire networks.

## Tunnelling

Tunnelling wraps the original data inside another packet, then encrypts it. This is what lets traffic cross an untrusted network securely.

> **Analogy:** Putting a letter inside a locked box, then placing that box inside a courier's van. The van's route is public, but the letter stays hidden.

## Protocols

| Protocol | Status | Key point |
|---|---|---|
| **SSL** | Retired | Found to be cryptographically broken, so it should no longer be used |
| **TLS** | Current | The successor to SSL, used for secure web and VPN connections |
| **IPsec** | Current | A suite of extensions that secures IP traffic |

> [!WARNING]
> **Exam clue:** SSL is no longer secure. TLS is its replacement, even though people still sometimes say "SSL VPN" for the same concept.

### IPsec and ESP

IPsec includes Encapsulating Security Payload (ESP), which provides confidentiality by encrypting the contents of each packet. ESP can also provide integrity, so tampering is detected.

> **Analogy:** ESP is the sealed envelope. Others can see that a letter is being sent between two people, but they cannot open it to read the message.

## Extra Context (Beyond the Video)

- **Split tunnelling:** Sends only corporate traffic through the VPN, while other traffic goes directly to the Internet. It reduces load on the gateway, but traffic outside the tunnel is not protected by it.
- **Full tunnelling:** Sends all of the user's traffic through the VPN, which gives more control and monitoring, but uses more bandwidth.
