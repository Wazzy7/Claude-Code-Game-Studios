<!-- PROTOTYPE - NOT FOR PRODUCTION -->
<!-- Question: Voelt minion-sturen (counters kiezen) + de oplopende Bloedstreak actief en krachtig, of is het toekijken? -->
<!-- Date: 2026-11-01 -->

# Concept Prototype Report: Warlord's Tide

> **Date**: 2026-11-01
> **Prototype Path**: HTML
> **Concept File**: design/gdd/game-concept.md

---

## Hypothesis

Als de speler minion-kaarten tikt om vijandelijke golven te counteren, voelt dat
actief en krachtig — we weten dat het waar is als een testspeler binnen 3 minuten
(a) minstens één 7-kill-streak haalt, (b) zelf een minion-type kiest op basis van
de vijand, en (c) na afloop direct opnieuw wil beginnen.

---

## Riskiest Assumption Tested

"Minion-keuze en timing maken voelbaar uit (het is geen toekijken)." Uit het
concept (Design Risks: "Te passief").

**Uitkomst: niet bewezen.** De speler koos de juiste counter in 31% van de
tikken, gelijk aan willekeurig (33%). Bots bevestigen het: willekeurig mixen
werkt bijna even goed als gericht counteren; alleen één type spammen verliest.

---

## Approach

Eén zelfstandig HTML-bestand, portret, touch. Eén lane, drie minion-kaarten
(Zwaard/Boog/Schild) met zelf-opladende essentie, drie vijandtypes met counters
(Brute/Zwaard, Vlieger/Boog, Zwerm/Schild; 2,5× schade bij counter, 0,1× anders),
Bloedstreak met drempels 3 (Goudregen ×2), 7 (Botgolem), 15 (Schaduwdraak), en
een scorekaart die de hypothese meet. Ongeveer een middag werk inclusief
bot-afstemming.

**Path chosen:** HTML
**Reason for path:** de hypothese gaat over keuzes en streak-escalatie, niet over
frame-precieze timing; Godot was niet beschikbaar in de bouwomgeving, en HTML is
direct op de telefoon speelbaar.

**Shortcuts taken (intentional):**
- Alle waarden hardcoded; geen architectuur
- Vormen in plaats van art, geen geluid, geen menu's
- Geen champion: de streak reset wanneer een vijand de burcht bereikt (afwijking van het concept, waar championdood de streak reset)
- Geen edelstenen, upgrades of meerdere levels

---

## Result

**Bot-afstemming (vóór de menselijke test).** Met de eerste waarden won een
willekeurig kiezende bot én een bot die alleen zwaarden stuurde, zonder één lek:
de keuze deed niets. Na sterkere vijanden en scherpere counters (20 runs per bot):
slimme bot 10/20 gewonnen, willekeurig 7/20, alleen-zwaard 0/20.

**Menselijke test (1 speler, de ontwerper, op iPhone via een claude.ai-artifact).**
Scorekaart van een gespeelde slag: hoogste streak 61, 7-streak na 21 s, goede
counter-keuzes 13/42 (31%), 67 kills, 1 Botgolem, 1 Schaduwdraak, 770 goud,
burcht gevallen na 70 s.

- **Beste moment:** "De draak die alles wegvaagde."
- **Slechtste moment:** "Burcht ging ineens snel onderuit" — oorzaak: te veel vijanden tegelijk.
- **Verrassingen:** geen.
- **Opnieuw spelen:** "wou er na iets upgraden om wel nog een slag te doen maar sterker."
- **Bewust counteren:** "niet".

---

## Metrics

| Metric | Value |
|--------|-------|
| Path used | HTML |
| Iterations to playable | N/A |
| Prototype duration | ~een middag (bouwen + bot-afstemming) |
| Playtesters | 1 intern (de ontwerper), 0 extern; plus bot-simulaties (3 strategieën × 20 runs) |
| Feel assessment | Draak/streak-escalatie voelt als hoogtepunt; counter-keuze voelt niet als keuze (31% correct ≈ willekeurig); moeilijkheid stort na ~60 s in binnen enkele seconden. Impact-feel op een echte telefoon in Godot niet getoetst (browser). |
| Hypothesis verdict | PARTIALLY CONFIRMED — (a) ja, (b) nee, (c) ja, maar alleen met een upgrade ertussen |

---

## Recommendation: PROCEED

De kern van het concept — streak-escalatie die uitmondt in een spektakelmoment
(de Schaduwdraak) — werkt: de 7-streak kwam binnen 21 seconden, de draak was het
beste moment, en de speler wilde terug. Wat niet werkte is de counter-keuze als
bron van actieve besluitvorming (31% correct, gelijk aan willekeurig, ook bij
bots), en de terugkeerdrang hangt aan progressie (upgraden) in plaats van aan
"het nu beter doen". Dat zijn ontwerpproblemen die in de GDD's op te lossen zijn,
geen reden om de kern te verlaten. Kanttekening: één tester die de ontwerper zelf
is, en een browserprototype — dit valideert interesse, geen feel op het doelapparaat.

---

## If Proceeding

- **Core tuning values discovered:**
  - Streakdrempels 3/7/15 zijn bereikbaar: 7 na ~21 s, 15 ruim binnen een slag.
  - Zwakke counter-modifiers (2× / 0,5×) maken de keuze betekenisloos; ook 2,5× / 0,1× liet willekeurig mixen nog ~70% van de slimme score halen.
  - Een spawn-interval dat lineair krimpt (1,5 s → 0,9 s plus ruis) zonder rustmomenten geeft een plotselinge instorting rond 60–70 s.
- **Assumptions confirmed:**
  - *De streak is koning* (pijler 2): escalerende beloningen met een spektakelmoment werken.
  - *Elke slag maakt je sterker* (pijler 5): de speler vroeg zelf om upgrades tussen slagen.
- **Assumptions disproved:**
  - Dat drie minion-types met counters vanzelf tot bewuste keuzes leiden. Zonder leesbaarheid en zonder gewicht kiest de speler niet; willekeurig mixen is voldoende.
- **Emergent mechanics:**
  - De wens om tussen slagen te upgraden ontstond zonder dat het prototype upgrades had — bevestigt de meta-loop als terugkeerhaak.

**Ontwerprichtingen voor de GDD's:**
1. Edelsteen-upgrades tussen slagen zijn MVP (staat al in het concept; nu bevestigd).
2. Counters óf leesbaar en zwaarwegend maken (duidelijke vijandsilhouetten, counter-hint op de kaart, een vijand die alleen door zijn counter te verslaan is) óf naar de achtergrond schuiven en de keuze elders leggen (timing van grote acties).
3. Moeilijkheid in golven met adempauzes en een zichtbare waarschuwing vóór een zware golf, in plaats van een steeds snellere spawn.
4. Meer momenten zoals de draak: grote, schermvullende beloningen zijn het sterkste gevoel.

> Note: HTML path; feel op het doelapparaat is onzeker. Overweeg in de vertical
> slice een Godot-build gericht op impact-feel op een echte telefoon.

**Next steps:**
1. `/design-review design/gdd/game-concept.md`
2. `/gate-check`
3. `/map-systems`
4. `/design-system [mechanic]` (use learnings in Tuning Knobs and Formulas sections)

---

## If Pivoting

N.v.t. — verdict is PROCEED.

---

## If Killing

N.v.t. — verdict is PROCEED.

---

## Lessons Learned

- **What assumptions were broken by actually building this?**
  Dat een counter-driehoek vanzelf een keuze oplevert. De eerste afstelling was zo
  ruim dat zelfs één type spammen won; ook na afstemming bleef willekeurig mixen
  bijna even goed.

- **What surprised us that didn't show up in the brainstorm?**
  Dat de terugkeerdrang direct naar upgraden wees, nog vóór er een upgrade-systeem
  bestond.

- **What would we test differently next time?**
  Externe testers zonder uitleg (niet alleen de ontwerper); de counter-leesbaarheid
  apart testen (zag de speler welk vijandtype het was?); en vastleggen hoeveel
  slagen iemand vrijwillig speelt in plaats van het zelf te laten invullen.

---

> *Prototype code location: `prototypes/warlords-tide-concept/`*
> *This code is throwaway. Never refactor into production.*
