# Mini-DSP (Real-Time Bidding Engine)

A lightweight real-time bidding engine built in Go, designed for high-throughput and low-latency programmatic ad bidding.

**Mini-DSP** is a single-container Go RTB engine built to handle **50,000 requests per second** with **p95 latency under 7 ms** on commodity hardware. It streams every auction event to Kafka for replay and analytics

---

## Quick Start

```bash
docker compose up -d
curl -X POST http://localhost:8080 -d '{"id":"1"}'
