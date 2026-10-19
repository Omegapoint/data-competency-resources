# Azure-certifieringar: DP-900 och DP-750

[Programkatalog](../README.md) | [Stakeholder brief](stakeholder-brief.md)

**Status: förslag till extra certifieringsspår.** Fakta kontrollerades mot Microsoft Learn den 19 oktober 2026. Kurskopplingarna är vår bedömning, inte en officiell bedömning eller garanti för godkänt prov.

## Kort sammanfattning för stakeholders

- **DP-900 ger bredd:** core data concepts och en översikt av Azure data services. Ett möjligt tidigt delmål med ett extra Azure-block.
- **DP-750 ger fördjupning:** praktisk data engineering i Azure Databricks. Ett möjligt senare delmål efter teknikkurserna och extra Databricks-labbar.
- **Business-kurserna tillför annat:** value chains, KPIs, requirements och decision-oriented presentation ersätts inte av certifieringarna.
- Grundprogrammet är fortsatt plattformsneutralt. Certifieringsspåren är förslag, inte nya krav.

DP-900 och DP-750 är provkoder. De hör till certifieringarna nedan. DP-750 gäller Azure Databricks och ska inte förväxlas med DP-700, som gäller Microsoft Fabric.

## DP-900: Microsoft Azure Data Fundamentals

**Certifiering:** Microsoft Certified: Azure Data Fundamentals.

Provet passar personer som börjar arbeta med data i molnet. Det handlar om att förklara begrepp och välja lämpliga tjänster, inte om avancerad programmering eller självständigt arbete i produktion.

Enligt [Microsofts studieguide för DP-900](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/dp-900), med målområden från den 21 juli 2026:

| Målområde | Andel av provet |
| --- | --- |
| Core data concepts | 25–30 % |
| Relational data i Azure | 20–25 % |
| Non-relational data i Azure | 15–20 % |
| Analytics workloads i Azure | 25–30 % |

**Placering:** efter kurs 01, en introduktion till analysbegreppen i kurs 05 och ett extra Azure-block. Provet behöver inte vänta tills hela programmet är klart. DP-900 är inte ett formellt förkunskapskrav för andra rollbaserade Azure-certifieringar.

**Behöver läggas till:** Azure SQL-familjen och tjänster för open-source databases; Blob Storage, Files, Table Storage och Cosmos DB; batch kontra streaming; en översikt av Azure Databricks, Microsoft Fabric och Power BI. Grundkurserna går inte igenom alla dessa tjänster.

## DP-750: Implementing Data Engineering Solutions Using Azure Databricks

**Certifiering:** Microsoft Certified: Azure Databricks Data Engineer Associate.

Provet handlar om att konfigurera, säkra, bygga och underhålla lösningar i Azure Databricks. Microsoft räknar med praktisk erfarenhet av SQL, Python, Git, data quality och data governance. Deltagaren behöver också känna till Microsoft Entra, Azure Data Factory och Azure Monitor.

Enligt [Microsofts studieguide för DP-750](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/dp-750), med målområden från den 19 oktober 2026:

| Målområde | Andel av provet |
| --- | --- |
| Setup och configuration av Azure Databricks | 15–20 % |
| Security och governance för Unity Catalog objects | 15–20 % |
| Data preparation och processing | 30–35 % |
| Deployment och maintenance av data pipelines och workloads | 30–35 % |

**Placering:** ett senare, valbart mål efter främst kurserna 03 och 05. Grundprogrammet räcker inte som DP-750-förberedelse. Stora delar av environment setup, security, orchestration och drift ingår inte.

**Behöver läggas till:** Spark/PySpark och Delta tables; compute; Unity Catalog och access control; identities och secrets; Lakeflow Connect, Auto Loader och streaming ingestion; Lakeflow Spark Declarative Pipelines och Jobs; deployment med Declarative Automation Bundles; monitoring, troubleshooting samt performance och cost optimization.

Grundprogrammets [governance-spår](shared-case-and-assessment.md#governance-genom-hela-caset) ger roller, regler, metadata, lineage och enkla access-tester. Det ersätter inte implementation av Unity Catalog, plattformsspecifika policies, audit logging eller automatiserad retention i Databricks.

## Koppling till de sex kurserna

**Direkt grund** betyder att kursen tar upp sådant som återkommer i provet, inte att hela området täcks. **Indirekt stöd** ger sammanhang men ersätter inte provförberedelser.

| Kurs | DP-900 | DP-750 |
| --- | --- | --- |
| [01: Data Fundamentals](../courses/01-data-fundamentals/README.md) | Direkt grund: data concepts, file formats, relational och non-relational storage, workloads och enkel SQL. Lägg till Azure-tjänster och mer om analytics. | Direkt grund: data types, integrity, data quality, ownership och lineage. Lägg till Delta, Unity Catalog och praktisk användning i Databricks. |
| [02: Business 101](../courses/02-business-101/README.md) | Indirekt stöd: use cases och roller. Value chains och KPI trees är inte egna provområden. | Indirekt stöd: business needs bakom lösningen. Business understanding är inget eget provområde. |
| [03: SQL + Python for DE](../courses/03-sql-python-for-de/README.md) | Direkt grund: SQL och data processing. Python-delen går längre än provets begreppsnivå. | Direkt grund: transformations, ingestion, data quality, tester och Git. Lägg till Spark, Databricks-verktyg och deployment. |
| [04: Business 102](../courses/04-business-102/README.md) | Indirekt stöd: välja lösning efter behov. Detaljerade metric definitions och SLA är inte egna provområden. | Direkt grund: grain och data quality requirements. Övrig requirements framing ger indirekt stöd. Lägg till implementation och monitoring. |
| [05: Data Modelling + DW / Lakehouse](../courses/05-data-modelling-dw-lakehouse/README.md) | Direkt grund: analytical storage, ingestion och processing. Lägg till Azure-tjänster, real-time analytics och Power BI. | Direkt grund: data modelling, SCD, grain och history handling. Lägg till Delta, Unity Catalog, physical optimization och ingestion i Databricks. |
| [06: Business 103](../courses/06-business-103/README.md) | Indirekt stöd: data visualization. Power BI behöver tas upp separat. Decision narrative och impact går utöver provet. | Indirekt stöd: förklara impact, risk och cost. Decision-oriented presentation är inget eget provområde. |

## Förslag till kompletterande aktiviteter

| Spår | Kort aktivitet | Resultat att följa upp |
| --- | --- | --- |
| DP-900 | Jämför Azure-tjänster för relational data, dokument, filer och analys i vårt retail case. | Motiverade tjänsteval och lista över kunskapsluckor mot studieguiden. |
| DP-750 | Bygg samma case i Azure Databricks med syntetiska data, access control, data quality tests och schemalagda jobs. Öva streaming ingestion, deployment och troubleshooting. | Lösning som går att köra om, dokumenterade permissions, testresultat och exempel på error handling och monitoring. |

Använd Microsofts officiella practice assessments för att hitta kunskapsluckor. En labb täcker inte hela provet. Bestäm miljö, access, budget och handledning innan Databricks-spåret startar.

**Rekommendation:** använd DP-900 som ett möjligt tidigt delmål och DP-750 som en senare specialisering om kommande uppdrag använder Azure Databricks. Behåll programmets praktiska bedömning och business-kurser oavsett certifieringsval.

## Officiella källor

- [Microsoft Certified: Azure Data Fundamentals](https://learn.microsoft.com/en-us/credentials/certifications/azure-data-fundamentals/)
- [Studieguide för DP-900](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/dp-900)
- [Microsoft Certified: Azure Databricks Data Engineer Associate](https://learn.microsoft.com/en-us/credentials/certifications/implementing-data-engineering-solutions-using-azure-databricks/)
- [Studieguide för DP-750](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/dp-750)

Kontrollera alltid aktuell studieguide och provinformation före planering och bokning; innehåll och produktnamn kan ändras.
