# 03: SQL + Python for DE

[Programkatalog](../../README.md) | Föregående: [Business 101](../02-business-101/README.md) | Nästa: [Business 102](../04-business-102/README.md)

**Status:** utkast till kursöversikt.

## Syfte

Bygga data transformations med SQL och Python som går att testa och köra om. Det minskar manuellt arbete och gör fel i data synliga.

## Förkunskaper

Kurserna 01-02 eller motsvarande kunskaper. Kontrollera programmeringsvanan och erbjud en Python-introduktion vid behov.

## Lärandemål

APP ska kunna:

- Skriva SQL med joins, aggregations, CTEs och window functions.
- Använda functions, collections, modules samt databas- och filgränssnitt i Python.
- Hantera data types, nulls, datum och fel tydligt.
- Bygga en liten ETL pipeline som går att köra om utan att skapa dubbletter.
- Testa business rules och jämföra resultat med source data.
- Dokumentera kvalitetsfel och kodändringar utan att exponera känsliga data, samt lämna över fel till rätt ansvarig.

## Centrala begrepp

| Område | Begrepp att introducera |
| --- | --- |
| SQL transformations | Join cardinality, GROUP BY, CTEs, window functions, deduplication |
| Python basics | Functions, types, collections, modules, exceptions, structured logging |
| Data interfaces | File formats, database connections, parameterized SQL, configuration |
| Repeatability | Idempotency, incremental loads, checkpoints, late-arriving data |
| Validation | Unit tests, data quality checks, reconciliation, rejected records |
| Arbetssätt | Version control, dependencies, miljösetup, inga credentials i koden |
| Governance i kod | Issue management, spårbara ändringar, data minimization och skydd för logs, testdata och rejected records. Audit evidence visar vad som kördes, vilken version och vilka fel som uppstod utan att kopiera känsliga värden. |

Full orchestration och deployment i produktion ingår inte i kursen.

## Praktiskt arbete

Transformera syntetiska order- och leveransdata från [vårt gemensamma retail case](../../docs/shared-case-and-assessment.md). Beräkna föreslagna metrics från Business 101 med tydligt märkta, preliminära definitioner. Ta med dubbletter och ogiltiga poster. Visa att omkörningar inte ger för höga värden.

Bygg automatiska data quality checks för problemen som hittades i Data Fundamentals. Visa vilka fel som stoppar körningen och vilka poster som avvisas. Dokumentera preliminära regler inför Business 102.

Öva ett kvalitetsfel med syntetiska data. Skapa en issue med omfattning, konsekvens, ansvarig och nästa åtgärd. Spara run ID, kodversion och testresultat, men inga credentials eller känsliga värden i logs eller issues. Begränsa access till rejected records. Dokumentera en kodändring och uppdatera evidence i er [governance brief](../../templates/governance-brief-template.md).

Efter Business 102 ska koden och testerna uppdateras så att de följer överenskomna metric definitions.
Uppdatera även felhantering och dokumentation enligt överenskomna governance-regler.

## Bedömningsunderlag

- SQL- och Python-kod med instruktioner för setup och körning.
- Tester för joins, nulls, dubbletter, datum och säkra omkörningar.
- Tydlig rapportering eller avvisning av ogiltiga poster.
- Reconciliation mellan source data och resultat, plus öppna frågor om definitioner.
- Ett issue-exempel, en spårbar kodändring och test som visar att logs inte exponerar de syntetiska fält som markerats som känsliga.

Använd [den gemensamma bedömningsmatrisen](../../docs/shared-case-and-assessment.md#bedömningsmatris).

## Planering

- Ansvarig, tid och format: inte bestämt.
- Miljö: välj Python-version, database driver, dependency management och test runner.
- Material att ta fram: syntetiska input data, förväntade resultat, startprojekt och referenslösning.
