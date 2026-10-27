# Kompendium: System Design Fundamentals

Źródło: `pictures.png` (lista tematów "System design fundamentals"). Każdy temat ma krótki opis tutaj oraz szczegółowy plik (kontekst, diagramy, kompromisy, pytania rekrutacyjne, referencje).

## Proponowana ścieżka nauki

1. Podstawy i szacowanie: [Back of the Envelope](topics/21-back-of-the-envelope-estimation.md), [Skalowanie H vs V](topics/20-horizontal-vs-vertical-scaling.md)
2. Warstwa ruchu: Load Balancing → CDN → API Gateway → Rate Limiting
3. Dane: Caching → Invalidation → Partitioning/Sharding → Replication → Database Scaling
4. Teoria rozproszona: CAP → Consistency Models → Eventual Consistency → Leader Election → Distributed Transactions
5. Architektura: Microservices vs Monolith → Service Discovery → Queues → Fault Tolerance → Idempotency

## Indeks

| # | Temat | Krótki opis | Szczegóły |
|---|-------|-------------|-----------|
| 1 | Load Balancing | Rozdzielanie ruchu między instancje (L4/L7, round robin, least conn, consistent hashing). | [01](topics/01-load-balancing.md) |
| 2 | CDN | Sieć brzegowa serwująca statyki i cache blisko użytkownika. | [02](topics/02-cdn.md) |
| 3 | Caching | Trzymanie często używanych danych w szybkiej pamięci (cache-aside, write-through, TTL). | [03](topics/03-caching.md) |
| 4 | Cache Invalidation | Utrzymanie spójności cache z źródłem prawdy (TTL, event-driven, stampede). | [04](topics/04-cache-invalidation.md) |
| 5 | Rate Limiting | Ograniczanie liczby żądań (token bucket, sliding window). | [05](topics/05-rate-limiting.md) |
| 6 | API Gateway | Jeden punkt wejścia: routing, auth, throttling, agregacja. | [06](topics/06-api-gateway.md) |
| 7 | CAP Theorem | Przy partycji sieci wybierasz spójność albo dostępność (+ PACELC). | [07](topics/07-cap-theorem.md) |
| 8 | Sharding | Poziomy podział danych na niezależne węzły wg klucza. | [08](topics/08-sharding.md) |
| 9 | Replication | Kopiowanie danych dla dostępności i odczytów (leader-follower, multi-leader, leaderless). | [09](topics/09-replication.md) |
| 10 | Partitioning | Dzielenie zbioru danych (zakres, hash, lista; pionowe i poziome). | [10](topics/10-partitioning.md) |
| 11 | Queues | Asynchroniczna komunikacja i buforowanie obciążenia (Kafka, RabbitMQ, SQS). | [11](topics/11-queues.md) |
| 12 | Microservices | Małe, niezależnie wdrażane usługi wokół domen biznesowych. | [12](topics/12-microservices.md) |
| 13 | Microservices vs Monoliths | Kiedy który styl; modularny monolit jako środek. | [13](topics/13-microservices-vs-monoliths.md) |
| 14 | Fault Tolerance | Działanie mimo awarii (retry, circuit breaker, bulkhead, redundancja). | [14](topics/14-fault-tolerance.md) |
| 15 | Database Scaling | Indeksy, repliki odczytowe, cache, sharding, CQRS. | [15](topics/15-database-scaling.md) |
| 16 | Service Discovery | Dynamiczne znajdowanie adresów usług (Consul, Eureka, K8s DNS). | [16](topics/16-service-discovery.md) |
| 17 | Consistency Models | Spektrum gwarancji: linearizable → sequential → causal → eventual. | [17](topics/17-consistency-models.md) |
| 18 | Eventual Consistency | Repliki zbiegają się w czasie; konflikty, CRDT, read-your-writes. | [18](topics/18-eventual-consistency.md) |
| 19 | Distributed Transactions | 2PC, Saga, Outbox, TCC. | [19](topics/19-distributed-transactions.md) |
| 20 | Horizontal vs Vertical Scaling | Więcej maszyn vs mocniejsza maszyna. | [20](topics/20-horizontal-vs-vertical-scaling.md) |
| 21 | Back of the Envelope Estimation | Szybkie szacunki QPS, storage, bandwidth. | [21](topics/21-back-of-the-envelope-estimation.md) |
| 22 | Leader Election | Wybór koordynatora (Raft, Paxos, ZooKeeper, lease). | [22](topics/22-leader-election.md) |
| 23 | Idempotency and Data Latency | Bezpieczne powtórki żądań oraz opóźnienia danych/replik. | [23](topics/23-idempotency-and-data-latency.md) |

## Dobre źródła ogólne

- Martin Kleppmann, *Designing Data-Intensive Applications* (DDIA)
- Alex Xu, *System Design Interview* vol. 1 i 2
- [System Design Primer](https://github.com/donnemartin/system-design-primer)
- [Jeff Dean: Numbers Every Programmer Should Know](https://gist.github.com/jboner/2841832)
- [AWS Builders' Library](https://aws.amazon.com/builders-library/)
- [microservices.io](https://microservices.io/patterns/)
