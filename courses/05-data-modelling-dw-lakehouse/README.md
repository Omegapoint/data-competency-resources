# 05: Data Modelling + Data Warehouse / Lakehouse

[Programkatalog](../../README.md) | Föregående: [Business 102](../04-business-102/README.md) | Nästa: [Business 103](../06-business-103/README.md)

**Status:** utkast till kursöversikt.

## Syfte

Strukturera data för analys och förklara valen bakom modellen. Det gör det lättare att återanvända metrics och undvika fel när data kombineras.

## Förkunskaper

Kurserna 01-04 eller motsvarande kunskaper om relational databases, SQL/Python och metric definitions.

## Lärandemål

Traineerna ska kunna:

- Skilja operational database design från analytical modelling.
- Använda Kimball dimensional modelling: business process, grain, dimensions och facts.
- Bygga ett star schema och skriva queries utan double counting.
- Förklara surrogate keys, conformed dimensions och grunderna i history handling.
- Jämföra data warehouse och lakehouse utifrån requirements.

## Centrala begrepp

| Område | Begrepp att introducera |
| --- | --- |
| Dimensional modelling | Kimball, facts, dimensions och star schema. En bus matrix visar vilka business processes som använder samma dimensions. |
| Fact design | Transaction facts, periodic snapshots, accumulating snapshots, measure additivity |
| Dimension design | Business keys, surrogate keys, conformed dimensions, slowly changing dimensions (SCD) type 1 och 2 |
| Analytical correctness | Fact grain, unknown members, late-arriving facts och dimensions. Join fan-out innebär att en join ger fler rader och riskerar att multiplicera värden. |
| Architecture | Data warehouse, data lake, lakehouse, ETL/ELT, storage och modelling |
| Data layers | Raw, staged och curated data; data lineage, data quality checks, access boundaries |

Ett lakehouse ersätter inte data modelling. Ett star schema kan byggas på olika plattformar. Välj plattform och modell efter behov, inte efter etikett.

## Praktiskt arbete

Bygg en analytical model för [vårt gemensamma retail case](../../docs/shared-case-and-assessment.md) utifrån Business 102. Välj rätt grain för försäljning och leveranser. Visa hur metrics kan kombineras över olika grains utan double counting. Implementera ett litet star schema.

Jämför data warehouse och lakehouse i ett kort architecture decision record. Det räcker att bygga lösningen på en plattform i labbmiljön.

## Bedömningsunderlag

- Bus matrix, star schema diagram och data dictionary med tydlig fact grain.
- Motivering av keys och history handling, med ett exempel på en ändrad dimension.
- Load logic och queries för överenskomna metrics.
- Tester för key uniqueness, relationships, join fan-out och source-to-report reconciliation.
- Ett architecture decision record med requirements, trade-offs och begränsningar.

Använd [den gemensamma bedömningsmatrisen](../../docs/shared-case-and-assessment.md#bedömningsmatris).

## Planering

- Ansvarig, tid och format: inte bestämt.
- Miljö: välj en SQL-plattform för analys och testdata som går att återställa.
- Material att ta fram: modelling scenarios, testdata för SCD och en referensmodell.
