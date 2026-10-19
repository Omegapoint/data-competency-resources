# Stakeholder Brief: APP-program för Data Engineers

[Programkatalog](../README.md)

**Status: diskussionsförslag.** Programmet är inte beslutat.

## Förslaget i en mening

Sex kurser som lär APP att gå från en business question till en pålitlig data product och en tydlig rekommendation.

## Varför kombinera verksamhet och teknik?

En korrekt SQL query kan besvara fel business question. En dashboard kan vilseleda om metrics är otydliga eller data kommer för sent. Programmet kombinerar teknik med business understanding så att APP lär sig att upptäcka och förklara sådana problem.

| Förmåga | Nytta för stakeholders | Kurser |
| --- | --- | --- |
| Pålitliga grunder | Förstå data types, storage, data quality, ownership och säkra databasändringar | Data Fundamentals |
| Business relevance | Identifiera beslut, stakeholders och metrics innan lösningen byggs | Business 101 |
| Repeatable delivery | Transformera data med tester i stället för manuella engångssteg | SQL + Python for DE |
| Gemensamma förväntningar | Enas om metric definitions, grain och när data ska finnas | Business 102 |
| Användbara analysdata | Göra data enkla att använda utan double counting | Data Modelling + DW / Lakehouse |
| Decision support | Förklara vad underlaget visar, vad som är osäkert och vilken åtgärd som föreslås | Business 103 |

## Förväntade färdigheter efter programmet

Efter programmet ska en APP med handledning kunna:

- Förklara en business question och vem som ska använda svaret.
- Definiera en metric, grain och testbara acceptance criteria.
- Bygga och testa en liten SQL/Python-transformation som går att köra om.
- Bygga en enkel dimensional model och förklara viktiga trade-offs.
- Presentera en rekommendation med spårbara siffror och tydliga begränsningar.
- Följa enkla governance-regler, dokumentera beslut och veta när en fråga måste eskaleras.

Detta är föreslagna lärandemål, inte ett löfte om självständigt arbete i produktion.

## Upplägg

- Följ [kursordningen](../README.md#kurskatalog) och uppdatera tidigare arbete när requirements blir tydligare.
- Använd ett [gemensamt retail case med syntetiska data](shared-case-and-assessment.md), inte sex fristående övningar.
- Kombinera begrepp, praktiskt arbete och feedback.
- Ta med en business reviewer i Business 101, 102 och 103, utöver tekniska reviewers.
- Bedöm inlämnat arbete och motiveringar till val, inte bara närvaro.

## Data governance i grundprogrammet

Governance följer de sex kurserna, inte en separat sjunde kurs. APP övar ownership och decision rights, classification, access lifecycle, retention/deletion, quality issues, change control och residual risk.

En [governance brief](../templates/governance-brief-template.md) samlar regler, ansvar och evidence för vårt case. Bedömningen omfattar rollspel om godkännande och escalation, enkla access-tester och review av downstream impact. Se [case och bedömning](shared-case-and-assessment.md#governance-genom-hela-caset).

Utbildaren behöver förbereda fiktiv policy och mandat. Programmet ger inte juridisk specialistkunskap eller ett komplett governance operating model. Plattformsspecifik catalog, policy automation och production audit logging behöver fortsatt fördjupning.

## Möjliga certifieringsspår

DP-900 (Azure Data Fundamentals) kan vara ett tidigt delmål med ett extra Azure-block. DP-750 (Azure Databricks Data Engineer Associate) kan bli en senare specialisering med fler Databricks-labbar. Certifieringarna ersätter inte business-kurserna eller den praktiska bedömningen.

Se [certifieringsöversikten](azure-certifications.md) för kurskopplingar och vad som behöver läggas till. Provkrav, budget och plattform är inte bestämda. Grundprogrammet är fortsatt plattformsneutralt.

## Föreslaget litteraturstöd

Fundamentals of Data Engineering ger en gemensam bas. SQL for Data Analysis stödjer SQL-övningarna och The Data Warehouse Toolkit är huvudreferens för dimensional modelling. Storytelling with Data stödjer kommunikationsdelen. Designing Data-Intensive Applications används för utvald teknisk fördjupning. NoSQL Distilled är valbar och kan strykas om tid eller budget inte räcker. Förslaget gäller utvalda avsnitt, inte sex hela böcker.

Se [litteraturöversikten](reading-list.md) för bokbeskrivningar, kurskopplingar och läsordning. Bestäm upplagor, lästid och tillgång till böcker före start.

## Utvärdering av en pilot

| Önskad nytta | Så kan den följas upp | Att tänka på |
| --- | --- | --- |
| Bättre koppling mellan business needs och data | Review av frågeställning, KPI definitions och acceptance criteria | Använd samma kriterier för alla |
| Starkare tekniska grunder | Inlämningar som går att köra igen och godkända data quality checks | En godkänd labb räcker inte för självständigt produktionsarbete |
| Bättre stakeholder communication | Business reviewer förstår beslut, rekommendation och begränsningar | Spara feedback, inte bara närvaro |
| Rimlig tidsåtgång | Tid för övningar, stödbehov och feedback från APP | Justera scope och tempo efter piloten |

Bestäm baseline och success criteria före piloten. Vi räknar ännu inte med några vinster i produktivitet, bemanning eller ekonomisk avkastning.

## Beslut som behövs före start

| Beslut | Föreslagna deltagare i beslutet | Nuvarande status |
| --- | --- | --- |
| Målgrupp och förkunskaper | Programsponsor och APP-ansvarig | Återstår att besluta |
| Scope, kursordning och tid | Programansvarig och kursansvariga | Ordning föreslagen; tid inte bestämd |
| Kapacitet för undervisning och granskning | Tekniska ledare och verksamhetsrepresentanter | Ansvariga och kapacitet inte tilldelade |
| Labbverktyg och access | Tekniska kursansvariga och plattformsteam | Plattformsneutralt förslag |
| Bedömningsnivå och success criteria för piloten | Programansvarig och reviewers | Utkast finns |
| Pilotgrupp och tidpunkt för start | Sponsor och APP-ansvarig | Återstår att besluta |

## Risker och motåtgärder

| Risk | Föreslagen motåtgärd |
| --- | --- |
| Varierande förkunskaper | Kartlägg förkunskaper och erbjud förberedande arbete |
| För mycket innehåll för tiden | Prova ett litet end-to-end case innan scope utökas |
| Business-kurserna blir frikopplad teori | Använd samma beslut och metrics i alla kurser |
| Verktygssetup tar fokus från lärandet | Förbered och testa en gemensam labbmiljö |
| Avslutad utbildning förväxlas med production readiness | Förklara gränserna och fortsätt med handledning i riktiga leveranser |
| Känsliga data hamnar i materialet | Använd bara syntetiska data; granska nya datasets innan de tas med |

## Föreslagen genomgång med stakeholders

1. Förklara problemet: bra teknik måste besvara rätt business question.
2. Visa de sex kurserna och vad APP lämnar in.
3. Visa hur vårt gemensamma case knyter ihop arbetet.
4. Diskutera tid, ansvar och öppna beslut.
5. Bestäm om programmet ska utvecklas och testas i en pilot.
