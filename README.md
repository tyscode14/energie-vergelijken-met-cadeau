# Energieactie-checker

Open checklist die beoordeelt of een **welkomstactie** bij een energiecontract u werkelijk iets oplevert. Zeven vragen, een score en een lijst met concrete bevindingen. Eén HTML-bestand, geen build, geen tracking, geen afhankelijkheden. Gemaakt door [energievergelijkenmetcadeau.nl](https://energievergelijkenmetcadeau.nl), MIT-licentie.

**Gebruik de checker:** https://tyscode14.github.io/energieactie-checker/

## Waarom deze tool bestaat

Sinds **1 januari 2026** mogen Nederlandse energieleveranciers onder de Energiewet **geen fysieke cadeaus** meer geven bij een energiecontract: geen televisies, tablets, spelcomputers of cadeaubonnen. Wat overblijft is geld — welkomstkorting, cashback of loyaliteitsbonus.

Die drie namen zijn geen marketing. Sinds **1 juni 2023** gelden er regels voor welke naam wanneer gebruikt mag worden, en die naam vertelt u precies wannéér u uw geld krijgt en of u het kwijtraakt als u eerder vertrekt:

| Naam | Wanneer krijgt u het | Kwijt bij tussentijds opzeggen? |
|---|---|---|
| Welkomstkorting | Uiterlijk bij de tweede termijnbetaling | Nee, u heeft het al |
| Cashback | Na een wachtperiode, meestal 30–90 dagen | Meestal wel |
| Loyaliteitsbonus | Aan het eind van het eerste contractjaar | Ja, volledig |

Vrijwel geen enkele vergelijkingssite legt dit uit. Deze tool codeert het.

## Wat de checker doet

- Signaleert wanneer de **naam niet klopt met de uitbetaling** — een korting die pas op de jaarafrekening komt mag geen welkomstkorting heten.
- Waarschuwt voor bedragen die u **kwijtraakt bij vertrek**.
- Controleert de **twaalfmaandenregel** voor oud-klanten.
- Let op of de korting **al in de getoonde jaarprijs** zit, de meest gemaakte rekenfout.
- Rekent de **nettowaarde over de looptijd** uit: actiewaarde min het prijsverschil maal het aantal jaren.

## Data

`data/regels.json` bevat de zes regels met ingangsdatum, toelichting en bron, plus indicatieve marktcijfers. De logica in de pagina leest die regels uit, zodat de beoordeling controleerbaar is in plaats van een black box.

De marktbedragen (cashback € 0–700, uitschieters tot € 850) zijn **indicatief** en gecontroleerd op 20 augustus 2026; ze wijzigen wekelijks.

## Geen juridisch advies

Dit is een samenvatting van publiek beschikbare regelgeving. De actievoorwaarden van de leverancier zijn altijd leidend.

## Licentie

MIT.
