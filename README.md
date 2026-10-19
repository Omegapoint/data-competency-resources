# Traineeprogram för Data Engineers

**Status: utkast för intern diskussion.** Förslaget innehåller sex kurser för framtida data engineers. Tid, format, ansvar och teknikval är inte bestämda.

## Varför detta program?

Målet är att utbilda data engineers som kan koppla pålitliga data till beslut, inte bara bygga data pipelines. Traineerna ska förstå en business question, välja rätt data, bygga en lösning och förklara dess värde och begränsningar.

Vi skriver förklaringar på enkel svenska och använder etablerade engelska facktermer, som grain, star schema och stakeholder. Ovanliga termer förklaras när de introduceras.

## Kurskatalog

Kurserna varvar teknik med business context. Business 101 kommer efter databasintroduktionen så att programmeringen får ett tydligt syfte.

| Ordning | Kurs | Central fråga | Underlag för bedömning |
| --- | --- | --- | --- |
| 01 | [Database Foundations](courses/01-database-foundations/README.md) | Hur lagrar och hämtar vi data på ett pålitligt sätt? | Relational schema, constraints och demonstration av transactions |
| 02 | [Business 101: Value Chain, KPIs och Stakeholder Context](courses/02-business-101/README.md) | Var kan data förbättra ett beslut? | Value chain map, stakeholder map och KPI tree |
| 03 | [SQL + Python for DE](courses/03-sql-python-for-de/README.md) | Hur gör vi source data till pålitliga resultat? | En testad data transformation som går att köra om |
| 04 | [Business 102: Requirements, Metric Definitions, Grain och SLA](courses/04-business-102/README.md) | Vad ska vår data product leverera? | Metric definitions, grain, service levels och acceptance criteria |
| 05 | [Data Modelling + Data Warehouse / Lakehouse](courses/05-data-modelling-dw-lakehouse/README.md) | Hur strukturerar vi data för analys? | Dimensional model, motiverade architecture choices och testade queries |
| 06 | [Business 103: Decision-oriented Presentation, Impact och Risk](courses/06-business-103/README.md) | Vilket beslut ska en stakeholder fatta, och hur säkert är underlaget? | Decision brief med impact, risker och assumptions |

## Presentera programmet internt

- Börja med [stakeholder brief](docs/stakeholder-brief.md) för nytta, scope och beslut som behövs.
- Använd kurskatalogen för att diskutera innehåll och lärandemål.
- Använd [gemensamt case och bedömning](docs/shared-case-and-assessment.md) för att visa hur traineerna ska visa sina kunskaper.
- Använd [översikten över DP-900 och DP-750](docs/azure-certifications.md) för att diskutera certifieringsspår och vad som behöver läggas till.
- Använd [litteraturöversikten](docs/reading-list.md) för bokval, koppling till kurserna och förslag på läsordning.
- Använd [kursmallen](templates/course-template.md) när kurser vidareutvecklas eller läggs till.

## Mappkatalog

```text
.
|-- README.md                              # Programöversikt och kurskatalog
|-- docs/
|   |-- stakeholder-brief.md                # Internt förslag och underlag för godkännande
|   |-- shared-case-and-assessment.md       # Sammanhängande övningar och bedömningskriterier
|   |-- azure-certifications.md             # DP-900, DP-750 och koppling till kurserna
|   `-- reading-list.md                     # Litteratur, kurskopplingar och läsordning
|-- courses/
|   |-- 01-database-foundations/README.md
|   |-- 02-business-101/README.md
|   |-- 03-sql-python-for-de/README.md
|   |-- 04-business-102/README.md
|   |-- 05-data-modelling-dw-lakehouse/README.md
|   `-- 06-business-103/README.md
`-- templates/
    `-- course-template.md                 # Återanvändbar kursstruktur i Markdown
```

Varje kurssida har samma struktur: syfte, förkunskaper, lärandemål, begrepp, praktiskt arbete, bedömningsunderlag och planering. Lägg övningar, lösningsförslag och resurser i respektive kursmapp när de är klara.

## Omfattning och utgångspunkter

- Målgrupp: traineer på väg mot en junior roll som data engineer. Kontrollera förkunskaperna före start.
- Detta är en kurs- och dokumentstruktur, inte färdigt undervisningsmaterial.
- Ett fiktivt retail case kopplar tekniken till beslut utan att använda kund- eller produktionsdata.
- Programmet är plattformsneutralt. Välj relational database, Python-miljö och analytics platform innan labbarna byggs.
- Production orchestration, cloud infrastructure, security engineering, streaming och avancerad drift ingår inte i grundprogrammet. Vissa grunder tas upp, men programmet räcker inte för självständigt arbete i produktion.

## Nästa steg

1. Bestäm målgrupp och vad traineerna ska kunna efter programmet.
2. Utse programansvarig, kursansvariga och business reviewers.
3. Bestäm kursordning, tidsbudget och format.
4. Välj labbmiljö och ta fram syntetiska data och referenslösningar.
5. Provkör övningarna och testa att bedömningen fungerar före start.