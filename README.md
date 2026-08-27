# CAS Advanced AI in Marketing HWZ · Dozierenden-Cockpit Herbst 2026

Statische Einzeldatei (`index.html`), kein Build-Step. Öffnen im Browser genügt.

Inhalt: Semesterband mit allen 18 Terminen, Tagesseiten (Thema, Lernziele, Transfer ins klassische Marketing, FERC-Rhythmus, Aufgaben der Dozierenden), Dozierenden-Übersicht mit Einsätzen und Absprachen, sieben Schnittthemen, Disziplinen-Matrix, drei Vorschläge für Leistungsnachweise mit Bewertungsrastern sowie Rahmenmodelle (FERC, CORE+, Value-Maturity Ladder, swissAI-Ressourcen, BEYONDER 68 KI-Use-Cases).

Datenquellen: Stundenplan V1.2 (27.08.2026), Modulaufbau-Matrix, Dozierendenprofile. Alle Daten liegen im ersten `<script>`-Block von `index.html` und lassen sich dort direkt pflegen.

Ordner `pre-reading/`: Vorbereitungspaket für Teilnehmende, neu mit `05-challenge-pitch.md` (Zulassungsbedingung, Abgabe am Ende von Tag 1, 02.09.).

Ordner `downloads/`: HWZ Curriculum-Vorlage (leer), HWZ Präsentationsvorlage (.potx) und unter `downloads/curriculum/` 16 vorbefüllte Curricula, je eines pro Kurstag. Die Seite verlinkt sie relativ; die Ordnerstruktur muss im Repo erhalten bleiben.

Ordner `skills/`: Claude-Skill [cas-ai-unterricht](skills/cas-ai-unterricht/) für Dozierende. Führt geführt vom Briefing (Dozent/in, Kurstag, eigene Inhalte) über Dramaturgie und Übungen bis zur fertig befüllten PowerPoint in der HWZ-Vorlage (`scripts/build_pptx.py`). Nutzung in Claude Code: Ordner als Skill installieren oder den Inhalt von `skills/cas-ai-unterricht/` in ein Claude-Projekt laden. Derselbe Skill wird zusätzlich über den BEYONDER-Marketplace (`BEYONDERnow/claude-marketplace`, privat) verteilt.

**Pflege-Hinweis:** Die Kursdaten (Lernziele, Leitideen, Transfer, FERC, Dozierende) liegen an zwei Orten: im Kurs-Repo (`index.html`, erster Script-Block, plus die Skill-Kopie unter `skills/cas-ai-unterricht/references/`) und im Marketplace-Repo (`plugins/beyonder-skills/skills/cas-ai-unterricht/references/`). Bei Änderungen an Kursdaten immer beide Orte nachführen.
