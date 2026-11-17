# Application Security

## Overview

Application security considers how an attacker could target an application, and how to build defences into the code and its inputs.

## Input Validation

Input validation checks that data entered into a field matches what is expected. If a field expects a number, only numbers within a valid range are accepted. Input that does not match is rejected, so images or malicious code cannot be submitted.

> **Analogy:** A nightclub bouncer who checks each guest against the list before letting them in, rather than letting anyone walk through.

- **Prevents:** Cross site scripting (XSS), covered in its own file
- **Prevents:** Buffer overflows, where oversized input spills into memory and can harm the rest of the system, or be acted on by the code

> [!IMPORTANT]
> **Exam clue:** Input validation is the main defence against injection attacks, including SQL injection and XSS.

## Secure Cookies

The `Secure` attribute restricts a cookie so it is only transmitted over an HTTPS channel. It also ensures the cookie can only return to the host that set it.

> **Analogy:** A letter sealed in a locked box that can only travel by a secure courier to one address.

## Fuzzing

Fuzzing sends garbage or unexpected input to an application and observes how it responds. Developers and testers use it to find weaknesses before attackers do.

> **Analogy:** Testing a lock by repeatedly trying random keys to see which ones make it misbehave.
