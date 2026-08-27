# HWZ-Vorlage: Layouts, Farben, PPTX-Erzeugung

Vorlage: `assets/HWZ_Praesentationsvorlage_extern_DE.potx` (identisch mit `downloads/` im Kurs-Repo).
16:9 (12192000×6858000 EMU), Schrift **Aptos**, Sprache Deutsch.

## Farbpalette (aus dem Theme)

- HWZ-Dunkelblau `#001447`, HWZ-Blau `#002FA8`, Mittelblau `#2F56B9`, Hellblau `#3C6BDA`
- Hellblau-Fläche `#D8E1F7`, Grün `#92B93D`, Gelb `#FFAA00`, Rot `#DA1E28`, Schwarz/Weiss
- Nur diese Farben verwenden. Akzente sparsam (Grün = positiv, Rot = Warnung, Gelb = Hinweis).

## Layout-Katalog (Name exakt so im Folienplan verwenden)

| Layout-Name | Einsatz | Text-Platzhalter (idx) |
|---|---|---|
| `Titelfolie hell` / `Titelfolie dunkel` | Deck-Start (dunkel = Standard) | title, subtitle, body idx 10 (Datum/Dozent) |
| `Titel Bild vollflächig` | Kapiteltrenner mit Bild | title, body idx 11; Bild idx (Picture) |
| `Titel hell - Bild rechts` / `Titel dunkel  - Bild rechts` | Kapiteltrenner (dunkel hat 2 Spaces!) | title, subtitle, body idx 11, Bild idx 10 |
| `Inhalt normal` | Standard-Inhaltsfolie | title, body idx 1 |
| `Inhalt 3 Spalten` | Drei Konzepte nebeneinander | title, Spalten idx 2, 4, 14 |
| `Vergleich` | Zwei Optionen gegenüberstellen | title, links: Kopf idx 1 + Inhalt idx 2, rechts: Kopf idx 10 + Inhalt idx 11 |
| `Folie mit Bild rechts` | Inhalt + grosses Bild | title, body idx 1, Bild idx 10 |
| `Folie mit schmalerem Bild rechts` | Inhalt + schmales Bild | title, body idx 1, Bild idx 10 |
| `Inhalt Bild rechts` / `Inhalt Bild links` | Inhalt + Bild + Bildlegende | title, body idx 1, Bild idx 10, Legende idx 16 |
| `Inhalt 2 Bilder` | Zwei Bilder mit Legenden | title, Bilder idx 10+11, Legenden idx 16+17 |
| `Bild vollflächig` | Vollbild (Demo-Screenshot) | nur Bild idx 10 |
| `3 Spalten Titel - blau` | Drei Textspalten auf Blau | title, Spalten idx 10, 11, 12 |
| `Team 4 Personen` / `Team 6 Personen` | Dozierenden-/Team-Vorstellung | title, Bild+Name+Rolle pro Person |
| `Schlussfolie` | Letzte Folie | keine Platzhalter (fixes Design) |

Faustregeln:
- Titelfolie dunkel → Tagesbogen/Agenda auf `Inhalt normal` → Kapiteltrenner mit `Titel dunkel  - Bild rechts` oder `Titel Bild vollflächig` → Inhalt gemischt → `Schlussfolie`.
- Übungsfolien auf `Inhalt normal` (Auftrag, Zeit, Artefakt, Kriterien als Bullets).
- Bild-Platzhalter dürfen leer bleiben (Dozierende ergänzen eigene Bilder/Screenshots). Zu jedem leeren Bild-Platzhalter gehört eine Note-Zeile `BILD-PLATZHALTER: <Beschreibung>` (siehe `dramaturgie-uebungen.md`).
- **Layout-Varianz ist Pflicht:** nie mehr als 3 Folien `Inhalt normal` hintereinander; pro Deck mindestens 5 verschiedene Layouts einsetzen.

## Layout-Zuordnung pro Folientyp (1 Aussage = 1 Folie)

| Folientyp | Layout |
|---|---|
| Leitidee / grosse These | `Titel Bild vollflächig` oder `3 Spalten Titel - blau` (Mittelspalte leer) |
| Modell-/Framework-Übersicht (Grafik) | `Inhalt Bild rechts` oder `Bild vollflächig` (Grafik-Platzhalter) |
| Element-Erklärung (z.B. «C wie Character») | `Inhalt normal` oder `Folie mit Bild rechts` |
| Element-Beispiel | `Inhalt Bild rechts` (Screenshot + Legende) oder `Vergleich` (Vorher/Nachher) |
| Drei Konzepte / drei Optionen | `Inhalt 3 Spalten` |
| Gegenüberstellung / Pro-Contra | `Vergleich` |
| Live-Demo-Anker / Screenshot | `Bild vollflächig` |
| Zwei Beispiele nebeneinander | `Inhalt 2 Bilder` |
| Merkregel / Kernaussage auf Blau | `3 Spalten Titel - blau` |
| Transfer- und Leadership-Folie | `Folie mit schmalerem Bild rechts` (Bild-Platzhalter) |

## PPTX bauen: `scripts/build_pptx.py`

Der Folienplan ist eine JSON-Datei; das Script füllt die Vorlage und schreibt eine .pptx.

```bash
python3 scripts/build_pptx.py plan.json output.pptx           # nutzt assets-Vorlage
python3 scripts/build_pptx.py plan.json output.pptx pfad.potx # eigene Vorlage
```

Plan-Format (eine Folie pro Objekt):

```json
{"slides": [
  {"layout": "Titelfolie dunkel",
   "title": "Advanced Prompt-Engineering",
   "subtitle": "CAS Advanced AI in Marketing · Tag 3",
   "texts": {"10": ["Gustavo Salami · Mi 09.09.2026"]},
   "notes": "Begrüssung, Bezug zu Tag 1, Challenge-Liste erwähnen."},
  {"layout": "Inhalt normal",
   "title": "Lernziele heute",
   "bullets": ["strukturierte JSON-/XML-Outputs erzeugen",
               {"t": "Prompt-Chains für eine Kampagne bauen", "lvl": 0},
               {"t": "Beispiel: Recherche → Botschaft → Varianten", "lvl": 1}],
   "notes": "Lernziele wörtlich aus dem Curriculum."},
  {"layout": "Vergleich",
   "title": "Einzel-Prompt vs. Chain",
   "texts": {"1": ["Einzel-Prompt"], "2": ["schnell", "nicht reproduzierbar"],
             "10": ["Chain"], "11": ["Produktionsplan", "skalierbar"]}},
  {"layout": "Schlussfolie"}
]}
```

Felder pro Folie:
- `layout` (Pflicht): exakter Layout-Name aus der Tabelle.
- `title`, `subtitle`: Strings.
- `bullets`: Liste für den ersten Body-/Object-Platzhalter; Eintrag als String oder `{"t": "...", "lvl": 0-4}`.
- `texts`: gezielt per Platzhalter-idx (Schlüssel als String), Wert = Liste von Absätzen (String oder `{"t","lvl"}`).
- `images`: `{"10": "pfad/bild.png"}`, füllt Bild-Platzhalter.
- `notes`: Speaker Notes (Regieanweisungen, Zeitmarken, Demo-Schritte).

Nach dem Bauen IMMER verifizieren: Script meldet Folienzahl und Warnungen
(unbekanntes Layout, nicht gefundene idx). Warnungen beheben, nicht ignorieren.
Die Datei zusätzlich mit `python3 -c "from pptx import Presentation; print(len(Presentation('out.pptx').slides.__iter__.__self__._sldIdLst))"`
oder schlicht durch Öffnen prüfen. Abgabe an HWZ: PPTX **und** PDF-Export.
