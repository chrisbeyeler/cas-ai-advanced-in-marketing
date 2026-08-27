# Dramaturgie & Übungen: Kurstag bauen

Zielgruppe: Marketing-Profis mit KI-Erfahrung, an oder vor der Schwelle zur Führungsrolle.
Sie verzeihen keine Grundlagen-Wiederholung und keine Alibi-Übungen.

## Tagesraster (8 Lektionen, 08.15–16.45)

Bewährter Rhythmus, an den konkreten Tag anpassen (nicht sklavisch übernehmen):

| Slot | Zeit | Inhalt | FERC-Phase |
|---|---|---|---|
| 1 | 08.15–09.00 | Ankommen, Tagesbogen, Bezug zur Challenge, Vorwissen aktivieren | Frame |
| 2 | 09.00–10.30 | Input-Block 1: Kernkonzept mit Live-Demo | Frame |
| Pause | 10.30–10.50 | | |
| 3 | 10.50–12.15 | Hands-on 1: geführte Übung, alle am gleichen Beispiel | Explore |
| Mittag | 12.15–13.15 | | |
| 4 | 13.15–14.30 | Input-Block 2: Vertiefung, Fallstricke, Profi-Perspektive | |
| 5 | 14.30–15.45 | Hands-on 2: Übung am eigenen Case (Challenge), Coaching in Gruppen | Explore/Refine |
| 6 | 15.45–16.30 | Ergebnisse vergleichen (Raster), Peer-Feedback, Transfer-Diskussion | Refine |
| 7 | 16.30–16.45 | Commit: Was übernehme ich? FERC-Reflexion ausgeben, Ausblick | Commit |

Regeln:
- **Nachmittag gehört dem eigenen Case.** Vormittag darf am gemeinsamen Beispiel laufen.
- **Jeder Tag produziert ein Hands-on-Artefakt** (steht pro Tag in den Tagesdaten, z.B. «1 Master-Prompt + 1 Chain pro Person»). Das Artefakt ist der Baustein für den Leistungsnachweis.
- **Live-Demos vor Folien.** Folien rahmen, das Werkzeug überzeugt. Pro Input-Block max. 10–12 Folien.
- **Energie-Kurve:** Nach dem Mittag nie mit 45 Minuten Theorie starten; erst aktivieren (kurze Anwendung, Quiz, Diskussion), dann Input.

## Folien-Dramaturgie (Struktur des Decks)

**Grundprinzip: 1 Aussage = 1 Folie.** Jede Folie trägt genau eine Kernbotschaft im Titel.
Lieber mehr Folien mit wenig Inhalt als wenige volle. Sammelfolien («5 Punkte zu X») nur
für Agenda, Lernziele und Zusammenfassungen.

Standardaufbau eines Tagesdecks (30–50 Folien, mit Framework-Blöcken auch mehr):

1. **Titelfolie:** Tag, Thema, Dozent/in, Datum (Layout «Titelfolie dunkel»).
2. **Tagesbogen:** Wo stehen wir im CAS, was war vorher, was baut darauf auf («Inhalt normal»).
3. **Leitidee als These:** Die Leitidee des Tages (aus den Tagesdaten) als eine grosse Aussage.
4. **Lernziele + Agenda:** Lernziele wörtlich aus dem Curriculum übernehmen (Konsistenz!).
5. **Pro Input-Block:** These → Konzept → Beispiel/Demo-Verweis → Merkregel, je als eigene Folie. Nie mehr als 5 Bullets pro Folie, Bullets sind Aussagen, keine Stichwort-Wolken.
6. **Übungsfolien:** Auftrag, Zeitbudget, erwartetes Artefakt, Bewertungskriterien: alles auf EINER Folie, die während der Übung stehen bleibt.
7. **Transfer-Folie:** Der Transfer-ins-Marketing-Text des Tages, als Brücke formuliert.
8. **Leadership-Folie:** Was heisst das für Führung? (Delegation, Qualitätssicherung, Team-Rollout, Ownership/Authorship.) Mindestens eine pro Tag.
9. **Commit + Reflexion:** FERC-Reflexionsauftrag, Abgabefrist (+5 Arbeitstage), nächster Schritt.
10. **Schlussfolie** (Layout «Schlussfolie»).

Speaker Notes nutzen: Regieanweisungen, Zeitmarken, Demo-Schritte, erwartete Rückfragen
gehören in die Notizen, nie auf die Folie.

## Framework-Muster: Modelle in Folien auflösen

Modelle und Frameworks (CORE+, FERC, SDSP, Funnel-Modelle, eigene Raster) NIE auf eine
einzelne Textfolie quetschen. Standardmuster:

1. **Übersichtsfolie mit Diagramm:** Das ganze Modell als gerendertes Diagramm
   (`diagram` typ zyklus/prozess/pyramide auf «Inhalt normal», Spezifikation in
   `hwz-vorlage.md`). Nur wenn kein Diagramm-Typ passt: Grafik-Platzhalter setzen.
2. **Pro Element eine Erklärfolie:** Element im Titel (z.B. «C wie Character»), 2–4 Bullets
   was es leistet und worauf zu achten ist («Inhalt normal» oder «Folie mit Bild rechts»).
3. **Pro Element eine Beispielfolie:** Konkretes Marketing-Beispiel, Prompt-Ausschnitt oder
   Screenshot dazu («Inhalt Bild rechts», «Vergleich» für Vorher/Nachher, «Bild vollflächig»
   für Screenshots).
4. **Abschlussfolie des Blocks:** Modell nochmals komplett (gleiche Grafik wie 1.), jetzt
   als Merkbild vor der Übung.

Beispiel CORE+: 1 Übersicht + je Erklärung und Beispiel für C, O, R, E, + Talk = 11 Folien,
plus Merkbild. Diese Folienzahl ist gewollt; der Takt hält das Publikum im Vortrag.

Bei jedem Muster die Layouts abwechseln (Katalog und Zuordnung in `hwz-vorlage.md`):
nie mehr als 3 reine Textfolien «Inhalt normal» hintereinander (Folien mit `cards`
oder `diagram` zählen als eigene Optik, nicht als Textfolie).

## Cards & Diagramme einsetzen (Anspruch: aussergewöhnlich gute Folien)

- **Struktur sichtbar machen statt aufzählen:** Sobald Bullets eine verdeckte Struktur
  haben (Schritte, Kreislauf, Ebenen, 2 Dimensionen, Zeitachse), das passende Diagramm
  wählen: prozess, zyklus, pyramide, matrix, timeline (Spezifikation in `hwz-vorlage.md`).
- **Karten für Nebeneinander:** 2–4 gleichrangige Konzepte, Hebel, Regeln oder Rollen als
  `cards`; Kennzahlen und Vorher/Nachher-Werte als KPI-Karten (`kpi`).
- **Akzentfarben nach Bedeutung:** gruen = positiv/empfohlen, rot = Risiko/Warnung,
  gelb = Hinweis. Standard bleibt Blau. Nie dekorativ einfärben.
- **Pro Deck mindestens 2 Diagramm-Folien und 1 Card-Folie**, sonst wirkt das Deck wie
  eine Textwüste. Umgekehrt: nie zwei Diagramme derselben Art direkt hintereinander.
- **Tagesbogen/Agenda als timeline**, Framework-Übersichten als zyklus/prozess/pyramide,
  Entscheidungshilfen als matrix.

## Grafik- und Bild-Platzhalter

- Wo eine Grafik oder ein Screenshot hingehört, immer ein Layout MIT Bild-Platzhalter wählen
  und den Platzhalter leer lassen; Dozierende ergänzen das Bild selbst.
- In die Speaker Notes eine Zeile `BILD-PLATZHALTER: <was hier hingehört>` schreiben
  (z.B. «BILD-PLATZHALTER: CORE+-Übersichtsgrafik, 5 Bausteine als Kreis»).
- Hat das Layout eine Bildlegende (idx 16/17), dort eine kurze Beschriftung setzen, damit
  der Platzhalter auf der Folie erkennbar bleibt.
- Pro Deck-Entwurf am Schluss eine Liste aller Bild-Platzhalter ins Übergabepaket aufnehmen,
  damit Dozierende wissen, welche Grafiken sie noch beschaffen müssen.

## Übungsformate (passend zur Zielgruppe)

- **Challenge-Sprint:** 20–40 Min. am eigenen Case mit klarem Artefakt-Ziel. Das Arbeitspferd.
- **Varianten-Battle (Explore/Refine):** Alle erzeugen N Varianten, Vergleich mit Bewertungsraster aus dem Materialpool. Trainiert kritisches Urteil statt Tool-Bedienung.
- **Peer-Review-Runde:** Tandems prüfen gegenseitig mit Raster (Peer-Review-Bogen im Materialpool). Führungsrelevant: Feedback geben nach Kriterien.
- **Reverse Engineering:** Fertiges gutes Ergebnis zeigen, Teilnehmende rekonstruieren den Weg (Prompt, Chain, Workflow). Stark für Fortgeschrittene.
- **Rollenwechsel Lead/Doer:** Eine Person briefet nur (wie eine Führungskraft), die andere setzt mit KI um; danach Wechsel. Macht Delegations-Qualität sichtbar.
- **Live-Klinik:** Freiwillige/r bringt echten Fall, Plenum löst gemeinsam, Dozent/in moderiert. Hoher Energiewert nach dem Mittag.
- **Gallery Walk:** Artefakte aufhängen/teilen, alle sichten, Punkte vergeben. Schneller Abschluss-Vergleich ohne 16 Einzelpräsentationen.

Jede Übung braucht: Auftrag in einem Satz, Zeitbudget, Artefakt, Kriterien, Anschluss (was passiert mit dem Ergebnis).

## Typische Fehler (vermeiden)

- Grundlagen wiederholen, die Pre-Reading oder frühere Tage abdecken (Schnittthemen-Liste prüfen!).
- Übungen an fiktiven Firmen, obwohl die Challenge-Liste echte Cases liefert.
- Tool-Feuerwerk ohne Urteils-Training: Die Zielgruppe muss bewerten und entscheiden lernen, nicht nur bedienen.
- Folien als Skript-Ersatz volltexten. Skript ist Pflichtliteratur, Folien sind Bühne.
- FERC-Reflexion vergessen: Sie ist an jedem Tag Pflicht-Abschluss.
- Fahrplan-/Theorie-Overload am Nachmittag.
