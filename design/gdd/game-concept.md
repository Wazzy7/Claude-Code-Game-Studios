# Game Concept: Warlord's Tide

*Created: 2026-11-01*
*Status: Draft*

---

## Elevator Pitch

> Een mobiele lane-battler waarin je als duistere warlord minions en champions
> over het slagveld stuurt om vijandelijke burchten te verpletteren — en elke
> kill bouwt je Bloedstreak op tot een storm van goud, edelstenen en donkere
> magie.
>
> 10-secondentest: tik een minion-kaart, je leger stormt naar voren, vijanden
> spatten uiteen in goud, je streakmeter loopt vol tot er een draak uit de
> lucht valt.

---

## Core Identity

| Aspect | Detail |
| ---- | ---- |
| **Genre** | 2D lane-battler / strategie-lite met lichte progressie (upgrade-RPG) |
| **Platform** | Mobiel (iOS / Android), portretmodus, één-duim-bediening |
| **Target Audience** | Casual tot mid-core mobiele spelers — zie Target Player Profile |
| **Player Count** | Singleplayer |
| **Session Length** | 20–40 minuten (één rijk); een match duurt 2–3 minuten |
| **Monetization** | Nog niet bepaald (zie anti-pijlers: geen echt-geld-gokken, geen pay-to-progress-muur) |
| **Estimated Scope** | Medium (4–6 maanden, solo) — MVP in 2–4 weken |
| **Comparable Titles** | Mobiele lane-/tower-battlers; League of Legends (champions/minions/items); Call of Duty (scorestreaks) |

---

## Core Fantasy

Jij bent de warlord op de heuvel. Met één gebaar ontketen je een leger van
zwaardknechten, schaduwbogen en botschilden, en wanneer de slag op z'n
hoogtepunt is, roep je een champion of een Schaduwdraak op die de hele lane
verschroeit. Je begint klein, maar elke slag maakt je sterker, tot je de
Duistere Troon opeist.

De emotionele belofte: **escalerende macht**. Goed spelen wordt niet één keer
beloond, maar steeds harder — net zoals een killstreak in een shooter, maar dan
met een heel leger en een scherm dat ontploft in goud.

---

## Unique Hook

*"Zoals een mobiele lane-battler, EN OOK: je killstreak escaleert live van
Goudregen naar Botgolem naar Schaduwdraak — en de buit regent neer in
cascades van goud en edelstenen."*

De Bloedstreak is geen bijzaak maar de ruggengraat: hij bepaalt je
beloningen, je grootste momenten en je strategie (je champion in leven houden
betekent je streak beschermen).

---

## Player Experience Analysis (MDA Framework)

### Target Aesthetics (What the player FEELS)

| Aesthetic | Priority | How We Deliver It |
| ---- | ---- | ---- |
| **Sensation** (sensory pleasure) | 1 | Schermschud, botsplinters, goud- en edelsteenexplosies, streak-escalatie in beeld en geluid, haptiek |
| **Fantasy** (make-believe, role-playing) | 2 | De speler is een duistere warlord; champions met eigen identiteit; donker rijk om te veroveren |
| **Narrative** (drama, story arc) | 7 | Licht: lore per champion en per rijk, geen dialoogverhaal |
| **Challenge** (obstacle course, mastery) | 3 | Geleidelijk zwaardere levels, minion-counters, timing van champion en spreuken, langere streaks |
| **Fellowship** (social connection) | N/A | Singleplayer; geen sociale systemen in scope |
| **Discovery** (exploration, secrets) | 5 | Nieuwe champions, relikwieën en rijken ontgrendelen; lore-fragmenten |
| **Expression** (self-expression, creativity) | 6 | Keuze welke champion, items en upgrades je meeneemt |
| **Submission** (relaxation, comfort zone) | 4 | Korte matches, simpele bediening, geen energietimers, altijd "nog één slag" |

### Key Dynamics (Emergent player behaviors)

- Spelers gaan hun champion actief beschermen om hun Bloedstreak niet te verliezen.
- Spelers leren vijandtypes lezen en sturen de juiste minion als counter.
- Spelers sparen essentie op om een grote golf tegelijk los te laten bij een hoogtepunt.
- Spelers spelen oudere levels opnieuw om edelstenen te farmen voor een specifieke upgrade.
- Spelers jagen op hun eerste Schaduwdraak (15-streak) als persoonlijk record.

### Core Mechanics (Systems we build)

1. **Lane-gevecht met minion-sturing** — minions lopen automatisch over één lane; de speler kiest met kaarten welk type (⚔️ Zwaardknecht, 🏹 Schaduwboog, 🛡️ Botschild) wordt gestuurd, betaald met zelf-opladende donkere essentie. Typen counteren elkaar.
2. **Champion met ultieme spreuk** — één champion per match, met een opladende ultimate; de champion sterven = streak reset.
3. **Bloedstreak** — kills vullen een oplopende meter met drempelbeloningen (3: Goudregen, 7: Botgolem, 15: Schaduwdraak).
4. **Edelsteen-progressie** — edelstenen uit kills, streaks en buitkisten worden uitgegeven aan upgrades voor champions, minions en items.
5. **Rijkskaart met oplopende moeilijkheid** — levels per rijk, elk iets zwaarder, met een boss-burcht aan het einde; nieuwe micro-vaardigheden worden geleidelijk geïntroduceerd.

---

## Player Motivation Profile

### Primary Psychological Needs Served

| Need | How This Game Satisfies It | Strength |
| ---- | ---- | ---- |
| **Autonomy** (freedom, meaningful choice) | Welke minion wanneer, welke champion en items mee, welke upgrade eerst | Supporting |
| **Competence** (mastery, skill growth) | Langere streaks, eerder de draak halen, zwaardere levels verslaan, zichtbaar sterker worden | Core |
| **Relatedness** (connection, belonging) | Band met champions via hun lore en identiteit (verzamelgevoel) | Minimal |

### Player Type Appeal (Bartle Taxonomy)

- [x] **Achievers** (goal completion, collection, progression) — How: streak-records, rijken veroveren, alle upgrades en champions verzamelen
- [x] **Explorers** (discovery, understanding systems, finding secrets) — How: secundair; counters en synergieën ontdekken, lore van champions en rijken
- [ ] **Socializers** (relationships, cooperation, community) — How: niet in scope
- [ ] **Killers/Competitors** (domination, PvP, leaderboards) — How: niet in scope (geen PvP); de "destruction"-voldoening zit in het verpletteren van AI-legers

Quantic Foundry-motivaties: primair *Power* (sterker worden), *Completion* en
*Destruction*; secundair *Fantasy* en *Discovery*.

### Flow State Design

- **Onboarding curve**: level 1 speel je met alleen tikken op één minion-kaart; level 2 introduceert de tweede minion en de champion; level 3 de streakbeloningen. Eén nieuwe vaardigheid per level, nooit meer dan één tutorialscherm.
- **Difficulty scaling**: elk level iets sterkere of gemengdere vijandgolven; vanaf rijk 2 komen strategische micro-acties erbij (minion terugroepen, champion vooruit sturen, spreuk richten).
- **Feedback clarity**: streakmeter altijd in beeld; counters zijn visueel leesbaar (vijand flitst bij zwakte); edelsteen-teller en upgrade-niveau zichtbaar groeiend.
- **Recovery from failure**: een verloren slag duurt maximaal 3 minuten, je houdt de edelstenen die je verdiende, en er is altijd een upgrade binnen bereik. Direct opnieuw spelen zonder wachttijd.

---

## Core Loop

### Moment-to-Moment (30 seconds)

Donkere essentie laadt op. Je tikt een minion-kaart en een groepje minions
stormt de lane in; je kiest het type dat de aankomende vijand counteert. Elke
botsing geeft impact: schermschud, botsplinters, goud dat uit gevallen vijanden
spat. Kills vullen de Bloedstreak; bij 3, 7 en 15 kills ontploft een beloning
(Goudregen-multiplier, Botgolem, Schaduwdraak). Op het juiste moment tik je de
ultimate van je champion.

### Short-Term (5-15 minutes)

Een slag van 2–3 minuten: breek de poort, verpletter de burcht, versla de
warlord. Daarna de buitkist-explosie: goud en edelstenen cascaderen met
multipliers (spelgeld, vaste uitkomst — geen gok). Je koopt eventueel een
upgrade en de volgende burcht op de kaart wacht al. Hier zit het "nog één
slag"-gevoel.

### Session-Level (30-120 minutes)

Een sessie van 20–40 minuten verovert een rijk van ongeveer 8 burchten, met een
boss-burcht als finale. Winst levert een nieuwe champion of relikwie op.
Natuurlijk stoppunt: na elke burcht. Reden om terug te komen: het volgende rijk
en het silhouet van een champion die je nog niet hebt.

### Long-Term Progression

Champions verzamelen (elk met lore, ultimate en een streak-variant),
relikwieën (items) vinden, minions en champions upgraden met edelstenen, en
rijk na rijk veroveren richting de **Duistere Troon** in het laatste rijk. De
game is "uitgespeeld" als de Troon is ingenomen; daarna blijven streak-records
en volledige verzameling als doelen.

### Retention Hooks

- **Curiosity**: volgend rijk op de kaart, champion-silhouetten die nog op slot zitten, onbekende relikwieën
- **Investment**: opgebouwde upgrades en champions; een upgrade die net binnen bereik ligt
- **Social**: geen (singleplayer, buiten scope)
- **Mastery**: langste Bloedstreak, eerste Schaduwdraak, zwaardere levels zonder verlies

---

## Game Pillars

### Pillar 1: Elke tik is een donderslag

Elke speleractie heeft een zichtbare, voelbare klap.

*Design test*: twijfelen we tussen een subtiel tactisch effect en een groot
zichtbaar effect, dan kiezen we het zichtbare.

### Pillar 2: De streak is koning

Opeenvolgend succes wordt steeds harder beloond.

*Design test*: twijfelen we tussen een vaste beloning en een oplopende, dan
kiezen we de oplopende.

### Pillar 3: Makkelijk te leren, ruimte voor meesterschap

Het eerste level speel je met één tik; strategische micro (minion terugroepen,
champion vooruit sturen, spreuk richten) komt er geleidelijk bij.

*Design test*: nieuwe micro mag, maar pas wanneer het level erom vraagt, en
nooit meer dan één nieuwe vaardigheid tegelijk.

### Pillar 4: Een duister rijk om te verzamelen

Nieuwe content komt als personage met lore, niet als kale stat.

*Design test*: twijfelen we tussen "+10% schade" en een nieuwe champion of
relikwie met een verhaal, dan kiezen we het personage.

### Pillar 5: Elke slag maakt je sterker

Levels worden geleidelijk zwaarder; de speler groeit mee met edelstenen die in
het spel verdiend worden en uitgegeven aan upgrades.

*Design test*: loopt een speler vast, dan moet er altijd een upgrade binnen
bereik zijn die met spelen te verdienen is — nooit een muur.

*Bewuste spanning*: pijler 1 (spektakel) trekt aan pijler 3 (eenvoud); pijler 2
(streaks die resetten) trekt aan het ontspannen flowgevoel.

### Anti-Pillars (What This Game Is NOT)

- **NOT echt-geld-gokken of loot boxes voor echt geld**: de casino-visuals zijn beloningspresentatie, geen weddenschap; gokken zou *De streak is koning* ondermijnen en het vertrouwen van de speler schaden.
- **NOT edelstenen kopen als enige manier om verder te komen**: dat breekt *Elke slag maakt je sterker*.
- **NOT realtime PvP-multiplayer**: breekt *Makkelijk te leren* en past niet in de tijdlijn.
- **NOT micro die je op dag één overspoelt** (formaties, meerdere lanes tegelijk vanaf het begin): breekt *Makkelijk te leren, ruimte voor meesterschap*.
- **NOT energietimers die je laten wachten**: breekt het ontspannen flowgevoel en het "nog één slag"-ritme.
- **NOT een dialoogzwaar verhaal**: lore leeft in champions en relikwieën (*Een duister rijk om te verzamelen*), niet in cutscenes.

---

## Inspiration and References

| Reference | What We Take From It | What We Do Differently | Why It Matters |
| ---- | ---- | ---- | ---- |
| League of Legends | Champions met ultimate, minion-golven over een lane, items | Eén duim, singleplayer, matches van 2–3 minuten | Bewijst dat champion + minion + item een herkenbare, geliefde structuur is |
| Call of Duty | Scorestreaks: kills → punten → steeds grotere beloningen | Streak voor een heel leger, met een champion die je moet beschermen | Het topmoment van de gebruiker; kern van pijler 2 |
| Pokémon | Verzamelen van wezens met eigen identiteit en lore | Champions als verzamelobject in een duister rijk | Verzamelen drijft lange-termijnretentie |
| Rome Total War | Legers aanvoeren, unit-types die elkaar counteren | Drie minion-types en lichte micro in plaats van formaties | Strategische laag zonder complexiteit |
| Casino-cascade-visuals | Tumbles, multipliers, goud-explosies als beloningspresentatie | Spelgeld en vaste uitkomsten, geen gok | Het meest bevredigende beloningsgevoel op mobiel, zonder het gokken |

**Non-game inspirations**: duistere fantasy-illustratie (obsidiaan, as, giftig
groene magie), het contrast van goud op zwart.

---

## Target Player Profile

| Attribute | Detail |
| ---- | ---- |
| **Age range** | 16–35 |
| **Gaming experience** | Casual tot mid-core |
| **Time availability** | Korte sessies van 5–15 minuten, af en toe 30–40 minuten |
| **Platform preference** | Mobiel |
| **Current games they play** | League of Legends / mobiele MOBA's, Pokémon, Call of Duty / Fortnite, Minecraft |
| **What they're looking for** | Het streak-gevoel en champion-fantasie in korte, simpele mobiele sessies |
| **What would turn them away** | Pay-to-win-muren, energietimers, ingewikkelde bediening |

---

## Technical Considerations

| Consideration | Assessment |
| ---- | ---- |
| **Recommended Engine** | Godot (voorkeur van de gebruiker); versie en referentie worden vastgelegd door `/setup-engine` |
| **Key Technical Challenges** | Veel units en particles tegelijk op goedkope telefoons; leesbare touch-UI in portret; eerste Godot-project |
| **Art Style** | 2D gestileerd (zijaanzicht of licht schuin), chunky silhouetten |
| **Art Pipeline Complexity** | Laag tot Medium — simpele vormen met gloed; beloningen grotendeels particles/shaders |
| **Audio Needs** | Moderate — sterke impact-SFX, streak-escalatie in geluid, sfeermuziek |
| **Networking** | None |
| **Content Volume** | MVP: 1 rijk, 5 levels, 1 champion, 3 minion-types, 3 vijandtypes, 3 streakbeloningen. Volledig: 5 rijken (~40 burchten), 10+ champions, relikwieën |
| **Procedural Systems** | Geen in MVP; eventueel later variatie in vijandgolven |

---

## Visual Identity Anchor

**Richting: "Obsidiaan & Goud"**

**Visuele regel:** *duisternis is het doek, beloning is licht.*

**Ondersteunende principes**

1. **Alleen beloning glanst.** Goud en edelsteenkleuren (robijn, smaragd,
   saffier) zijn exclusief voor beloningen, streaks en upgrades.
   *Design test*: krijgt een niet-belonend element goud of edelsteenglans, dan
   kiezen we een andere kleur.
2. **Intensiteit volgt de streak.** Hoe hoger de Bloedstreak, hoe meer gloed,
   particles en donkere bliksem in beeld.
   *Design test*: twijfelen we over de visuele sterkte van een effect, dan
   koppelen we die aan het streakniveau in plaats van een vaste waarde.
3. **Leesbaar in één blik.** Chunky, duidelijk verschillende silhouetten per
   minion- en vijandtype, ook op een klein telefoonscherm.
   *Design test*: is een unit op telefoonformaat niet herkenbaar aan z'n
   silhouet alleen, dan vereenvoudigen we de vorm.

**Kleurfilosofie:** diep paars, zwart en asgrijs als basis; giftig groen voor
vijandmagie (gevaar); goud en edelsteenkleuren uitsluitend voor beloning. De
speler leert: groen = gevaar, glans = winst.

---

## Risks and Open Questions

### Design Risks

- Te passief: als minion-keuze en champion-timing te weinig uitmaken, voelt een slag als toekijken.
- Moeilijkheidscurve wordt een edelsteen-grind in plaats van een uitdaging.
- Streak-reset bij champion-dood kan frustreren en het ontspannen gevoel breken.

### Technical Risks

- Prestaties met veel units en particles tegelijk op goedkope Android-toestellen.
- Eerste project in Godot; leercurve van de engine en mobiele export.
- Feasibility is niet beoordeeld door de technical-director (TD-FEASIBILITY overgeslagen — Lean mode).

### Market Risks

- Lane- en tower-battlers zijn druk bezet op mobiel; onderscheid moet uit streak-escalatie en de Obsidiaan & Goud-stijl komen.
- Winkelregels (App Store / Play Store) rond loot boxes en beloningspresentatie in casinostijl moeten worden gecontroleerd vóór release.

### Scope Risks

- Een roster van champions met lore is veel content voor solo-ontwikkeling.
- Tijdlijn van "weken" past bij de MVP, niet bij de volledige visie. Scope is niet beoordeeld door de producer (PR-SCOPE overgeslagen — Lean mode).

### Open Questions

- Is minion-sturen + Bloedstreak actief genoeg? → beantwoorden met `/prototype`.
- Welke streakdrempels (3/7/15) voelen goed? → tunen in het prototype.
- Wat gebeurt er bij champion-dood: volledige reset of half? → testen in het prototype.
- Monetisatiemodel (premium, advertenties, cosmetica)? → later beslissen, binnen de anti-pijlers.

---

## MVP Definition

**Core hypothesis**: Minions sturen plus de oplopende Bloedstreak voelt in 2–3
minuten krachtig genoeg dat de speler meteen nog een slag wil spelen.

**Required for MVP**:
1. Eén lane met automatisch lopende minions en drie minion-kaarten die elkaar counteren
2. Eén champion met opladende ultimate
3. Bloedstreak met drie drempelbeloningen (Goudregen, Botgolem, Schaduwdraak)
4. Drie vijandtypes en een vijandelijke burcht om te verwoesten
5. Eén rijk met 5 levels van oplopende moeilijkheid
6. Edelstenen verdienen en één upgrade-scherm
7. Buitkist-explosie in Obsidiaan & Goud-stijl na een gewonnen slag

**Explicitly NOT in MVP** (defer to later):
- Meerdere champions en het verzamelsysteem
- Relikwieën (items)
- Boss-burchten en meerdere rijken
- Strategische micro-acties (terugroepen, vooruit sturen, spreuk richten)
- Lore-teksten en monetisatie

### Scope Tiers (if budget/time shrinks)

| Tier | Content | Features | Timeline |
| ---- | ---- | ---- | ---- |
| **MVP** | 1 rijk, 5 levels, 1 champion | Kernloop + streak + upgrades | 2–4 weken |
| **Vertical Slice** | 1 gepolijst rijk met boss, 3 champions | Kern + progressie + relikwieën | +3–4 weken |
| **Alpha** | 3 rijken, 6 champions, placeholder-art | Alle systemen, ruw, inclusief micro | +2–3 maanden |
| **Full Vision** | 5 rijken, 10+ champions, Duistere Troon | Alles, gepolijst | 4–6 maanden totaal (solo) |

---

## Next Steps

- [ ] Configureer de engine (`/setup-engine`) — voorkeur: Godot
- [ ] **Prototype de kern** (`/prototype minion-sturen + bloedstreak`) — valideer dat het leuk is vóór GDD's
- [ ] Als het prototype PROCEED geeft: art bible (`/art-bible`) vanuit het Visual Identity Anchor
- [ ] Concept valideren (`/design-review design/gdd/game-concept.md`)
- [ ] Systemen in kaart brengen (`/map-systems`)
- [ ] Per systeem een GDD (`/design-system [systeem]`) — met de lessen uit het prototype
- [ ] Architectuur (`/create-architecture`, `/architecture-decision`, `/architecture-review`)
- [ ] Vertical slice in Pre-Production (`/vertical-slice`)
- [ ] Eerste milestone plannen (`/sprint-plan new`)
