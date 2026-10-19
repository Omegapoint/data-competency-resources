# Gemensamt case och bedömning

[Programkatalog](../README.md) | [Stakeholder brief](stakeholder-brief.md)

**Status: förslag till övningar.** Datasets, körbara labbar och referenslösningar behöver tas fram.

## Case: order performance i en fiktiv retail-verksamhet

En operations manager vill veta om sena leveranser och returer kräver åtgärder. APP ska först klargöra beslutet. Därefter kan de enas om vilka KPIs som behövs.

Använd genererade kunder, produkter, order, orderrader, försändelser och returer. Ta med missing values, duplicates, delleveranser, annulleringar, sena leveranser och returer som registreras efter försäljningen.

Använd inte personuppgifter, kundmaterial eller utdrag från produktionssystem.

## Governance genom hela caset

APP ska kunna följa governance-regler och veta när något behöver eskaleras, inte utforma ett helt governance-program. Bygg en gemensam [governance brief](../templates/governance-brief-template.md) genom kurserna:

| Kurs | Tillägg till briefen |
| --- | --- |
| Data Fundamentals | Preliminär classification, lifecycle, metadata och lineage |
| Business 101 | Data owner, data steward, technical owner, metric owner och decision rights |
| SQL + Python for DE | Quality checks, ett issue, skydd för logs/rejected records och spårbara kodändringar |
| Business 102 | Rollspelsreview av regler, access lifecycle, retention/deletion, escalation och change control |
| Data Modelling + DW / Lakehouse | Metadata och downstream lineage, testade access boundaries samt impact review av en schemaändring |
| Business 103 | Kvarvarande risk och dokumenterat riskbeslut eller escalation |

Utbildaren behöver ta fram en kort fiktiv policy, rollkort med mandat och scenarier före piloten. Policyn ska ange classification, tillåten användning och delning, retention/deletion samt regler för access och undantag. Alla data är syntetiska. Godkännanden gäller bara övningen.

Tidiga förslag är preliminära. Efter Business 102 uppdateras kod och brief enligt besluten. Skilj på planerade regler, faktiskt testade kontroller och kvarstående luckor. Full catalog-automation, production audit logging och teknisk deletion i alla backups ingår inte; sådana begränsningar dokumenteras och eskaleras.

## Frågor att reda ut

- Betyder revenue beställt värde, fakturerat värde eller värde efter returer? Hur hanteras skatt, rabatter och valuta?
- Mäts leveransutfall per order, orderrad eller försändelse?
- Hur hanteras delvis levererade eller annullerade order?
- Vilket datum och vilken tidszon styr rapporteringsperioden?
- Vem är metric owner, och vilken källa är source of truth?
- Vilken data freshness kräver beslutet, alltså hur gamla får data vara?
- Vad kan tillgängliga data visa om returer, och vad kräver ytterligare underlag?

## Sammanhängande kursresultat

| Kurs | Praktiskt resultat | Användning i nästa steg |
| --- | --- | --- |
| Data Fundamentals | Enkelt schema, data quality review, data dictionary och lineage-skiss | Ger source context och kända kvalitetsproblem för senare transformations |
| Business 101 | Decision statement, value chain map, stakeholder map och föreslagna KPIs | Ger programmeringsövningen ett syfte |
| SQL + Python for DE | En transformation som går att köra om, med tester och preliminära definitioner | Visar problem att reda ut i Business 102 |
| Business 102 | Metric definitions och acceptance criteria | Styr uppdateringen av kod och data modelling |
| Data Modelling + DW / Lakehouse | Analytical model och testade queries | Tar fram siffror till en decision brief |
| Business 103 | Rekommendation med begränsningar och spårbara siffror | Visar både business understanding och teknisk förståelse |

Den första programmeringsövningen använder dokumenterade, preliminära definitioner. Efter Business 102 uppdaterar APP koden och testerna enligt överenskommelsen. Arbetet görs alltså i flera steg, men slutinlämningen får inte innehålla motstridiga definitioner.

## Föreslagen slutinlämning

- Business question, beslut, målgrupp och scope.
- Source schema, data dictionary och instruktioner för syntetiska data.
- Data quality review med kontroller, följder för användaren, data owner och enkel data lineage.
- Metric definitions med formulas, grain, exclusions, reporting periods och ownership.
- SQL/Python-kod med körinstruktioner och automatiska tester.
- Dimensional model med fact grain, keys, relationships och motiverad history handling.
- Source-to-report reconciliation och exempel på analytical queries.
- Decision brief med impact, assumptions, risker och nästa steg.
- En governance brief med owners, classification, access lifecycle, retention/deletion, quality rules, change control och residual risk, med länkar till beslut och testresultat.

## Bedömningsmatris

Använd tre nivåer: **inte visat ännu**, **visat med stöd** och **visat självständigt i labbmiljön**. Den sista nivån gäller bara övningen, inte självständigt arbete i produktion.

| Område | Underlag som krävs för att visa förmågan |
| --- | --- |
| Business framing | Anger decision-maker, beslut, nytta och berörda stakeholders |
| Metric definitions | Anger formula, grain, time basis, exclusions och hantering av edge cases |
| Data fundamentals | Skiljer data types, file formats och storage options; använder relationships och constraints; förklarar transactions |
| Data quality och context | Skiljer quality från integrity; beskriver quality dimensions, följder för användaren, ownership, source of truth, lineage och least privilege |
| Governance roles och lifecycle | Anger roller och decision rights, tillåten användning, classification och retention/deletion för source och relevanta kopior; motiverar regler med övningens policy |
| Access och auditability | Beskriver request, approval, review och revocation; visar tillåten/nekad läsning och borttagen access i labben; sparar beslut och körningsevidence utan känsliga värden |
| Issue och change management | Visar ansvar, responstid och escalation för ett kvalitetsfel samt downstream impact, tester, godkännande och kommunikation för en ändring |
| Engineering reliability | Kan köras med dokumenterade input data; visar fel tydligt; omkörningar skapar inte dubbletter |
| Analytical modelling | Anger fact grain, undviker join fan-out och förklarar dimensions och history handling |
| Validation | Testar förväntade resultat och edge cases; gör reconciliation mellan source och resultat på jämförbar grain |
| Kommunikation | Ger en tydlig rekommendation, skiljer observation från causality och visar begränsningar |
| Risk acceptance | Beskriver residual risk, risk owner, approver med mandat, villkor och review date; eskalerar när beslut saknas eller ligger utanför mandatet |

## Exempel på acceptance tests

Före kursstart bör utbildarna ta fram fasta syntetiska testdata och förväntade resultat för minst dessa tester:

- Duplicates i input data ger inte ett för högt värde för en metric.
- En join mellan orderrader och flera försändelser multiplicerar inte försäljningssummorna.
- Annullerade order och senare returer följer överenskomna metric definitions.
- Saknade keys och ogiltiga datum ger tydliga validation errors eller dokumenteras som rejected records.
- En omkörning med samma indata ger samma analysresultat utan ytterligare rader.
- En incremental load jämförs med en full beräkning för samma reporting cutoff.
- Data freshness mäts mot överenskommen cutoff och tidszon. Late-arriving data visas, inte döljs.

Detta är exempel. Exakta värden beror på definitionerna och testdata.

## Governance-scenarier att bedöma

- En ny användare begär access. APP anger syfte, classification, minsta access och rätt approver, och dokumenterar beslutet. I labben visas tillåten och nekad läsning samt att access kan tas bort.
- En data quality check fallerar. Körningen följer beslutad stop/reject/warn-regel och lämnar ett issue med ansvarig, responstid och escalation. Logs och issues innehåller inte de syntetiska värden som markerats som känsliga.
- En metric eller ett schema ändras. APP identifierar berörda pipelines, rapporter och användare, uppdaterar tester och definitioner och dokumenterar godkännande och kommunikation.
- En retention-period löper ut. APP beskriver deletion för source och relevanta layers, exports, logs och backups, anger ansvarig och visar vilka delar som är planerade respektive testade. Perioder och undantag följer övningens policy.
- En stakeholder vill använda resultat trots kvarvarande kvalitetsfel. APP visar risk och alternativ. En roll med rätt mandat beslutar med villkor och review date, eller frågan eskaleras. Ingen riskacceptans får åsidosätta policy.

Utbildaren tar fram förväntade beslut och testresultat för scenarierna. Governance bedöms genom briefen, rollspel och labbevidence tillsammans, inte enbart genom ifyllda rubriker.

## Review och feedback

1. Bestäm förväntade testresultat, krav för godkänt och ansvar för review före piloten.
2. Granska resultaten efter varje kurs. Ge både teknisk feedback och feedback från verksamheten där det behövs.
3. Tillåt ändringar och spara motiveringarna till nya definitioner eller modellval.
4. Granska hela slutinlämningen. Tidigare arbete måste följa den slutliga specifikationen.
5. Dokumentera styrkor, kunskapsluckor och behov av fortsatt övning med handledning.

Kursansvariga bör prova bedömningsmatrisen på en referensinlämning. Alla obligatoriska områden behöver visas på den nivå som beslutas. Kravnivåer och regler för komplettering är inte bestämda.
