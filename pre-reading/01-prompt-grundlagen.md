# Prompt-Grundlagen

Pflichtlektüre vor dem ersten Kurstag. Ziel: Du verstehst, wie du ein Sprachmodell präzise steuerst, und hast die Grundtechniken selbst ausprobiert.

## Warum das wichtig ist

Früher musste man ein KI-Modell aufwendig neu trainieren, um es an neue Aufgaben anzupassen. Heute reicht oft ein gut formulierter Prompt. Du gibst damit nicht nur die Aufgabe vor, sondern auch den Kontext, das Format und die Denkweise der KI. Im CAS bauen wir darauf auf: Aus einzelnen Prompts werden wiederverwendbare Skills und ganze Systeme.

## Die Bausteine eines Prompts

| Komponente | Beispiel | Nutzen |
|---|---|---|
| Rolle | «Du bist Marketingleiterin eines Schweizer KMU.» | Perspektive und Fachniveau |
| Kontext | «Der Text stammt aus einem Wirtschaftsmagazin.» | Situative Einbettung |
| Aufgabe | «Fasse den Text in 3 Sätzen zusammen.» | Klare Zielvorgabe |
| Format | «Nutze Bullet Points.» | Steuerung des Outputs |
| Beispiele | «Input: …, Output: …» | Lerneffekt durch Demonstration |

Merke: Langer Kontext gehört an den **Anfang** des Prompts, die eigentliche Aufgabe kommt **zum Schluss**.

## Die vier Grundprinzipien

1. **Kontext ist König.** Gib der KI alle relevanten Hintergrundinformationen. Die häufigste Ursache für schwache Resultate ist fehlender Kontext, nicht ein schlechtes Modell.
2. **Few-Shot Prompting.** Zeige der KI 1 bis 3 Beispiele, statt abstrakt zu beschreiben. Beispiele schlagen Adjektive.
3. **Klarheit gewinnt.** Zerlege grosse Aufgaben in kleine, klare Häppchen. Ein Prompt, eine Aufgabe.
4. **Struktur hilft.** Abschnitte oder Tags wie `<aufgabe>` und `<kontext>` helfen der KI, deinen Prompt sauber zu lesen.

## Die Grundtechniken

| Technik | Was es ist | Wann einsetzen |
|---|---|---|
| Zero-Shot | Aufgabe ohne Beispiele | Einfache Standardaufgaben |
| Few-Shot | Aufgabe mit 1 bis 3 Beispielen | Stil, Format oder Ton vorgeben |
| Chain-of-Thought | KI denkt Schritt für Schritt («Erkläre dein Vorgehen, bevor du antwortest») | Analysen, Rechnungen, komplexe Entscheide |
| Erst fragen, dann arbeiten | «Stelle mir zuerst Rückfragen, bevor du beginnst» | Immer, wenn die KI Kontext von dir braucht |

## Prompt Engineering vs. Context Engineering

Im CAS unterscheiden wir zwei Ebenen. Das eine formuliert den perfekten Befehl, das andere orchestriert die gesamte Informationswelt der KI.

| | Prompt Engineering | Context Engineering |
|---|---|---|
| Fokus | Sprachliche Genauigkeit | Informationsfluss und Systemdesign |
| Geltungsbereich | Einzelner Befehl | Gesamtes System inkl. Werkzeuge |
| Skalierbarkeit | Anfällig bei Komplexität | Stabil über viele Nutzer |

Merke: Das Kontextfenster ist wie teure Bürofläche, jeder Quadratmeter sollte nur mit dem Nützlichsten belegt sein.

## Dos und Don'ts

**Dos**

- Klare Sprache und strukturierte Prompts nutzen
- Kontext angeben und Beispiele einbauen
- Schrittweise an komplexe Aufgaben herangehen
- Eigene Fehler analysieren und Prompts iterativ verfeinern

**Don'ts**

- Zu vage oder allgemein bleiben
- Nur Theorie lesen, ohne zu testen
- Modellantworten ungeprüft übernehmen

## Übungen (ca. 30 Minuten)

1. **Zero- vs. Few-Shot:** Lass dir einen LinkedIn-Post zu einem Fachthema schreiben, einmal ohne, einmal mit zwei Beispiel-Posts von dir. Vergleiche die Resultate.
2. **Kontext-Effekt:** Stelle dieselbe Frage einmal ohne und einmal mit 5 Sätzen Kontext zu deinem Unternehmen. Notiere den Unterschied.
3. **Rückfragen-Technik:** Gib der KI eine Aufgabe mit dem Zusatz «Stelle mir zuerst 5 Rückfragen, bevor du beginnst». Beantworte die Fragen und vergleiche das Ergebnis mit einem Direktversuch.

## Glossar

| Begriff | Erklärung |
|---|---|
| Prompt | Texteingabe zur Steuerung der KI |
| LLM | Large Language Model, grosses Sprachmodell |
| Token | Kleinste Texteinheit, in der ein Modell rechnet |
| Kontextfenster | Menge an Text, die ein Modell gleichzeitig «sieht» |
| Few-Shot | Technik mit Beispielen im Prompt |
| Chain-of-Thought | Denkprozess Schritt für Schritt im Prompt |
| Halluzination | Falsche, aber plausibel klingende KI-Antwort |
| Temperature | Parameter für die Zufälligkeit der Antwort |
| Skill | Wiederverwendbarer Kontext-Baustein (Kern des CAS) |
