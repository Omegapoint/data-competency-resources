# 05: Data Modelling + Data Warehouse / Lakehouse

[Programkatalog](../../README.md) | Föregående: [Business 102](../04-business-102/README.md) | Nästa: [Business 103](../06-business-103/README.md)

**Status:** utkast till kursöversikt.

## Syfte

Strukturera data för analys och förklara valen bakom modellen. Det gör det lättare att återanvända metrics och undvika fel när data kombineras.

## Förkunskaper

Kurserna 01-04 eller motsvarande kunskaper om relational databases, SQL/Python och metric definitions.

## Lärandemål

APP ska kunna:

- Skilja operational database design från analytical modelling.
- Använda Kimball dimensional modelling: business process, grain, dimensions och facts.
- Bygga ett star schema och skriva queries utan double counting.
- Förklara surrogate keys, conformed dimensions och grunderna i history handling.
- Jämföra data warehouse och lakehouse utifrån requirements.
- Dokumentera metadata och downstream lineage samt verifiera enkla access boundaries och bedöma change impact.

## Centrala begrepp

| Område | Begrepp att introducera |
| --- | --- |
| Dimensional modelling | Kimball, facts, dimensions och star schema. En bus matrix visar vilka business processes som använder samma dimensions. |
| Fact design | Transaction facts, periodic snapshots, accumulating snapshots, measure additivity |
| Dimension design | Business keys, surrogate keys, conformed dimensions, slowly changing dimensions (SCD) type 1 och 2 |
| Analytical correctness | Fact grain, unknown members, late-arriving facts och dimensions. Join fan-out innebär att en join ger fler rader och riskerar att multiplicera värden. |
| Architecture | Data warehouse, data lake, lakehouse, ETL/ELT, storage och modelling |
| Data layers | Raw, staged och curated data; data lineage, data quality checks, access boundaries |
| Governance i modellen | Metadata för tabeller och kolumner, classification, permissions och change impact. Retention/deletion behöver omfatta relevanta layers, exports och kopior, inte bara source-tabellen. |

Ett lakehouse ersätter inte data modelling. Ett star schema kan byggas på olika plattformar. Välj plattform och modell efter behov, inte efter etikett.

## Praktiskt arbete

Bygg en analytical model för [vårt gemensamma retail case](../../docs/shared-case-and-assessment.md) utifrån Business 102. Välj rätt grain för försäljning och leveranser. Visa hur metrics kan kombineras över olika grains utan double counting. Implementera ett litet star schema.

Kontrollera att data quality håller även efter modelleringen. Följ kraven från Business 102 och visa source-to-report reconciliation, inte bara att tabellerna går att läsa.

Uppdatera er [governance brief](../../templates/governance-brief-template.md) med metadata, lineage från source till rapport och access boundaries per layer. Testa att en labbroll får läsa godkända data men inte en skyddad tabell eller kolumn, och att access kan tas bort. Beskriv retention/deletion för source, modell och exports; markera det som kräver plattformsspecifik implementation.

Gör en impact review av en schemaändring: vilka pipelines, metrics och användare berörs? Dokumentera testbehov, approver och hur ändringen kommuniceras. Verktygsstyrd catalog, audit logging och full lifecycle automation ingår inte i grundlabben.

Jämför data warehouse och lakehouse i ett kort architecture decision record. Det räcker att bygga lösningen på en plattform i labbmiljön.

## Bedömningsunderlag

- Bus matrix, star schema diagram och data dictionary med tydlig fact grain.
- Motivering av keys och history handling, med ett exempel på en ändrad dimension.
- Load logic och queries för överenskomna metrics.
- Tester för key uniqueness, relationships, join fan-out och source-to-report reconciliation.
- Ett architecture decision record med requirements, trade-offs och begränsningar.
- Uppdaterad metadata och lineage, resultat från access- och revocation-test samt impact review för en schemaändring.

Använd [den gemensamma bedömningsmatrisen](../../docs/shared-case-and-assessment.md#bedömningsmatris).

## Planering

- Ansvarig, tid och format: inte bestämt.
- Miljö: välj en SQL-plattform för analys och testdata som går att återställa.
- För governance-labben behövs separata testroller och stöd för att ge, neka och ta bort läsbehörighet.
- Material att ta fram: modelling scenarios, testdata för SCD och en referensmodell.
