# Bharat Singh — Go Backend Engineer

```go
stack  → Go · gRPC · Kafka · RabbitMQ · PostgreSQL · Redis · Docker
focus  → Distributed Systems · Event-Driven Architecture · Microservices
method → First principles. Understand the why before the how.
```

---

## What I build

Systems that handle failure gracefully, scale without surprises, and are boring to operate.

I break complex systems down to their fundamentals — then build back up with only what's necessary.

---

## Projects

**[FlowPay](https://github.com/Bharat1Rajput/FlowPay)** `Apr 2026`
4-service distributed payment system. Go · gRPC · Kafka · PostgreSQL.
Idempotent processing, payment state machine (`CREATED → PROCESSING → SUCCESS/FAILED`), DLQ on retry exhaustion.

**[DispatchGo](https://github.com/Bharat1Rajput/DispatchGo)** `Jan 2026`
Distributed webhook dispatcher. Go · RabbitMQ · PostgreSQL.
HTTP ingestion decoupled from async delivery via worker pool + exponential backoff.

**[URL Shortener](https://github.com/Bharat1Rajput/Url-Shortner)** `Mar 2026`
Layered architecture: handler → service → repository. Redis on the hot redirect path. TTL + click analytics.

**[HoldUp](https://github.com/Bharat1Rajput/HoldUp)** `Feb 2026`
Token bucket rate limiter as HTTP middleware. O(1), thread-safe, zero data races (verified by Go race detector).

---

## How I think

Most engineering problems are solved at the conceptual level, not the code level.

Before touching a keyboard: *What is this system actually doing? What can go wrong? What guarantees does it need?*

Idempotency, backpressure, failure modes — these aren't advanced topics. They're the basics.

---

## Links

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bharat5768/)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=flat-square&logo=leetcode&logoColor=black)](https://leetcode.com/BharatSRajput7)
[![Email](https://img.shields.io/badge/Email-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:developer.singh.bharat@gmail.com)
