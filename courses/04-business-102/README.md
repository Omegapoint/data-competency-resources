# 04: Business 102 - Requirements, Metric Definitions, Grain och SLA

[Programkatalog](../../README.md) | Föregående: [SQL + Python for DE](../03-sql-python-for-de/README.md) | Nästa: [Data Modelling + DW / Lakehouse](../05-data-modelling-dw-lakehouse/README.md)

**Status:** utkast till kursöversikt.

## Syfte

Gå från en business question till en tydlig och testbar specifikation för en data product. Stakeholders ska vara överens om vad siffrorna betyder och när data måste finnas.

## Förkunskaper

Kurserna 01-03 eller motsvarande erfarenhet. Ta med föreslagna KPIs och problem med data från tidigare övningar.

## Lärandemål

Traineerna ska kunna:

- Formulera requirements utifrån ett beslut, inte bara ett önskat diagram.
- Definiera en metric så tydligt att två data engineers får samma resultat.
- Ange grain: vad en rad representerar.
- Sätta mätbara mål för data freshness, data quality och availability.
- Skriva acceptance criteria och ange vem som godkänner definitioner och ändringar.

## Centrala begrepp

| Område | Begrepp att introducera |
| --- | --- |
| Requirements framing | User, beslut, nytta, scope, constraints och exclusions |
| Metric definitions | Formula, numerator/denominator, units, filters, time basis, ownership |
| Grain och aggregation | Order, orderrad eller försändelse; distinct counts; additive och non-additive measures |
| Service levels | SLI (service level indicator: vad vi mäter), SLO (service level objective: målet), SLA (service level agreement: överenskommet åtagande) |
| Acceptance och change | Exempelbaserade acceptance criteria, source of truth, godkännande, version control för definitioner |

Skilj på föreslagna targets i övningen och ett SLA som ansvariga faktiskt har godkänt för produktion.

## Praktiskt arbete

Red ut olika definitioner av revenue och on-time delivery i [vårt gemensamma retail case](../../docs/shared-case-and-assessment.md). Använd delleveranser, annulleringar och senare returer för att hitta oklarheter. Enas om definitionerna med en person som spelar business owner. Uppdatera sedan koden och testerna från kurs 03.

## Bedömningsunderlag

- En requirements brief med beslut, målgrupp, scope och exclusions.
- Metric definitions med formula, grain, datum/tidszon, edge cases, source och owner.
- Förslag till service levels med mätmetod, target, reporting window och åtgärder vid avvikelse.
- Acceptance examples med förväntade resultat samt lösta och öppna frågor.
- Uppdaterad kod och tester som följer specifikationen.

Använd [den gemensamma bedömningsmatrisen](../../docs/shared-case-and-assessment.md#bedömningsmatris).

## Planering

- Ansvarig, tid och format: inte bestämt.
- Miljö: resultat från tidigare övningar och en workshop med business reviewers.
- Material att ta fram: motstridiga requirements, testdata för metrics och en exempelspecifikation.
