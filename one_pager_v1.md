# Mini-DSP — One-Pager v1

## 1  Why Now?
Programmatic ad buyers need a low-latency, fault-tolerant bidder to compete in real-time auctions, yet most open-source DSPs are heavyweight or outdated. A lean Go-based engine that demonstrates sub-10 ms latency, infra observability, and container-first deployment is an ideal learning opportunity for me to learn what ad-tech or fintech infra roles involve.

## 2  Who Benefits?
* **Me** — hands-on with Go, Redis, Kafka, Prometheus, Docker, and RTB protocols.  
* **Open-source learners** — a modern, <1000 LOC reference DSP.

## 3  Must-Have (MVP)  
1. Go bidder using **fasthttp**; parses **OpenRTB 2.5** JSON.  
2. **Redis 7 (AOF)** for atomic budget & frequency caps.  
3. **Kafka 3** topic (`rtb-raw`) capturing every request/win/loss.  
4. Built-in **Prometheus** metrics; Grafana dashboard JSON in repo.  
5. **Docker Compose** stack (`bidder + redis + kafka + prom + graf`) with one-command startup.  
6. Vegeta load script sustaining **≥50 k req/s, p95 < 7 ms** on an Apple M1.  
7. CI pipeline (Go tests, `golangci-lint`, image build) required to merge.

## 4  Nice-to-Have (Stretch)  
* Kubernetes manifests with HPA autoscaling.  
* Bloom-filter user allow/deny lists.  
* ClickHouse analytics sink via `KafkaEngine`.  
* OpenTelemetry + Jaeger traces.  
* Rule-based bid shading or pacing algorithm v2.

## 5  Success Metric
> Sustain ≥ 50 k req/s @ p95 < 7 ms for 30 minutes in vegeta load test.

## 6  Non-Goals / Cut Lines
* Creative rendering or ad serving.  
* UI dashboards beyond Grafana default boards.  
* GDPR / CCPA compliance features.  
* Multi-tenant seat management.  
* PCI-style billing settlement.

