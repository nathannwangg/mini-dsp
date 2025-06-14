# Problem Statement

Programmatic ad buyers need a low-latency, fault-tolerant bidder to compete in real-time auctions, yet most open-source DSPs are heavyweight or outdated.

I will build a single-container Go RTB engine that handles **50 000 requests per second** with **p95 latency under 7 ms** on commodity hardware and streams every event to Kafka for replay and analytics.

**Success metric:** sustain ≥ 50 k req/s @ p95 < 7 ms for 30 minutes in vegeta load test.
