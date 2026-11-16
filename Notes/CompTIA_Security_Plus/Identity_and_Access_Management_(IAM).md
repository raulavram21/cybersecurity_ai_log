# Identity and Access Management (IAM)

## Overview

Identity and access management covers how user accounts are created, proven, and shared across systems. These topics often appear together on the exam, so it helps to see how they connect.

## Account Creation and Identity Proofing

- **Separation of duties:** No single person should create user accounts alone. Requests should come from an authorised department, such as HR or the technology director
- **Identity proofing:** Proving that a person is who they claim to be before an account is issued

> **Analogy:** Opening a bank account requires two people to sign off, and you show ID before the account is activated.

## Federation

Federation lets one identity be trusted across several organizations or services, so a user does not need a separate login for each.

## Single Sign On (SSO)

Single sign on lets a user authenticate once through a secure means and then access several services without logging in again.

> **Analogy:** A theme park wristband. You show your ticket once at the gate, then ride everything without buying a new ticket each time.

## Directories and LDAP

The Lightweight Directory Access Protocol (LDAP) is a common way to store and look up identity information. Entries are described using X.500 attributes.

| Attribute | Meaning |
|---|---|
| **CN** | Common name of the object |
| **OU** | Organizational unit, such as a work group |
| **O** | Organization, such as a company |
| **L** | Locality, such as a city or town |
| **ST** | State |
| **C** | Country |
| **DC** | Domain component |

## Cloud Access Security Broker (CASB)

A CASB sits between an organization and its cloud services. It enforces security policy, monitors activity, and controls access to cloud applications.

## OAuth and OpenID Connect

- **OAuth:** An authorisation framework, first developed by Twitter, that lets a user grant an app limited access to their account without sharing their password
- **OpenID Connect:** Built on OAuth to add authentication, so the service can confirm who the user is

> **Analogy:** OAuth is a valet key. It lets the valet drive the car without giving them the house key. OpenID Connect adds a check that confirms who the valet is.

## SAML

The Security Assertion Markup Language (SAML) is an XML format used to pass authentication information between an identity provider and a service provider. It is the standard for authenticating users across the open Internet.

> [!IMPORTANT]
> **Exam clue:** SAML is the XML format for authenticating users over the open Internet. OAuth handles authorisation, while SAML handles authentication.

## Attestation

Attestation is a formal statement affirming that information is correct and valid. The person signing attests to the accuracy of the credentials or data they provide.
