# Email Security

## Overview

Email is insecure by default. Messages can be spoofed, so a spammer can pretend to come from a trusted domain. Email security uses DNS records and checks at the receiving server to confirm that a message really came from the domain it claims.

## The Three Records

| Record | What it checks | How it works |
|---|---|---|
| **SPF** (Sender Policy Framework) | Which servers are allowed to send mail for the domain | The domain's DNS lists its authorised mail servers. Mail from any other server fails |
| **DKIM** (DomainKeys Identified Mail) | Whether the message was altered and really came from the domain | The sending server signs each message with a private key. The matching public key is published in DNS, so the receiver can verify the signature |
| **DMARC** (Domain-based Message Authentication, Reporting and Conformance) | What to do when SPF or DKIM fails | The domain owner publishes a policy in DNS, which tells receivers to do nothing, quarantine, or reject failing messages, and to send reports |

> **Analogy:** SPF is a list of approved couriers. DKIM is a wax seal that only the sender can produce. DMARC is the instruction on the envelope that tells the post office what to do with anything that fails the checks.

> [!IMPORTANT]
> **Exam clue:** SPF checks the sending server. DKIM checks the message signature. DMARC decides the action and reporting when either check fails.

## How a Message Is Checked

1. The domain's SPF, DKIM, and DMARC records are published in DNS
2. The sender's mail transfer agent (MTA) forwards the message with SPF and DKIM headers
3. A spammer may send from a server with a spoofed domain name
4. The recipient's MTA checks the message against the DNS records
5. A legitimate message is delivered to the recipient's mailbox
6. A message failing DMARC is rejected
7. A failure report is sent back to the sender's MTA

> [!WARNING]
> **Spoofing:** Without these checks, a message can show a trusted sender's address while coming from an attacker's server. Failing DMARC is the signal that it should not be delivered.

## Mail Gateway Inspection

A mail gateway sits in front of the mail servers and inspects incoming email for malware, suspicious links, and other threats. Threats are stopped at the gateway before they reach users' mailboxes.

> **Analogy:** A mail room that checks every parcel with an X-ray before it reaches the office floor.
