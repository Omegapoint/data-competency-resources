# 06: Business 103 - Decision-oriented Presentation, Impact och Risk

[Programkatalog](../../README.md) | Föregående: [Data Modelling + DW / Lakehouse](../05-data-modelling-dw-lakehouse/README.md)

**Status:** utkast till kursöversikt.

## Syfte

Presentera analysresultat så att en stakeholder kan fatta ett välgrundat beslut. Fokusera på åtgärd, impact, confidence och begränsningar, inte på en genomgång av all teknik.

## Förkunskaper

Kurserna 01-05 eller motsvarande erfarenhet. Ta med kontrollerade analysresultat, requirements och metric definitions.

## Lärandemål

APP ska kunna:

- Inleda med beslutet och rekommendationen.
- Välja underlag och data visualizations som passar målgruppen.
- Förklara möjlig impact utan att lova mer precision eller säkrare causality än data stöder.
- Ange assumptions, risker, begränsningar och andra möjliga tolkningar.
- Avsluta med en tydlig call to action, ansvarig och nästa steg.
- Förklara residual risk och ange vem som har mandat att besluta om fortsatt användning.

## Centrala begrepp

| Område | Begrepp att introducera |
| --- | --- |
| Decision narrative | Context, fråga, underlag, alternativ, rekommendation, call to action |
| Presentation | Målgruppsanpassat språk, chart selection, units, jämförelser, reporting period |
| Impact | Baseline, expected benefit, cost, feasibility, scenario estimates |
| Confidence | Data coverage, data quality, data freshness, uncertainty, correlation kontra causality |
| Risk och assumptions | Sensitivity, operational risk, saknat underlag, reversibility |
| Follow-up | Decision owner, nästa steg, success metric, tid för uppföljning |
| Risk acceptance | Residual risk är risken som finns kvar efter åtgärder. Beskriv impact, alternativ, risk owner, beslutsmandat, villkor och review date. Ett riskbeslut får inte åsidosätta policy eller lagkrav. |

## Praktiskt arbete

Skriv en decision brief till operations manager i [vårt gemensamma retail case](../../docs/shared-case-and-assessment.md). Använd den testade modellen för att rekommendera en åtgärd kring leveranser eller returer. Skilj observationer från hypoteser. Beskriv vilket underlag som behövs innan verksamheten gör en större investering.

Förklara vilka data quality-problem som finns kvar och hur de påverkar confidence och rekommendationen.

Använd er [governance brief](../../templates/governance-brief-template.md) för att visa kvarvarande risk, föreslagen åtgärd och vem som behöver fatta beslut. Genomför en rollspelsreview: dokumentera godkännande, avslag eller behov av escalation, med villkor och review date. Skilj ett faktiskt beslut i övningen från APP:s egen rekommendation.

## Bedömningsunderlag

- En kort decision brief eller presentation med beslutet och rekommendationen först.
- Några diagram eller tabeller som går att spåra till testade queries och metric definitions.
- En bedömning av impact med tydliga assumptions. Märk uppskattningar som scenarier när underlaget är osäkert.
- Risker, begränsningar, alternativ och en call to action.
- Svar på granskarnas frågor, även om vad data inte kan visa.
- Ett riskbeslut från rollspelet med ansvarig beslutsfattare, mandat, villkor och review date, eller tydlig escalation om beslut inte kan fattas.

Använd [den gemensamma bedömningsmatrisen](../../docs/shared-case-and-assessment.md#bedömningsmatris). Presentationen måste stämma med tekniska specifikationer och metric definitions.

## Planering

- Ansvarig, tid och format: inte bestämt.
- Miljö: tidigare resultat och en review med stakeholders.
- Material att ta fram: målgruppsbeskrivning, presentationsexempel och kriterier för feedback.
