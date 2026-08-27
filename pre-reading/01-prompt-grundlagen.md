# Prompt-Grundlagen

Pflichtlektüre vor dem ersten Kurstag. Ziel: Du verstehst, wie du ein Sprachmodell präzise steuerst, kennst das CORE+-Schema als gemeinsames Vokabular des CAS und hast die Grundtechniken selbst ausprobiert.

## Warum das wichtig ist

Ein Sprachmodell ist ein Gegenüber, das gebrieft werden will. Wer eine Agentur oder Freelancer sauber briefen kann, kann auch ein Sprachmodell briefen. Im CAS bauen wir darauf auf: Aus einzelnen Prompts werden Master-Prompts, Chains und ganze Systeme, alle für deine eigene Marketing-Challenge.

## CORE+: das Briefing-Schema des CAS

CORE+ ist das gemeinsame Vokabular ab Tag 1. Es ist ein Kreativ-Briefing in fünf Feldern:

| Feld | Bedeutet | Beispiel |
|---|---|---|
| **C** Character | Rolle und Perspektive der KI | «Du bist Marketingleiterin eines Schweizer KMU.» |
| **O** Objective | Ziel der Aufgabe | «Erstelle 3 Betreffzeilen, die die Öffnungsrate erhöhen.» |
| **R** Rules | Regeln und Grenzen | «Maximal 45 Zeichen, kein Ausrufezeichen, per Sie.» |
| **E** Example | Beispiele für das Gewünschte | «So klingt eine gute Betreffzeile von uns: …» |
| **+** Talk | Dialog statt Einwegbefehl | «Stelle mir zuerst Rückfragen, bevor du beginnst.» |

Merke: Langer Kontext gehört an den **Anfang** des Prompts, die eigentliche Aufgabe kommt **zum Schluss**. Und das «+» ist der am meisten unterschätzte Teil: Lass dich von der KI interviewen, bevor sie arbeitet.

## Die vier Grundprinzipien

1. **Kontext ist König.** Gib der KI alle relevanten Hintergrundinformationen. Die häufigste Ursache für schwache Resultate ist fehlender Kontext, nicht ein schlechtes Modell.
2. **Beispiele schlagen Adjektive.** Zeige der KI 1 bis 3 Beispiele (Few-Shot), statt abstrakt zu beschreiben, was du willst.
3. **Klarheit gewinnt.** Zerlege grosse Aufgaben in kleine, klare Häppchen (Chunking). Ein Prompt, eine Aufgabe.
4. **Struktur hilft.** Abschnitte oder Tags wie `<aufgabe>` und `<kontext>` helfen der KI, deinen Prompt sauber zu lesen. An Tag 3 treiben wir das mit JSON- und XML-Prompts weiter.

## Die Grundtechniken

| Technik | Was es ist | Wann einsetzen |
|---|---|---|
| Zero-Shot | Aufgabe ohne Beispiele | Einfache Standardaufgaben |
| Few-Shot | Aufgabe mit 1 bis 3 Beispielen | Stil, Format oder Ton vorgeben |
| Chain-of-Thought | KI denkt Schritt für Schritt («Erkläre dein Vorgehen, bevor du antwortest») | Analysen, Rechnungen, komplexe Entscheide |
| Reverse Prompt Engineering | Gutes Ergebnis rein, Prompt raus | Du weisst, wie das Resultat aussehen soll, aber nicht, wie du hinkommst (Tag 1) |
| Deep Research | KI recherchiert mehrstufig mit Quellen | Recherche-Vorstufe für präzise Prompts (Tag 3) |

## FERC: der Arbeitsrhythmus des CAS

Neben CORE+ (wie du briefst) nutzt der CAS FERC (wie du arbeitest und reflektierst): **Frame, Explore, Refine, Commit.** Ziel setzen, Alternativen erzeugen, vergleichen, verantwortet entscheiden. Jeder Kurstag folgt diesem Rhythmus an deiner eigenen Challenge, und nach Tag 3 schreibst du dazu eine benotete FERC-Reflexion. Du musst FERC vor Kursstart nicht üben, nur den Gedanken kennen: Nie die erste Antwort nehmen, immer Varianten erzeugen und begründet wählen.

## Dos und Don'ts

**Dos**

- Klare Sprache und strukturierte Prompts nutzen
- Kontext angeben und Beispiele einbauen
- Varianten erzeugen und vergleichen, statt die erste Antwort zu nehmen
- Eigene Fehler analysieren und Prompts iterativ verfeinern

**Don'ts**

- Zu vage oder allgemein bleiben
- Nur Theorie lesen, ohne zu testen
- Modellantworten ungeprüft übernehmen
- Kundendaten oder Personendaten in Consumer-Abos eingeben (mehr dazu an Tag 4)

## Übungen (ca. 30 Minuten)

1. **CORE+ komplett:** Nimm eine echte Aufgabe aus deinem Marketingalltag und schreibe einen Prompt mit allen fünf CORE+-Feldern. Vergleiche das Resultat mit einem Einzeiler-Prompt zur selben Aufgabe.
2. **Few-Shot-Effekt:** Lass dir einen LinkedIn-Post zu einem Fachthema schreiben, einmal ohne, einmal mit zwei Beispiel-Posts von dir. Notiere den Unterschied.
3. **Talk-Technik:** Gib der KI eine Aufgabe mit dem Zusatz «Stelle mir zuerst 5 Rückfragen, bevor du beginnst». Beantworte die Fragen und vergleiche das Ergebnis mit dem Direktversuch.
4. **Mini-FERC:** Lass dir zu Übung 1 drei Varianten geben, wähle die beste und notiere in einem Satz, warum. Genau das machst du ab Tag 1 an deiner Challenge.

## Glossar

| Begriff | Erklärung |
|---|---|
| Prompt | Texteingabe zur Steuerung der KI |
| LLM | Large Language Model, grosses Sprachmodell |
| Token | Kleinste Texteinheit, in der ein Modell rechnet |
| Kontextfenster | Menge an Text, die ein Modell gleichzeitig «sieht» |
| CORE+ | Briefing-Schema des CAS: Character, Objective, Rules, Example, + Talk |
| FERC | Arbeitsrhythmus des CAS: Frame, Explore, Refine, Commit |
| Chunking | Grosse Aufgaben in kleine, klare Teilschritte zerlegen |
| Few-Shot | Technik mit Beispielen im Prompt |
| Chain-of-Thought | Denkprozess Schritt für Schritt im Prompt |
| Master-Prompt | Wiederverwendbarer Kontext-Container, kommt an Tag 3 |
| Prompt-Chain | Mehrere Prompts als Produktionskette, kommt an Tag 3 |
| Halluzination | Falsche, aber plausibel klingende KI-Antwort |
| RAG | Retrieval-Augmented Generation, KI antwortet aus deinen Daten (Tag 9) |
