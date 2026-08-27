# Learnings: cas-ai-unterricht

> Erstellt: 2026-08-27
> Letztes Pruning: 2026-08-27
> Eintragsanzahl: 6

---

## Aktive Regeln (immer anwenden)

<!--
Hier kommen verifizierte Regeln rein, die der Skill bei jedem Lauf
anwenden soll. Format:

1. <Regel mit kurzer Begründung>
2. <nächste Regel>

Eintrag nur, wenn die Regel mindestens 2x bestätigt wurde.
-->

1. Textmenge pro Karte begrenzen statt Autofit: KPI-Karten nur Zahl + Label (max. 6 Wörter), Inhalts-Karten max. 30 Wörter. Autofit (`TEXT_TO_FIT_SHAPE`) erzeugt inkonsistente Schriftgrössen zwischen Karten. (Design-Recherche 2026-08-28)
2. Karten: entweder helle Flächenfüllung ODER dünner Rahmen, nie beides. Akzentbalken nur oben, 3-5pt. Eckenradius klein (adjustment 0.04-0.08), sonst wirkt es verspielt. (Design-Recherche 2026-08-28)
3. Diagramm-Element-Limits sind Lesbarkeits-Grenzen, nicht Geschmack: Prozess max. 6, Zyklus 4-6, Pyramide 3-5, Timeline max. 7. Das Script kürzt mit Warnung, besser vorher planen. (Design-Recherche 2026-08-28)
4. Schrift-Minimum in Diagrammen 11pt, Karten-Fliesstext 12-13pt; Bullets auf Folien deutlich grösser (Vorlagen-Standard). Kontrast auf farbigen Flächen immer über `text_color_for()` (programmatisch), nie per Augenmass. (Design-Recherche 2026-08-28)
5. Ein Deck ohne Diagramme wirkt wie eine Textwüste: pro Deck mindestens 2 Diagramm- und 1 Card-Folie, aber nie zwei gleiche Diagramm-Typen direkt hintereinander. (Chris-Auftrag 2026-08-28)
6. Verifikation der PPTX auf dem Air: PowerPoint per AppleScript als PDF exportieren, `pdftoppm -png` rastern, Folien als Bilder prüfen. Ein fehlerfreier Build-Lauf ist KEIN Beleg für gute Folien. (Session 2026-08-28)

---

## Beobachtete Muster

### Was funktioniert

<!--
- <Pattern>, <Datum>, <kurzer Kontext>
-->

_(noch keine Beobachtungen)_

### Was nicht funktioniert

<!--
- <Pattern>, <Datum>, <kurzer Kontext>
-->

_(noch keine Beobachtungen)_

---

## Skill-spezifische Kennzahlen

<!--
Numerische Werte mit Kontext. Beispiele:
- Optimale Länge: 800-1200 Zeichen
- FAQ-Block min. 3 Fragen
- Response-Zeit-Ziel: <30s
-->

_(noch keine Kennzahlen erfasst)_

---

## Offene Fragen / zu testen

<!--
Hypothesen, die noch nicht verifiziert sind. Werden nach Verifizierung
in "Aktive Regeln" verschoben oder verworfen.
-->

_(noch keine offenen Fragen)_

---

## Pruning-Notizen

<!--
Beim wöchentlichen Pruning hier kurz dokumentieren:
- <Datum>: <Anzahl> Einträge entfernt, Grund: <Duplikat/veraltet/Single-Event>
-->

_(noch nicht gepruned)_
