# 01: Data Fundamentals

[Programkatalog](../../README.md) | Nästa: [Business 101](../02-business-101/README.md)

**Status:** utkast till kursöversikt.

## Syfte

Förstå olika typer av data, hur de lagras och vad som gör dem användbara. Kursen kombinerar database basics med data quality och data context så att APP kan upptäcka problem innan data används i beslut.

## Förkunskaper

Grundläggande datorvana. Ingen erfarenhet av databaser eller programmering krävs. Kontrollera vilka förberedelser som behövs före kursen.

## Lärandemål

APP ska kunna:

- Skilja structured, semi-structured och unstructured data samt känna igen vanliga file formats.
- Jämföra relational och non-relational storage samt transactional och analytical workloads på grundnivå.
- Beskriva en enkel business process med tabeller, data types, keys och relationships.
- Använda enkla queries och constraints samt visa commit och rollback i en transaction.
- Identifiera data quality-problem och skilja data quality från data integrity.
- Beskriva metadata, data owner, source of truth och enkel data lineage.
- Känna igen personuppgifter och känsliga data samt förklara least privilege.
- Förklara vad data governance är, skilja på grundroller och föreslå classification och lifecycle-regler i ett övningsfall.

## Centrala begrepp

| Område | Begrepp att introducera |
| --- | --- |
| Data concepts | Structured, semi-structured och unstructured data; data types; CSV, JSON och Parquet |
| Data storage | Relational databases, översikt av NoSQL, transactional kontra analytical workloads |
| Database basics | Tables, primary keys, foreign keys, relationships, cardinality och enkel normalization |
| Data integrity | Constraints, nullability, uniqueness, referential integrity, transactions, ACID, commit och rollback |
| Queries | SELECT, filtering, enkla joins och aggregation |
| Data quality | Accuracy, completeness, validity, consistency, uniqueness och timeliness |
| Data context | Metadata, data dictionary, data owner, source of truth och data lineage: datans väg från källa till användning |
| Responsible data use | Personuppgifter, känsliga data och least privilege: bara den access som behövs |
| Data governance | Vem får bestämma om data, vilka regler gäller och hur följer vi upp dem? Data owner ansvarar för beslut, data steward för löpande definitioner och kvalitet, technical owner för implementation och drift. |
| Classification och lifecycle | Classification beskriver hur känsliga data är och hur de får användas. Retention anger hur länge de sparas. Deletion omfattar även kopior och downstream data enligt gällande regler. |

Data quality handlar om att data fungerar för sitt syfte. Accuracy betyder att värden stämmer med verkligheten. Completeness handlar om att nödvändiga data finns, validity om att de följer regler och consistency om att de inte motsäger varandra. Uniqueness handlar om oönskade dubbletter och timeliness om att data finns i tid och är tillräckligt aktuella.

Data integrity är inte samma sak som data quality. En order kan ha rätt data types och giltiga keys men ändå ha fel pris. Dagliga uppdateringar kan räcka för en månadsrapport men vara för gamla för ett operativt beslut.

Kursen fokuserar på att känna igen problem och göra enkla kontroller. Automatiska data quality checks byggs i kurs 03. Krav och ansvar bestäms i Business 102. Dimensional modelling behandlas i kurs 05. Index nämns kort; fördjupning i index, query plans och concurrency ingår inte.

## Praktiskt arbete

Använd syntetiska kunder, order, orderrader och produkter i [vårt gemensamma retail case](../../docs/shared-case-and-assessment.md).

1. Jämför exempel i CSV och JSON och beskriv hur de kan lagras.
2. Bygg ett enkelt relational schema och läs in data. Visa en query, en avvisad foreign key och rollback av en ändring.
3. Undersök missing values, duplicates, ogiltiga datum, motstridiga värden och gamla uppdateringar.
4. Jämför ett pris med en given referenskälla. Visa varför giltiga constraints inte garanterar accuracy.
5. Beskriv vilka problem som påverkar en månadsrapport respektive ett operativt beslut.
6. Dokumentera data owner, source of truth, enkel data lineage och vilken access olika roller behöver.
7. Starta en [governance brief](../../templates/governance-brief-template.md). Föreslå classification, tillåten användning och retention/deletion för ett dataset. Märk reglerna som preliminära, inte som godkänd policy.

## Bedömningsunderlag

- En kort jämförelse av data types, file formats och storage options.
- Schema diagram, table definitions, data dictionary och enkla queries.
- Kontroller som visar att ogiltiga keys och dubbla ID:n avvisas, plus ett exempel på commit och rollback.
- En data quality review med problem, quality dimension, enkel kontroll och följd för användaren. Föreslagna gränsvärden märks som preliminära inför Business 102.
- En enkel lineage-skiss med data owner, source of truth och förslag på access enligt least privilege.
- Ett första utkast till governance brief med classification, lifecycle och öppna frågor om ansvar.

Använd [den gemensamma bedömningsmatrisen](../../docs/shared-case-and-assessment.md#bedömningsmatris).

## Planering

- Ansvarig, tid och format: inte bestämt.
- Miljö: välj en relational database och syntetiska testdata som går att återställa.
- Material att ta fram: CSV/JSON-exempel, schemaövning, kvalitetsbrister med kända förväntade resultat, referenspriser, demonstration av transactions och referenslösning.
- Governance-material: fiktiva policykrav och syntetiska fält som används för att öva classification. Inga riktiga personuppgifter används.
