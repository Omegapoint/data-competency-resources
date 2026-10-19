# 01: Database Foundations

[Programkatalog](../../README.md) | Nästa: [Business 101](../02-business-101/README.md)

**Status:** utkast till kursöversikt.

## Syfte

Förstå hur databaser lagrar data och håller dem konsekventa. Det ger en grund för att undvika felaktiga poster och rapporter.

## Förkunskaper

Grundläggande datorvana. Ingen databaserfarenhet krävs. Kontrollera vilka förberedelser som behövs före kursen.

## Lärandemål

Traineerna ska kunna:

- Förklara tabeller, rader, kolumner, data types, keys och relationships.
- Beskriva en enkel business process med ett relational schema.
- Använda constraints för att skydda data integrity.
- Förklara transactions och visa commit och rollback.
- Förklara hur index kan snabba upp läsning men göra skrivning och lagring dyrare.

## Centrala begrepp

| Område | Begrepp att introducera |
| --- | --- |
| Relational structure | Primary keys, foreign keys, cardinality, nullability, uniqueness |
| Operational design | Normalization, redundancy, insert/update/delete anomalies |
| Integrity och consistency | Constraints, transactions, ACID, grunder i concurrency |
| Queries | SELECT, filtering, joins, aggregation |
| Performance och access | Index, query plans, least privilege |

Mer om data transformation finns i kurs 03. Dimensional modelling behandlas i kurs 05.

## Praktiskt arbete

Modellera kunder, order, orderrader och produkter i [vårt gemensamma retail case](../../docs/shared-case-and-assessment.md). Läs in syntetiska data, visa att en ogiltig foreign key avvisas och gör rollback av en ändring i flera steg.

## Bedömningsunderlag

- Schema diagram, table definitions och en kort data dictionary.
- Queries som visar relationships och enkel datahämtning.
- Tester som visar att ogiltiga keys och dubbla ID:n avvisas.
- Ett exempel på en transaction och en motivering till ett index.

Använd [den gemensamma bedömningsmatrisen](../../docs/shared-case-and-assessment.md#bedömningsmatris).

## Planering

- Ansvarig, tid och format: inte bestämt.
- Miljö: välj en relational database och syntetiska testdata som går att återställa.
- Material att ta fram: schemaövning, demonstration av transactions och referenslösning.
