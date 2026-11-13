# 13 SQL Injection

## Overview

SQL injection is a very common attack. It inserts malicious logic into a standard database query, so the database runs the attacker's instructions alongside the intended ones.

## How It Works

A normal query asks the database for one record. In this example, it selects a user with a specific ID.

```sql
SELECT * FROM users WHERE id = 2968;
```

An attacker injects extra logic into the query, such as `OR 1=1`. Because `1=1` is always true, the condition matches every row in the table.

```sql
SELECT * FROM users WHERE id = 2968 OR 1=1;
```

> **Analogy:** A bouncer checks a guest list by asking "Is this person on the list?" An attacker answers "Yes, and so is everyone else", so the door opens for the whole crowd.

> [!IMPORTANT]
> **Exam clue:** If a question shows a SQL statement containing `OR 1=1`, it is almost certainly describing a SQL injection attack.

## Why It Works

The application builds the query by joining its own text with user input, without checking that input. The database cannot tell the intended logic from the injected logic, so it runs both.

## Common Types

| Type | How the attacker learns the result |
|---|---|
| **In-band (error based)** | Reads database error messages that reveal structure or data |
| **Union based** | Adds a `UNION SELECT` to pull data from other tables into the response |
| **Blind** | Infers answers from true or false responses, or from delays in the response time |

## Impact

- Reading sensitive data, such as usernames, passwords, and card details
- Changing or deleting records
- Bypassing login screens
- In some setups, running commands on the server

## Prevention

- **Parameterized queries (prepared statements):** Treat user input as data, never as part of the query logic. This is the main defence.
- **Input validation:** Reject input that does not match the expected format, such as a numeric ID that contains letters.
- **Least privilege:** Give the application database account only the permissions it needs.
- **Web application firewall (WAF):** Adds a filter in front of the application. It is useful, but it is a supporting layer, not a replacement for secure code.

> **Analogy:** Parameterized queries are like a form with fixed boxes. Whatever is typed in a box stays in that box, and it cannot rewrite the form itself.

> [!WARNING]
> **Common mistake:** Escaping input by hand is error prone. Use parameterized queries wherever the language supports them.
