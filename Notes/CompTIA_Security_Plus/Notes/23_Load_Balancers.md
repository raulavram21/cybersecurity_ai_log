# Load Balancers

## Overview

Load balancing keeps services available by spreading user traffic across a cluster of servers. If one server fails or becomes overloaded, the load balancer sends traffic to the others, so users see little or no interruption. Load balancing also removes the single point of failure that a lone server creates.

> **Analogy:** A supermarket with several checkout lanes. The load balancer is the staff member who directs each customer to an open lane, and closes a lane that has stopped working.

## How It Works

A load balancer sits in front of a cluster of servers and receives every incoming request. It chooses a server using a scheduling method, then forwards the request. It also runs **health checks**, which regularly test each server, so a failing server is removed from rotation until it recovers.

## Scheduling Methods

| Method | How it works | Best suited to |
|---|---|---|
| **Round robin** | Sends each new connection to the next server in turn, going around the group | Servers with similar capacity and similar workloads |
| **Least connections** | Sends each new connection to the server with the fewest active connections | Requests that vary in how long they take to complete |
| **Weighted** (extra context) | Gives stronger servers a larger share of traffic | Clusters where servers differ in hardware capacity |
| **Affinity** | Keeps a user connected to the same server for their session | Applications that store session data on one server |

> [!IMPORTANT]
> **Affinity (session persistence):** If a user's session data lives on one server, switching them to another mid-session can log them out or lose their work. Affinity prevents this. It is often set using a cookie or the client's IP address.

## Availability Modes

| Mode | How it works | Trade off |
|---|---|---|
| **Active-active** | All servers handle traffic at the same time | Better use of resources, but needs careful capacity planning |
| **Active-passive** | One server handles traffic, and a standby takes over if it fails | Simpler, but the standby capacity sits idle until a failure occurs |

> **Analogy:** Active-active is two cashiers serving customers at once. Active-passive is one cashier working, with a standby cashier ready to step in if they are called away.

> [!WARNING]
> **Exam clue:** In active-passive, the standby server does no work until a failure. In active-active, every server carries load all the time.

## Extra Context: Layers and Offloading (Beyond the Video)

- **Layer 4 load balancing:** Distributes traffic using network information such as IP address and TCP or UDP port. It is fast but cannot read the content of a request.
- **Layer 7 load balancing:** Reads application data, such as HTTP headers, URLs, or cookies, so it can route requests more intelligently. It is slower but more flexible.
- **SSL/TLS offloading:** The load balancer handles encryption and decryption, so the backend servers spend less processing power on it.

> **Analogy:** Layer 4 is a postal sorter who reads only the postcode. Layer 7 is one who opens the envelope and reads the contents before deciding where it goes.
