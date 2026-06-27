# DFO Opleidingen — website

Statische website voor het opleidingsportaal van Bureau DFO (homepage + trainerspagina).
Geen build-stap nodig: het zijn losse HTML-bestanden met afbeeldingen.

## Structuur

```
/
├─ index.html              → de homepage (dfo-opleidingen.nl)
├─ trainers/
│  └─ index.html           → de trainerspagina (dfo-opleidingen.nl/trainers)
├─ fotos/                  → pasfoto's van de trainers (voornaam-achternaam.jpg)
├─ logo-dfo.png            → logo in de header
├─ favicon.png             → tabblad-icoon
├─ llms.txt                → AI-/zoekvindbaarheid (in de root van het domein houden)
├─ README.md               → dit bestand
└─ _intern/
   └─ beheerdershandleiding.html  → NIET online plaatsen; interne uitleg
```

## Publiceren via GitHub Pages

1. Maak een repository en upload de inhoud van deze map (sleep alle bestanden + mappen in GitHub).
2. Ga naar **Settings → Pages** en kies de branch (meestal `main`) met map `/ (root)`.
3. De site komt online op `https://<gebruiker>.github.io/<repo>/`.
   - Homepage: `…/`
   - Trainers: `…/trainers/`
4. Eigen domein koppelen kan via **Settings → Pages → Custom domain**.

> Let op: de map `_intern/` bevat de beheerdershandleiding. Verwijder die map als je
> niet wilt dat hij (theoretisch) online benaderbaar is, of bewaar de handleiding buiten de repo.

## Een trainer/foto wijzigen

- Foto's: zet een vierkant `.jpg`-bestand in `fotos/` met de naam `voornaam-achternaam.jpg`
  (kleine letters, geen accenten, koppeltekens). Bestaat de foto niet, dan toont de kaart
  automatisch de initialen.
- Trainersgegevens staan in de lijst `const trainers = [ … ]` onderin **beide** HTML-bestanden.
  Wijzig een trainer in zowel `index.html` als `trainers/index.html`, zodat ze gelijk blijven.
- Zie `_intern/beheerdershandleiding.html` voor de volledige uitleg.

## Let op (AFM/compliance)

Het volgen van een opleiding geeft op zichzelf geen garantie dat aan de Wft-vakbekwaamheids-
of PE-eisen is voldaan. Pas PE-teksten alleen aan als dat per opleiding klopt met de erkenning
(o.a. SEH, NVHP, FFP).
