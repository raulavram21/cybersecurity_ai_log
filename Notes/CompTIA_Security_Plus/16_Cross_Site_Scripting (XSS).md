# Cross Site Scripting (XSS)

## Overview

Cross site scripting (XSS) is a form of injection attack. The attacker sends malicious code, usually JavaScript, to a web application. The aim is to misrepresent data or make the application malfunction.

## Why It Works

XSS happens when the web application does not sanitise its inputs. It accepts whatever the user sends, without checking that it matches what is expected. For example, a field that should only receive a number accepts a script instead.

> **Analogy:** A postal sorting office that delivers any parcel without checking the contents, so a booby trapped package ends up on the doorstep of whoever opens it.

## Types of XSS

| Type | Where the payload lives | How it triggers |
|---|---|---|
| **Reflected** | In the request, often a crafted link | The server echoes the input back and the victim's browser runs the script immediately |
| **Stored** | In the database, such as comments, reviews, or forum posts | The script is served to every visitor who views the stored content |

> [!IMPORTANT]
> **Reflected vs stored:** Reflected XSS needs the victim to click a crafted link. Stored XSS needs nothing from the victim beyond visiting the page, so it can affect every visitor.

> **Analogy:** Reflected XSS is a trap set on the doorstep that goes off when one person steps on it. Stored XSS is a trap built into the shared lobby floor that catches everyone who walks through.
