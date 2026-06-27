# DFO Opleidingen — website

Statische website voor het opleidingsportaal van Bureau DFO. Geen build-stap: losse HTML-bestanden met afbeeldingen.

## Belangrijk: alle bestanden in de ROOT (geen submappen)

Deze versie is gemaakt voor GitHub Pages op een subpad (bijv. `https://jeroen-o.github.io/dfo-opleidingen/`).
Daarom staan **alle bestanden plat in de hoofdmap** en gebruiken de pagina's relatieve paden
zonder map (`monique-londema.jpg`, `logo-dfo.png`). Zo werkt het ongeacht het subpad.

```
index.html         → de homepage
trainers.html      → de trainerspagina
*.jpg              → alle trainersfoto's (los in de root!)
logo-dfo.png       → logo in de header
favicon.png        → tabblad-icoon
llms.txt           → AI-/zoekvindbaarheid
README.md          → dit bestand
beheerdershandleiding.html → interne uitleg (eventueel verwijderen voor productie)
```

## Uploaden naar GitHub (de juiste manier)

1. Sleep **alle losse bestanden** (niet een map eromheen) in je repository.
2. Settings → Pages → branch `main`, map `/ (root)` → Save.
3. Online op:
   - Homepage: `https://<gebruiker>.github.io/<repo>/`
   - Trainers: `https://<gebruiker>.github.io/<repo>/trainers.html`

> Veelgemaakte fout: een map (zoals `fotos/`) meeslepen terwijl de pagina's de foto's in de root
> verwachten. In deze versie staan alle foto's bewust **plat in de root** — houd dat zo.

## Foto's / trainers wijzigen

- Foto toevoegen: zet een vierkant `.jpg` in de root met de naam `voornaam-achternaam.jpg`
  (kleine letters, geen accenten, koppeltekens). Ontbreekt de foto, dan toont de kaart de initialen.
  (Linda Vervloet heeft nog geen foto → toont initialen tot `linda-vervloet.jpg` wordt toegevoegd.)
- Trainersgegevens staan in `const trainers = [ … ]` onderin **beide** bestanden
  (`index.html` én `trainers.html`). Wijzig ze in allebei zodat ze gelijk blijven.

## Let op (AFM/compliance)

Het volgen van een opleiding geeft op zichzelf geen garantie dat aan de Wft-vakbekwaamheids-
of PE-eisen is voldaan. Pas PE-teksten alleen aan als dat per opleiding klopt met de erkenning
(o.a. SEH, NVHP, FFP).
