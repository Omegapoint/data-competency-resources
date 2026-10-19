# Governance Brief: [namn på data product]

[Programkatalog](../README.md) | [Gemensamt case och bedömning](../docs/shared-case-and-assessment.md)

**Status:** utkast för övning. Ange version, datum och ansvarig. Ersätt instruktionerna nedan och uppdatera länkar om mallen kopieras.

Briefen byggs genom de sex kurserna. Den visar vem som bestämmer, vilka regler som gäller och hur de följs upp. En enkel Markdown-fil räcker; inget catalog-verktyg krävs. Använd bara syntetiska data.

Regler, mandat och retention-perioder kommer från utbildarens fiktiva policy. Märk preliminära förslag och öppna frågor. Ett godkännande i rollspelet är inte ett godkännande för produktion eller en juridisk bedömning.

## 1. Syfte och scope

- Vilken business question och vilket beslut ska data stödja?
- Vilka datasets, metrics, användare och användningsområden ingår?
- Vad får data inte användas eller delas för?

## 2. Roller och decision rights

| Roll | Ansvarig i övningen | Ansvar och beslut inom mandatet |
| --- | --- | --- |
| Data owner | Ange roll/person | Ansvarar för användning och data requirements; godkänner access enligt policy |
| Data steward | Ange roll/person | Håller definitioner och metadata uppdaterade; samordnar quality issues |
| Technical owner | Ange roll/person | Implementerar kontroller, access och felhantering; dokumenterar tekniska ändringar |
| Metric owner | Ange roll/person | Ansvarar för metric definitions och godkänner ändringar |
| Risk owner / approver | Ange roll/person och mandat | Hanterar kvarvarande risk; anger vad rollen får acceptera och vad som måste eskaleras |

Ange kontaktväg vid oenighet och vem som tar policy-, security- eller privacy-frågor. Roller kan kombineras, men mandat måste vara tydligt.

## 3. Classification, metadata och lineage

| Dataset eller fält | Classification enligt övningens policy | Tillåten användning/delning | Data owner | Source of truth |
| --- | --- | --- | --- | --- |
| Ange dataset/fält | Ange klass och motivering | Ange begränsningar | Ange owner | Ange källa |

Länka till data dictionary med definitioner, data types, grain och metric definitions. Rita enkel lineage från source genom transformations till rapport och exports. Ange vilka pipelines och användare som beror på data.

## 4. Access lifecycle

| Data och roll | Tillåten access och syfte | Request och approver | Tilldelas av | Review och revocation | Evidence |
| --- | --- | --- | --- | --- | --- |
| Ange dataset och testroll | Ange minsta nödvändiga access | Ange flöde och mandat | Ange ansvarig | Ange intervall/slutdatum och vem som tar bort access | Länka beslut och testresultat |

Testa både tillåten och nekad läsning samt att borttagen access inte längre fungerar. Beskriv även åtkomst till logs och rejected records. Skilj dokumenterade krav från faktiskt testade kontroller.

## 5. Retention och deletion

| Data eller kopia | Retention och startpunkt | Regelkälla och approver | Deletion-metod och ansvarig | Verifiering och begränsningar |
| --- | --- | --- | --- | --- |
| Ange source, layer, export eller annan kopia | Ange period och när den börjar räknas | Hänvisa till fiktiv policy | Ange åtgärd och ansvar | Beskriv evidence eller vad som ännu inte är implementerat |

Ta med downstream data och relevanta logs, rejected records och backups. Beskriv hur kvarvarande kopior hanteras enligt policy. Föreslå inte att en raderad source-rad automatiskt tar bort alla kopior.

## 6. Quality rules och issue management

| Regel och quality dimension | Kontroll och target | Vid fel: stoppa, avvisa eller varna | Ansvarig, responstid och escalation | Evidence |
| --- | --- | --- | --- | --- |
| Ange regel | Ange test och gränsvärde | Ange tydligt beteende | Ange kontaktväg och nästa nivå | Länka test eller run ID |

Dokumentera ett issue: berörda data, impact, severity, upptäckt, ansvarig, åtgärd, status och hur lösningen verifieras. Lägg inte känsliga värden eller credentials i evidence.

## 7. Change control och audit evidence

| Ändring och skäl | Downstream impact | Approver och beslut | Tester och kod-/definitionsversion | Kommunikation och datum |
| --- | --- | --- | --- | --- |
| Ange schema-, metric- eller accessändring | Ange pipelines, rapporter och användare | Ange beslut eller öppen fråga | Länka evidence | Ange mottagare och när ändringen gäller |

Spara beslut om access, ändringar och undantag med datum, beslutsfattare och skäl. För körningar: ange run ID, version och testresultat. Detta är enkel audit evidence i labben, inte fullständig production audit logging.

## 8. Residual risk och beslut

| Risk och impact | Åtgärd och alternativ | Risk owner och approver med mandat | Beslut eller escalation | Villkor och review date |
| --- | --- | --- | --- | --- |
| Ange kvarvarande risk | Ange möjliga åtgärder | Ange vem som får besluta | Ange godkännande, avslag eller nästa steg | Ange villkor, ansvarig och tid för uppföljning |

Ingen får acceptera risk utanför sitt mandat eller åsidosätta policy eller lagkrav. Om beslut saknas ska det framgå; ett öppet issue är inte ett godkännande.
