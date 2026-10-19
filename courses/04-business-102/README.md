# 04: Business 102 - Requirements, Metric Definitions, Grain och SLA

[Programkatalog](../../README.md) | Föregående: [SQL + Python for DE](../03-sql-python-for-de/README.md) | Nästa: [Data Modelling + DW / Lakehouse](../05-data-modelling-dw-lakehouse/README.md)

**Status:** utkast till kursöversikt.

## Syfte

Gå från en business question till en tydlig och testbar specifikation för en data product. Stakeholders ska vara överens om vad siffrorna betyder och när data måste finnas.

## Förkunskaper

Kurserna 01-03 eller motsvarande erfarenhet. Ta med föreslagna KPIs och problem med data från tidigare övningar.

## Lärandemål

APP ska kunna:

- Formulera requirements utifrån ett beslut, inte bara ett önskat diagram.
- Definiera en metric så tydligt att två data engineers får samma resultat.
- Ange grain: vad en rad representerar.
- Sätta mätbara mål för data freshness, data quality och availability.
- Skriva acceptance criteria och ange vem som godkänner definitioner och ändringar.
- Beskriva access lifecycle, escalation och change control samt ange vilket mandat som krävs för undantag.

## Centrala begrepp

| Område | Begrepp att introducera |
| --- | --- |
| Requirements framing | User, beslut, nytta, scope, constraints och exclusions |
| Metric definitions | Formula, numerator/denominator, units, filters, time basis, ownership |
| Grain och aggregation | Order, orderrad eller försändelse; distinct counts; additive och non-additive measures |
| Service levels | SLI (service level indicator: vad vi mäter), SLO (service level objective: målet), SLA (service level agreement: överenskommet åtagande) |
| Acceptance och change | Exempelbaserade acceptance criteria, source of truth, godkännande, version control för definitioner |
| Access lifecycle | Request, approval, tilldelning, återkommande access review och revocation när behovet upphör. Ange ansvarig och evidence för varje steg. |
| Issue och change management | Severity, escalation, change impact, godkännande, kommunikation och uppföljning av undantag. En teknisk roll godkänner inte själv business risk. |

Skilj på föreslagna targets i övningen och ett SLA som ansvariga faktiskt har godkänt för produktion.

## Praktiskt arbete

Red ut olika definitioner av revenue och on-time delivery i [vårt gemensamma retail case](../../docs/shared-case-and-assessment.md). Använd delleveranser, annulleringar och senare returer för att hitta oklarheter. Enas om definitionerna med en person som spelar business owner. Uppdatera sedan koden och testerna från kurs 03.

Använd data quality review från Data Fundamentals och testerna från kurs 03 för att bestämma quality requirements, data owner, gränsvärden och åtgärder vid fel. Koppla kraven till beslutet som data ska stödja.

Gör en rollspelsreview av er [governance brief](../../templates/governance-brief-template.md). Bestäm classification, tillåten användning, access requirements, retention/deletion och quality rules utifrån övningens policy. Ange hur access begärs, godkänns, följs upp och tas bort. Sätt kontaktväg och responstid för kvalitetsfel.

Pröva en ändrad metric definition och ett önskemål om bredare access. Dokumentera downstream impact, beslut, approver, berörda användare och tid för uppföljning. Oklara policy- eller privacy-frågor eskaleras till rätt roll, inte avgörs av APP. Alla godkännanden gäller bara övningen.

## Bedömningsunderlag

- En requirements brief med beslut, målgrupp, scope och exclusions.
- Metric definitions med formula, grain, datum/tidszon, edge cases, source och owner.
- Förslag till service levels med mätmetod, target, reporting window och åtgärder vid avvikelse.
- Acceptance examples med förväntade resultat samt lösta och öppna frågor.
- Uppdaterad kod och tester som följer specifikationen.
- En granskad governance brief med access lifecycle, retention/deletion, escalation och change control, inklusive beslut och öppna frågor från rollspelet.

Använd [den gemensamma bedömningsmatrisen](../../docs/shared-case-and-assessment.md#bedömningsmatris).

## Planering

- Ansvarig, tid och format: inte bestämt.
- Miljö: resultat från tidigare övningar och en workshop med business reviewers.
- Material att ta fram: motstridiga requirements, testdata för metrics och en exempelspecifikation.
