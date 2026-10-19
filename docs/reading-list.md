# Litteraturöversikt och koppling till kurserna

[Programkatalog](../README.md) | [Stakeholder brief](stakeholder-brief.md) | [Certifieringsöversikt](azure-certifications.md)

**Status: förslag till litteraturstöd.** Kurskopplingar och prioritering är våra rekommendationer. Inköp är inte beslutade. Läsningen gäller utvalda avsnitt, inte sex hela böcker.

## Kort sammanfattning för stakeholders

| Bok | Bidrag | Föreslagen roll |
| --- | --- | --- |
| Fundamentals of Data Engineering | Överblick av rollen och data engineering lifecycle | Gemensam bas med utvalda avsnitt |
| SQL for Data Analysis | Praktisk SQL för att besvara analysfrågor | Praktiskt litteraturstöd för kurs 03 och stöd för kurs 04–05 |
| The Data Warehouse Toolkit | Dimensional modelling, grain och star schema | Huvudreferens för kurs 05 och stöd för kurs 04 |
| Storytelling with Data | Data visualization och storytelling för rätt målgrupp | Huvudreferens för kommunikationsdelen i kurs 06 |
| Designing Data-Intensive Applications | Reliability och trade-offs i datasystem | Utvald fördjupning efter grundkurserna |
| NoSQL Distilled | Non-relational data models och när de passar | Valbar för kurs 01 och 05; möjlig att stryka |

**Rekommendation:** prioritera utvalda delar av Fundamentals of Data Engineering, SQL for Data Analysis, The Data Warehouse Toolkit och Storytelling with Data. Använd Designing Data-Intensive Applications för fördjupning med handledare. NoSQL Distilled är valbar och kan strykas om tid eller budget inte räcker. Grunderna i non-relational data behöver då täckas av kursmaterialet.

## Böckerna i korthet

### Fundamentals of Data Engineering

**Författare:** Joe Reis och Matt Housley. **Förlag och referensutgåva:** O'Reilly, första upplagan, 2022.

Boken ger en överblick av data engineering: source systems, ingestion, storage, transformation och serving. Den kopplar architecture, security, data governance och arbetssätt till business needs.

- **Användning:** gemensamt språk för rollen och data engineering lifecycle, främst i kurserna 01, 03 och 05.
- **Lästeman:** lifecycle, business needs, architecture choices, ingestion, transformation och serving.
- **Begränsning:** ersätter inte SQL/Python-övningar eller labbar på den valda plattformen.
- **Bokinformation:** [O'Reilly](https://www.oreilly.com/library/view/fundamentals-of-data/9781098108304/).

### SQL for Data Analysis

**Författare:** Cathy Tanimura. **Förlag och referensutgåva:** O'Reilly, första upplagan, 2021. **Fullständig titel:** SQL for Data Analysis: Advanced Techniques for Transforming Data into Insights.

Boken visar hur SQL kan besvara analysfrågor, bland annat med time series analysis och cohort analysis. Den kopplar queries till vad analysen ska visa.

- **Användning:** SQL-stöd i kurs 03. Hjälper traineerna att skriva queries från metric definitions och analytical models i kurs 04–05.
- **Lästeman:** data transformation, aggregation, window functions och jämförelser över tid. Anpassa uppgifterna till traineernas SQL-nivå.
- **Begränsning:** ersätter inte SQL-grunder för nybörjare, Python, testning eller pålitliga data pipelines. Anpassa SQL dialect och funktioner till labbmiljön.
- **Bokinformation:** [O'Reilly](https://www.oreilly.com/library/view/sql-for-data/9781492088776/).

### The Data Warehouse Toolkit

**Författare:** Ralph Kimball och Margy Ross. **Förlag och referensutgåva:** Wiley, tredje upplagan, 2013. **Fullständig titel:** The Data Warehouse Toolkit: The Definitive Guide to Dimensional Modeling.

Boken beskriver dimensional modelling utifrån en business process. Den visar hur man väljer grain, facts och dimensions samt arbetar med conformed dimensions och history handling.

- **Användning:** huvudreferens för Kimball, star schema och SCD i kurs 05. Stöd för metrics och grain i kurs 04.
- **Lästeman:** grundstegen i dimensional modelling, fact tables, dimensions, additivity, bus matrix och history handling. Välj ett retail-exempel som passar vårt case.
- **Begränsning:** principerna behöver provas i den valda miljön. Boken är inte en aktuell produktguide till cloud data warehouses, Delta eller lakehouse.
- **Bokinformation och rättelser:** [Kimball Group](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/books/data-warehouse-dw-toolkit/).

### Storytelling with Data

**Författare:** Cole Nussbaumer Knaflic. **Förlag och referensutgåva:** Wiley, första upplagan, 2015. **Fullständig titel:** Storytelling with Data: A Data Visualization Guide for Business Professionals.

Boken visar hur man presenterar data tydligt för en business audience. Den tar upp context, chart selection, visual design och storytelling för att göra budskapet lätt att förstå.

- **Användning:** huvudreferens för kommunikation i kurs 06. Stöd för att förstå målgruppen i kurs 02.
- **Lästeman:** förstå mottagaren, välja charts, minska clutter, rikta uppmärksamheten och bygga en tydlig narrative.
- **Begränsning:** en övertygande presentation behöver inte vara korrekt. Kursen behöver egna övningar om uncertainty, causality, risk och assumptions.
- **Bokinformation:** [författarens boköversikt](https://www.storytellingwithdata.com/books). Förslaget gäller originalboken, inte de andra övnings- eller presentationsböckerna.

### Designing Data-Intensive Applications

**Författare för referensutgåvan:** Martin Kleppmann. **Förlag och referensutgåva:** O'Reilly, första upplagan, 2017.

Boken förklarar reliability, scalability och maintainability i datasystem. Den använder data models, storage, replication, partitioning, transactions samt batch och stream processing för att förklara tekniska trade-offs.

- **Användning:** fördjupning i kurs 01, 03 och 05 för att motivera teknikval, inte bara följa instruktioner.
- **Lästeman:** reliability, data models, storage och transactions först. Distributed systems och stream processing senare, vid behov.
- **Begränsning:** delar är avancerade för nybörjare och ligger utanför grundprogrammets scope. Boken lär inte ut programmeringsgrunder eller Kimball dimensional modelling.
- **Bokinformation:** [bokens webbplats](https://dataintensive.net/).

Förslaget utgår från första upplagan. Det betyder inte att den är den senaste. Om en annan upplaga väljs behöver författaruppgifter och läshänvisningar uppdateras före kursstart.

### NoSQL Distilled

**Prioritering: valbar och möjlig att stryka.** Behåll boken om gruppen behöver lära sig mer om non-relational databases. Boken behövs inte för grundprogrammets övningar.

**Författare:** Pramod J. Sadalage och Martin Fowler. **Förlag och referensutgåva:** Addison-Wesley, första upplagan. **Fullständig titel:** NoSQL Distilled: A Brief Guide to the Emerging World of Polyglot Persistence.

Boken introducerar key-value, document, column-family och graph databases. Den tar upp data models, distribution, consistency och polyglot persistence: att använda olika lagringstekniker för olika behov.

- **Användning:** valbar breddning i kurs 01 och stöd för att jämföra storage options i kurs 05.
- **Lästeman:** databasfamiljer, modelling utifrån access patterns, consistency och storage choices.
- **Begränsning:** produktbeskrivningarna är äldre. Läs även aktuell dokumentation. Column-family databases är inte samma sak som columnar storage i analytics engines. NoSQL ersätter inte data modelling.
- **Bokinformation:** [Martin Fowler](https://martinfowler.com/books/nosql.html) och [förlagets boksida](https://www.informit.com/store/nosql-distilled-a-brief-guide-to-the-emerging-world-9780321826626).

## Koppling till de sex kurserna

**Direkt stöd** betyder att boken tar upp kursens ämnen, inte att den ensam täcker kursen. **Indirekt stöd** ger bakgrund men behöver kompletteras med kursmaterial.

| Kurs | Fundamentals of Data Engineering | The Data Warehouse Toolkit | Designing Data-Intensive Applications | NoSQL Distilled |
| --- | --- | --- | --- | --- |
| [01: Database Foundations](../courses/01-database-foundations/README.md) | Direkt stöd: source systems, storage och rollen som data engineer | Indirekt stöd: operational kontra analytical model | Direkt stöd: data models, storage och transactions; välj enkla delar | Direkt stöd: valbar breddning till non-relational models |
| [02: Business 101](../courses/02-business-101/README.md) | Indirekt stöd: business needs och användare | Indirekt stöd: business processes och samarbete med stakeholders | Begränsat stöd för value chains och KPI trees | Begränsat stöd för kursens business objectives |
| [03: SQL + Python for DE](../courses/03-sql-python-for-de/README.md) | Direkt stöd: ingestion, transformation och pålitliga data pipelines | Direkt stöd: ETL och loading av dimensional models | Direkt stöd: principer för batch och stream processing; fördjupning | Indirekt stöd: data models och schema migrations |
| [04: Business 102](../courses/04-business-102/README.md) | Indirekt stöd: från business needs till requirements | Direkt stöd: grain, facts och measure additivity | Indirekt stöd: trade-offs kring reliability och consistency | Indirekt stöd: requirements för access patterns och consistency |
| [05: Data Modelling + DW / Lakehouse](../courses/05-data-modelling-dw-lakehouse/README.md) | Direkt stöd: architecture, storage och transformation | Direkt stöd och huvudreferens: Kimball, star schema, dimensions och history handling | Direkt stöd: system- och storage trade-offs, inte Kimball | Direkt stöd: jämföra non-relational options, inte dimensional modelling |
| [06: Business 103](../courses/06-business-103/README.md) | Indirekt stöd: värde och serving till användare | Indirekt stöd: hur modellen besvarar business questions | Indirekt stöd: förklara tekniska risker och begränsningar | Indirekt stöd: motivera teknikval och följder |

SQL och kommunikation får mer direkt stöd av dessa två böcker:

| Kurs | SQL for Data Analysis | Storytelling with Data |
| --- | --- | --- |
| [01: Database Foundations](../courses/01-database-foundations/README.md) | Direkt stöd: SQL queries efter introduktionen | Begränsat stöd för databasgrunder |
| [02: Business 101](../courses/02-business-101/README.md) | Indirekt stöd: göra business questions möjliga att analysera | Indirekt stöd: målgrupp, context och budskap |
| [03: SQL + Python for DE](../courses/03-sql-python-for-de/README.md) | Direkt stöd: transformation, aggregation och analytical SQL; inte Python | Indirekt stöd: förklara analysresultat |
| [04: Business 102](../courses/04-business-102/README.md) | Direkt stöd: från metric definitions till queries; ersätter inte requirements eller SLA | Indirekt stöd: klargöra frågan och användningen |
| [05: Data Modelling + DW / Lakehouse](../courses/05-data-modelling-dw-lakehouse/README.md) | Direkt stöd: analytical queries mot modellen, inte Kimball | Indirekt stöd: presentera analysresultat |
| [06: Business 103](../courses/06-business-103/README.md) | Indirekt stöd: spårbara siffror till en decision brief | Direkt stöd och huvudreferens: data visualization, fokus och narrative |

Ingen bok täcker hela business-spåret: value chains, KPI trees, metric definitions, SLA och decision-oriented presentation. Storytelling with Data stärker kommunikationen, men business-kurserna behöver egna exempel, workshops och business reviewers. SQL/Python behöver också praktiska övningar.

## Föreslagen läsordning och övningar

| När | Läsning | Kort aktivitet i vårt retail case |
| --- | --- | --- |
| Inledning och kurs 01 | Valda delar av Fundamentals of Data Engineering; NoSQL Distilled om den behålls | Rita datans väg från orderkälla till beslut. Motivera en första storage model. |
| Kurs 03 | SQL for Data Analysis om transformation och analys; Fundamentals of Data Engineering om ingestion; valda principer ur Designing Data-Intensive Applications | Beräkna en metric med SQL. Förklara hur koden hanterar duplicates och omkörningar. Visa det med tester. |
| Kurs 04–05 | The Data Warehouse Toolkit om grain, facts, dimensions och history handling | Granska en metric definition, välj fact grain och visa varför en join inte ger double counting. |
| Kurs 06 | Storytelling with Data om målgrupp, chart selection och narrative | Förbättra en presentation av vårt retail case. Motivera ändringarna utan att dölja uncertainty, risker eller assumptions. |
| Efter grunderna eller som fördjupning | Valda delar av Designing Data-Intensive Applications; NoSQL Distilled om den behålls och behövs | Jämför två lösningar utifrån access patterns, consistency, complexity och cost. Presentera assumptions och risker. |

Kursansvariga väljer korta läspaket och diskussionsfrågor när tidsbudgeten är klar. Ange kapitel och sidor först när upplagorna har valts. Bedöm hur läsningen används i övningarna, inte hur många sidor deltagaren har läst.

## Relation till certifieringarna

- **DP-900:** böckerna ger stöd för data concepts, storage och analytics options. Läs Microsoft Learn för aktuella Azure-tjänster och provmål.
- **DP-750:** böckerna ger principer för data modelling, transformation och reliability. De ersätter inte Databricks-labbar eller dokumentation om Unity Catalog, Lakeflow, access control, deployment och monitoring.

Se [certifieringsöversikten](azure-certifications.md) för vad kurserna ger och vilka extra förberedelser som behövs.

## Beslut före införande

- Bestäm upplagor, läspaket och rimlig lästid.
- Ordna tillgång via inköp eller en licensierad biblioteks- eller e-bokstjänst.
- Använd egna övningar och länkar till lagliga källor; lägg inte in bokkapitel eller otillåtna kopior i repot.
- Följ upp nyttan i piloten. Anpassa läsningen efter förkunskaper och feedback.
