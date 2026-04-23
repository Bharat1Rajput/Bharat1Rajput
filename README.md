<div align="center">

```
██████╗ ██╗  ██╗ █████╗ ██████╗  █████╗ ████████╗    ███████╗██╗███╗   ██╗ ██████╗ ██╗  ██╗
██╔══██╗██║  ██║██╔══██╗██╔══██╗██╔══██╗╚══██╔══╝    ██╔════╝██║████╗  ██║██╔════╝ ██║  ██║
██████╔╝███████║███████║██████╔╝███████║   ██║       ███████╗██║██╔██╗ ██║██║  ███╗███████║
██╔══██╗██╔══██║██╔══██║██╔══██╗██╔══██║   ██║       ╚════██║██║██║╚██╗██║██║   ██║██╔══██║
██████╔╝██║  ██║██║  ██║██║  ██║██║  ██║   ██║       ███████║██║██║ ╚████║╚██████╔╝██║  ██║
╚═════╝ ╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝╚═╝  ╚═╝   ╚═╝       ╚══════╝╚═╝╚═╝  ╚═══╝ ╚═════╝ ╚═╝  ╚═╝
```

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=22&duration=3000&pause=800&color=00D9FF&center=true&vCenter=true&width=650&lines=Go+Backend+Engineer+%F0%9F%90%B9;Distributed+Systems+Architect+%E2%9A%99%EF%B8%8F;Event-Driven+%7C+gRPC+%7C+Kafka+%7C+PostgreSQL;I+Write+Boring+Code+That+Just+Works.+%F0%9F%92%A1" alt="Typing SVG" />

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/bharat5768/)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Bharat1Rajput)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/BharatSRajput7)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/rajputtwt)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:developer.singh.bharat@gmail.com)

<img src="https://komarev.com/ghpvc/?username=bharat1rajput&label=Profile+Views&color=00D9FF&style=flat-square" />

</div>

---

## `$ whoami`

```go
package main

import "fmt"

type Engineer struct {
    Name        string
    Role        string
    Location    string
    Primary     string
    Focus       []string
    CurrentWork string
    Philosophy  string
}

func main() {
    me := Engineer{
        Name:     "Bharat Singh",
        Role:     "Go Backend Engineer",
        Location: "Bhopal, Madhya Pradesh, India",
        Primary:  "Go (Golang)",
        Focus: []string{
            "Distributed Systems",
            "Event-Driven Architecture",
            "Microservices",
            "System Design & Trade-Offs",
        },
        CurrentWork: "Building Scalable APIs & High-Performance Backends",
        Philosophy:  "Write boring code that ships reliably.",
    }

    fmt.Printf("Hello, World! I'm %s 👋\n", me.Name)
    fmt.Printf("I build systems that scale — %s\n", me.Philosophy)
}
```

---

## `$ cat tech_stack.yaml`

```yaml
languages:
  primary:   Go (Golang)
  secondary: [C++, JavaScript, SQL]

backend:
  frameworks:    [Gin, Chi]
  protocols:     [REST APIs, gRPC]
  patterns:      [Microservices, Event-Driven Architecture]

messaging:
  brokers:       [Apache Kafka, RabbitMQ]

databases:
  relational:    PostgreSQL
  cache:         Redis
  nosql:         MongoDB

devops:
  containers:    Docker
  orchestration: Kubernetes (learning)
  tools:         [Git, Linux]

core_concepts:
  - Concurrency & Goroutines
  - Idempotency
  - State Machines
  - Distributed Systems
  - Exponential Backoff & DLQ

testing:
  - Table-Driven Tests
  - Integration Tests
  - Go Race Detector
```

---

## `$ ls -la projects/`

<details>
<summary><b>🏦 FlowPay — Event-Driven Payment System</b> &nbsp;<code>Apr 2026</code></summary>
<br/>

> **Stack:** `Go` · `gRPC` · `Kafka` · `PostgreSQL` · `Docker`

A **4-service distributed payment system** that doesn't cut corners.

| Service | Responsibility |
|---------|---------------|
| API Gateway | Entry point, auth, routing |
| Order Service | Order lifecycle, consumes `payment.succeeded` |
| Payment Service | Idempotent processing, state machine |
| Notification Service | Async notifications via Kafka events |

**Engineering highlights:**
- ⚡ **gRPC** for sync inter-service communication — typed, fast, versioned
- 📨 **Kafka** as event backbone — decoupled, replayable, durable
- 🔐 **Idempotency** enforced at DB level via `UNIQUE` constraint on idempotency keys
- 🔄 **Payment State Machine:** `CREATED → PROCESSING → SUCCESS/FAILED`
- 🔁 **Retry logic** with exponential backoff + Dead Letter Queue (DLQ) on exhaustion

[![GitHub](https://img.shields.io/badge/View_Source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Bharat1Rajput/FlowPay)

</details>

<details>
<summary><b>📡 DispatchGo — Distributed Webhook Dispatcher</b> &nbsp;<code>Jan 2026</code></summary>
<br/>

> **Stack:** `Go` · `PostgreSQL` · `RabbitMQ` · `Docker`

Re-architected a **monolithic webhook system into a distributed producer-consumer pipeline**.

**Engineering highlights:**
- 🏗️ Decoupled HTTP ingestion from async delivery using **RabbitMQ**
- 🔄 **Worker pool** with goroutines — concurrent, resource-efficient delivery
- ⏳ **Exponential backoff** retry strategy for unreliable endpoints
- 📋 Full **job lifecycle tracking:** `pending → processing → success/failed`
- ✅ **Idempotent processing** — safe to retry, never double-deliver

[![GitHub](https://img.shields.io/badge/View_Source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Bharat1Rajput/DispatchGo)

</details>

<details>
<summary><b>🔗 Scalable URL Shortener</b> &nbsp;<code>Mar 2026</code></summary>
<br/>

> **Stack:** `Go` · `PostgreSQL` · `Redis` · `Docker`

A clean, layered URL shortener with **production-grade architecture**.

**Engineering highlights:**
- 🏛️ **Layered architecture:** `handler → service → repository` — clean separation of concerns
- ⚡ **Redis caching** on the hot redirect path — massively reduced DB reads
- ⏱️ **TTL-based expiration** for short URLs
- 📊 **Analytics tracking:** click count, last accessed timestamp

[![GitHub](https://img.shields.io/badge/View_Source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Bharat1Rajput/Url-Shortner)

</details>

<details>
<summary><b> 🤔HoldUp — Token Bucket Rate Limiter</b> &nbsp;<code>Feb 2026</code></summary>
<br/>

> **Stack:** `Go` · `Concurrency` · `HTTP Middleware`

A **thread-safe, O(1) rate limiter** built from scratch as HTTP middleware.

**Engineering highlights:**
- 🪣 **Token Bucket algorithm** — the industry-standard approach for smooth rate limiting
- 🔒 **Thread-safe** with goroutines + mutex — zero data races (verified by Go race detector)
- ⚡ **O(1) request handling** with lazy refill strategy
- 🧪 **Verified with table-driven tests** across edge cases

[![GitHub](https://img.shields.io/badge/View_Source-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Bharat1Rajput/HoldUp)

</details>

---

## `$ git log --achievements`

```
commit a1b2c3d  🏆 MP Super 100 Scheme
Author: Bharat Singh
Date:   2022

    Selected among Top 100 students statewide in competitive exam.
    Only PCM student selected from the entire district.

```

---

## `$ top` — GitHub Stats

<div align="center">

<img height="175em" src="https://github-readme-stats-eight-theta.vercel.app/api?username=Bharat1Rajput&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true&bg_color=0D1117&title_color=00D9FF&icon_color=00D9FF&text_color=C9D1D9"/>
<img height="175em" src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=Bharat1Rajput&layout=compact&langs_count=8&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=00D9FF&text_color=C9D1D9"/>

<br/>

[![GitHub Streak](https://streak-stats.demolab.com?user=Bharat1Rajput&theme=tokyonight&hide_border=true&background=0D1117&stroke=00D9FF&ring=00D9FF&fire=FF6B6B&currStreakLabel=00D9FF)](https://git.io/streak-stats)

</div>

---

## `$ traceroute me`

```
traceroute to bharat@backend-systems, 5 hops max

1  competitive-programmer  [250+ LC problems, MP Super 100]     ✓
2  go-backend-engineer     [Gin, Chi, gRPC, REST]               ✓
3  distributed-systems     [Kafka, RabbitMQ, State Machines]    ✓
4  infra-aware             [Docker, PostgreSQL, Redis]           ✓
5  bharat@prod             [building things that don't break]   ✓

Packets: 5 sent, 5 received, 0% packet loss
```

---

<div align="center">

### Let's build something that scales.

**📬 `developer.singh.bharat@gmail.com`**

<br/>

![GitHub Snake Animation](https://raw.githubusercontent.com/Bharat1Rajput/Bharat1Rajput/output/snake.svg)

<br/>

*"The best code is the code that doesn't surprise you at 3am."*

</div>
