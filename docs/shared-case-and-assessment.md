# Gemensamt case och bedömning

[Programkatalog](../README.md) | [Stakeholder brief](stakeholder-brief.md)

**Status: förslag till övningar.** Datasets, körbara labbar och referenslösningar behöver tas fram.

## Case: order performance i en fiktiv retail-verksamhet

En operations manager vill veta om sena leveranser och returer kräver åtgärder. Traineerna ska först klargöra beslutet. Därefter kan de enas om vilka KPIs som behövs.

Använd genererade kunder, produkter, order, orderrader, försändelser och returer. Ta med missing values, duplicates, delleveranser, annulleringar, sena leveranser och returer som registreras efter försäljningen.

Använd inte personuppgifter, kundmaterial eller utdrag från produktionssystem.

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
| Database Foundations | Operational schema och integrity checks | Ger relationships för senare transformations |
| Business 101 | Decision statement, value chain map, stakeholder map och föreslagna KPIs | Ger programmeringsövningen ett syfte |
| SQL + Python for DE | En transformation som går att köra om, med tester och preliminära definitioner | Visar problem att reda ut i Business 102 |
| Business 102 | Metric definitions och acceptance criteria | Styr uppdateringen av kod och data modelling |
| Data Modelling + DW / Lakehouse | Analytical model och testade queries | Tar fram siffror till en decision brief |
| Business 103 | Rekommendation med begränsningar och spårbara siffror | Visar både business understanding och teknisk förståelse |

Den första programmeringsövningen använder dokumenterade, preliminära definitioner. Efter Business 102 uppdaterar traineerna koden och testerna enligt överenskommelsen. Arbetet görs alltså i flera steg, men slutinlämningen får inte innehålla motstridiga definitioner.

## Föreslagen slutinlämning

- Business question, beslut, målgrupp och scope.
- Source schema, data dictionary och instruktioner för syntetiska data.
- Metric definitions med formulas, grain, exclusions, reporting periods och ownership.
- SQL/Python-kod med körinstruktioner och automatiska tester.
- Dimensional model med fact grain, keys, relationships och motiverad history handling.
- Source-to-report reconciliation och exempel på analytical queries.
- Decision brief med impact, assumptions, risker och nästa steg.

## Bedömningsmatris

Använd tre nivåer: **inte visat ännu**, **visat med stöd** och **visat självständigt i labbmiljön**. Den sista nivån gäller bara övningen, inte självständigt arbete i produktion.

| Område | Underlag som krävs för att visa förmågan |
| --- | --- |
| Business framing | Anger decision-maker, beslut, nytta och berörda stakeholders |
| Metric definitions | Anger formula, grain, time basis, exclusions och hantering av edge cases |
| Database foundations | Använder rätt relationships och constraints; förklarar transactions |
| Engineering reliability | Kan köras med dokumenterade input data; visar fel tydligt; omkörningar skapar inte dubbletter |
| Analytical modelling | Anger fact grain, undviker join fan-out och förklarar dimensions och history handling |
| Validation | Testar förväntade resultat och edge cases; gör reconciliation mellan source och resultat på jämförbar grain |
| Kommunikation | Ger en tydlig rekommendation, skiljer observation från causality och visar begränsningar |

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

## Review och feedback

1. Bestäm förväntade testresultat, krav för godkänt och ansvar för review före piloten.
2. Granska resultaten efter varje kurs. Ge både teknisk feedback och feedback från verksamheten där det behövs.
3. Tillåt ändringar och spara motiveringarna till nya definitioner eller modellval.
4. Granska hela slutinlämningen. Tidigare arbete måste följa den slutliga specifikationen.
5. Dokumentera styrkor, kunskapsluckor och behov av fortsatt övning med handledning.

Kursansvariga bör prova bedömningsmatrisen på en referensinlämning. Alla obligatoriska områden behöver visas på den nivå som beslutas. Kravnivåer och regler för komplettering är inte bestämda.
