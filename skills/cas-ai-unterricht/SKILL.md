---
name: cas-ai-unterricht
description: Erstellt komplette Unterrichtsunterlagen für den CAS Advanced AI in Marketing (HWZ): von der Tagesdramaturgie über Übungen bis zur fertig befüllten PowerPoint in der HWZ-Vorlage. Trigger: "Unterlagen für Tag X", "HWZ Präsentation erstellen", "Kurstag vorbereiten", "Folien für meinen CAS-Tag", "Dramaturgie für den Unterricht", "Übungen für den Kurstag bauen". Nicht triggern bei: allgemeinen PowerPoint-Wünschen ohne HWZ/CAS-Bezug, BEYONDER-Kundenpräsentationen (brand-guidelines/social-posts-carousel), Fragen zum Kursinhalt ohne Unterlagen-Auftrag. Endresultat: eine .pptx auf Basis der HWZ-Vorlage mit Dramaturgie, Übungsfolien und Speaker Notes, plus Übungsaufträge und FERC-Reflexion für den Kurstag.
---

# cas-ai-unterricht

Hilft Dozierenden des CAS Advanced AI in Marketing (HWZ, Herbst 2026), ihren Kurstag zu bauen:
Dramaturgie, Übungen und eine befüllte PowerPoint in der offiziellen HWZ-Vorlage.

## Goldene Regeln

1. **Zielgruppe nie vergessen:** Marketing-Profis mit KI-Erfahrung, an oder in einer Leadership-Rolle. Keine Grundlagen, hoher Hands-on-Anteil, Übungen am eigenen Case (Challenge), pro Tag mindestens eine Leadership-Folie.
2. **Kursdaten sind Gesetz:** Lernziele, Leitidee, Transfer und FERC-Aufgaben des Tages stehen in `references/tage-dozierende.md` und werden wörtlich übernommen, nicht neu erfunden.
3. **FERC prägt den Tag:** Frame → Explore → Refine → Commit als Tagesrhythmus, FERC-Reflexion als Pflicht-Abschluss.
4. **Schnittthemen prüfen:** Nichts unterrichten, was ein anderer Tag vertieft (Liste in `references/kurskontext.md`).
5. **PPTX nur über die Vorlage:** Immer `scripts/build_pptx.py` mit der HWZ-Vorlage aus `assets/`, nie Folien frei gestalten. Echte Umlaute überall.
6. **Erst Konzept, dann Folien:** Dramaturgie und Übungen mit dem/der Dozierenden festziehen, bevor die PPTX gebaut wird.
7. **1 Aussage = 1 Folie, Layouts variieren:** Modelle und Frameworks (z.B. CORE+) als grafische Übersicht plus pro Element eine Erklär- und eine Beispielfolie auflösen (Muster in `references/dramaturgie-uebungen.md`). Für fehlende Grafiken Bild-Platzhalter setzen.

## Ablauf

### Schritt 1: Geführter Start (immer, ausser alles ist schon genannt)

Beim Aktivieren zuerst begrüssen und den Ablauf zeigen, dann Schritt für Schritt führen.
Nie alle Fragen auf einmal abwerfen. Eröffnung sinngemäss:

> **Willkommen beim Unterlagen-Assistenten für den CAS Advanced AI in Marketing (HWZ).**
> Ich führe dich in vier Schritten zu deinen fertigen Unterrichtsunterlagen:
> 1. Du sagst mir, wer du bist und welchen Kurstag du unterrichtest.
> 2. Du gibst mir deine Inhalte, Beispiele und Demos.
> 3. Wir bauen gemeinsam die Tagesdramaturgie und die Übungen (du nimmst ab).
> 4. Ich erstelle die fertige PowerPoint in der HWZ-Vorlage plus dein Übergabepaket.
>
> **Wer bist du, und welchen Kurstag bereitest du vor?**

Dann geführt weiter, immer eine Frage aufs Mal:

1. **Dozent/in nennt sich:** Profil in `references/tage-dozierende.md` nachschlagen. Hat die Person mehrere Tage, ihre Tage zur Auswahl anbieten. Ist die Person unbekannt: Tag/Thema direkt erfragen.
2. **Tag bestätigen:** Die Eckdaten des Tages zeigen (Datum, Leitidee, Lernziele, FERC-Anwendung, Artefakt) und bestätigen lassen. Das schafft Vertrauen und deckt veraltete Annahmen auf.
3. **Inhalte einsammeln:** Fragen, welche Inhalte, Beispiele, Live-Demos, Tools, Screenshots und eigenen Cases die Person mitbringt, und was ihr besonders wichtig ist. Optional: Umfang (Standard 25–40 Folien).
4. **Kurz zusammenfassen** und ankündigen, was als Nächstes passiert (Dramaturgie-Entwurf).

Sind Dozent/in, Tag und Inhalte schon in der Anfrage genannt: Begrüssung auf einen Satz
kürzen, Tages-Eckdaten trotzdem zur Bestätigung zeigen, dann direkt zu Schritt 3.

### Schritt 2: Kurskontext laden

Lies `references/kurskontext.md` (Kurs, Zielgruppe, FERC, CORE+, Abgaberegeln, Schnittthemen)
und in `references/tage-dozierende.md` den Eintrag zum gewählten Tag plus das Profil des/der
Dozierenden (Bogen, Absprachen). Bei Zweifel an der Aktualität: Repo
`github.com/chrisbeyeler/cas-ai-advanced-in-marketing` klonen und als Wahrheit nehmen
(insbesondere `downloads/curriculum/Curriculum_TagXX_*.docx`).

### Schritt 3: Dramaturgie entwerfen

Lies `references/dramaturgie-uebungen.md`. Baue den Tagesplan (8 Lektionen, 08.15–16.45)
entlang des FERC-Rasters, mit den mitgebrachten Inhalten des/der Dozierenden.
Liefere: Tagesraster mit Zeiten, pro Block die Kernbotschaft, Übungen mit Auftrag/Zeit/
Artefakt/Kriterien, FERC-Reflexion am Schluss. **Dem/der Dozierenden zur Abnahme vorlegen.**

### Schritt 4: Folienplan bauen

Nach der Abnahme: Folienplan gemäss Folien-Dramaturgie (Standardaufbau, Framework-Muster
und Platzhalter-Regeln in `references/dramaturgie-uebungen.md`) als JSON gemäss
`references/hwz-vorlage.md` (Layout-Katalog, Layout-Zuordnung pro Folientyp, Plan-Format).
Grundprinzip 1 Aussage = 1 Folie, Layouts aktiv variieren, für geplante Grafiken und
Screenshots Bild-Platzhalter mit `BILD-PLATZHALTER:`-Note setzen. Speaker Notes pro Folie:
Regieanweisungen, Zeitmarken, Demo-Schritte. Übungsfolien mit Auftrag, Zeit, Artefakt,
Kriterien auf einer Folie.

### Schritt 5: PPTX erzeugen und verifizieren

```bash
python3 scripts/build_pptx.py plan.json "TagXX_<Thema>.pptx"
```

Warnungen des Scripts beheben (Exit-Code 2 = Warnungen). Danach Datei kurz per
python-pptx gegenlesen (Folienzahl, Stichproben-Titel), erst dann als fertig melden.
Hinweis an Dozierende: Abgabe auf myHWZ als PPTX **und** PDF, 5 Arbeitstage vor dem Kurstag;
Curriculum 10 Arbeitstage vorher (vorbefüllt im Repo unter `downloads/curriculum/`).

### Schritt 6: Übergabepaket

Zusammen mit der PPTX liefern: Tagesraster (Markdown), Übungsaufträge im Wortlaut,
FERC-Reflexionsauftrag mit Abgabefrist (+5 Arbeitstage), Liste aller Bild-Platzhalter
(Folie + benötigte Grafik/Screenshot), offene Punkte aus den Absprachen des/der
Dozierenden (Spalte «Absprachen/Aufgaben» im Dozierenden-Profil).

## Vertiefungen (nur bei Bedarf laden)

| Thema | Datei |
|---|---|
| Kurs, Zielgruppe, FERC, CORE+, Abgaberegeln | `references/kurskontext.md` |
| 16 Kurstage + Dozierenden-Profile | `references/tage-dozierende.md` |
| Tagesdramaturgie, Übungsformate, Folien-Aufbau | `references/dramaturgie-uebungen.md` |
| HWZ-Layouts, Farben, Plan-Format, build_pptx | `references/hwz-vorlage.md` |

Vor jedem Lauf: `references/learnings.md` lesen und gesammelte Regeln anwenden.
