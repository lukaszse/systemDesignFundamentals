# Microservices vs Monoliths

[← Indeks](../README.md)

## Porównanie
| Aspekt | Monolit | Mikroserwisy |
|--------|---------|--------------|
| Deploy | Jeden artefakt | Niezależne |
| Skalowanie | Całość | Per usługa |
| Złożoność | W kodzie | W operacjach/sieci |
| Transakcje | ACID lokalnie | Saga, spójność ostateczna |
| Latencja | Wywołania in-process | Sieć |
| Zespół | Mały, jedna baza kodu | Wiele autonomicznych zespołów |
| Debugowanie | Proste | Distributed tracing |
| Technologie | Jedna | Poliglotyczne |

## Środek: modularny monolit
Jeden deployment, ale silne granice modułów (pakiety/moduły, API między modułami, brak współdzielonych tabel). Łatwa ewolucja do mikroserwisów (Spring Modulith, ArchUnit).

```mermaid
flowchart LR
    M[Monolit] --> MM[Modularny monolit] --> MS[Mikroserwisy]
```

## Kiedy co
- **Monolit / modularny monolit**: start-up, niejasna domena, mały zespół, MVP.
- **Mikroserwisy**: wiele zespołów (Conway's Law), różne wymagania skalowania, dojrzałe DevOps, jasne bounded contexts.
- Migracja: **Strangler Fig**, anti-corruption layer.

## Antywzorzec
*Distributed monolith* – usługi ściśle sprzężone, wdrażane razem.

## Referencje
- [Fowler: MonolithFirst](https://martinfowler.com/bliki/MonolithFirst.html)
- [Spring Modulith](https://spring.io/projects/spring-modulith)
- [Amazon Prime Video: powrót do monolitu (case study)](https://www.primevideotech.com/video-streaming/scaling-up-the-prime-video-audio-video-monitoring-service-and-reducing-costs-by-90)
- Powiązane: [Microservices](12-microservices.md)
