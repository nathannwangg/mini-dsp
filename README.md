```markdown
# Mini-DSP (Real-Time Bidding Engine)

A lightweight real-time bidding engine built in Go, designed for high-throughput and low-latency programmatic ad bidding. Ideal for educational use or prototyping a demand-side platform (DSP) system.

## Quick Start

```bash
docker compose up -d
curl -X POST localhost:8080 -d '{"id":"1"}'
