# 03: SQL + Python for DE

[Programkatalog](../../README.md) | Föregående: [Business 101](../02-business-101/README.md) | Nästa: [Business 102](../04-business-102/README.md)

**Status:** utkast till kursöversikt.

## Syfte

Bygga data transformations med SQL och Python som går att testa och köra om. Det minskar manuellt arbete och gör fel i data synliga.

## Förkunskaper

Kurserna 01-02 eller motsvarande kunskaper. Kontrollera programmeringsvanan och erbjud en Python-introduktion vid behov.

## Lärandemål

Traineerna ska kunna:

- Skriva SQL med joins, aggregations, CTEs och window functions.
- Använda functions, collections, modules samt databas- och filgränssnitt i Python.
- Hantera data types, nulls, datum och fel tydligt.
- Bygga en liten ETL pipeline som går att köra om utan att skapa dubbletter.
- Testa business rules och jämföra resultat med source data.

## Centrala begrepp

| Område | Begrepp att introducera |
| --- | --- |
| SQL transformations | Join cardinality, GROUP BY, CTEs, window functions, deduplication |
| Python basics | Functions, types, collections, modules, exceptions, structured logging |
| Data interfaces | File formats, database connections, parameterized SQL, configuration |
| Repeatability | Idempotency, incremental loads, checkpoints, late-arriving data |
| Validation | Unit tests, data quality checks, reconciliation, rejected records |
| Arbetssätt | Version control, dependencies, miljösetup, inga credentials i koden |

Full orchestration och deployment i produktion ingår inte i kursen.

## Praktiskt arbete

Transformera syntetiska order- och leveransdata från [vårt gemensamma retail case](../../docs/shared-case-and-assessment.md). Beräkna föreslagna metrics från Business 101 med tydligt märkta, preliminära definitioner. Ta med dubbletter och ogiltiga poster. Visa att omkörningar inte ger för höga värden.

Efter Business 102 ska koden och testerna uppdateras så att de följer överenskomna metric definitions.

## Bedömningsunderlag

- SQL- och Python-kod med instruktioner för setup och körning.
- Tester för joins, nulls, dubbletter, datum och säkra omkörningar.
- Tydlig rapportering eller avvisning av ogiltiga poster.
- Reconciliation mellan source data och resultat, plus öppna frågor om definitioner.

Använd [den gemensamma bedömningsmatrisen](../../docs/shared-case-and-assessment.md#bedömningsmatris).

## Planering

- Ansvarig, tid och format: inte bestämt.
- Miljö: välj Python-version, database driver, dependency management och test runner.
- Material att ta fram: syntetiska input data, förväntade resultat, startprojekt och referenslösning.
