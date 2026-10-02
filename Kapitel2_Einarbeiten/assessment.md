---
jupytext:
  formats: md:myst
  text_representation:
    extension: .md
    format_name: myst
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# 🏆Selbsttest: Einarbeiten

````{admonition} Hinweis
:class: hinweis
Diese Übungsaufgaben dienen Ihrer Selbsteinschätzung und helfen Ihnen, das im Kapitel Gelernte zu reflektieren.

Sie können die Fragen in beliebiger Reihenfolge beantworten und auch mehrfach versuchen.

**So funktioniert es:**
- Wählen Sie bei jeder Frage die Antwort(en), die Sie für richtig halten
- Lesen Sie das Feedback zu den einzelnen Antwortoptionen sorgfältig durch
- Die Erklärungen helfen Ihnen, Ihr Verständnis zu vertiefen – auch bei korrekten Antworten

Es erfolgt keine Bewertung oder Speicherung Ihrer Ergebnisse. Nutzen Sie dieses Assessment, um Wissenslücken zu identifizieren und gegebenenfalls die entsprechenden Abschnitte des Kapitels noch einmal zu bearbeiten.

**Geschätzte Zeit**: XX Minuten

Viel Erfolg!
````

## Frage 1

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question1 = [
    {
        "question": "Warum ist es bei der Einarbeitung in ein (fremdes) Forschungsprojekt sinnvoll, zwischen Rohdaten und (aufbereiteten) Forschungsdaten zu unterscheiden?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Weil für beide Datenarten unterschiedliche Fragen zu Format, Entstehung und Dokumentationsstand beantwortet werden müssen, was eine strukturierte Übersicht über den gesamten Datenbestand ermöglicht.",
                "correct": True,
                "feedback": """✓ Richtig! Da Rohdaten und bereits aufbereitete Forschungsdaten unterschiedliche Entstehungs- und Bearbeitungsstadien durchlaufen haben, hilft die getrennte Betrachtung dabei, systematisch zu klären, was überhaupt vorliegt, wie es entstanden ist und was davon bereits dokumentiert oder publiziert ist."""
            },
            {
                "answer": "Weil Rohdaten grundsätzlich nicht veröffentlicht werden dürfen, Forschungsdaten aber immer.",
                "correct": False,
                "feedback": """× Nicht korrekt. Ob eine Veröffentlichung möglich ist, hängt nicht von dieser Unterscheidung ab, sondern von rechtlichen und inhaltlichen Kriterien wie Rechteinhaberschaft, Datenschutz und Qualität."""
            },
            {
                "answer": "Weil nur Forschungsdaten, nicht aber Rohdaten, eine Provenienz besitzen.",
                "correct": False,
                "feedback": """× Nicht korrekt. Auch Rohdaten haben eine nachvollziehbare Herkunft (Provenienz), die dokumentiert werden sollte – unabhängig davon, ob sie bereits weiterverarbeitet wurden."""
            },
            {
                "answer": "Weil diese Unterscheidung gesetzlich vorgeschrieben ist.",
                "correct": False,
                "feedback": """× Nicht korrekt. Es handelt sich um eine praktische, arbeitsorganisatorische Empfehlung zur besseren Strukturierung der Einarbeitung, nicht um eine rechtliche Pflicht."""
            }
        ]
    }
]
display_quiz(question1, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 2

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie die folgenden Beispiele dem jeweils verletzten Qualitätskriterium zu:",
    descriptions=[
        "Eine Exceltabelle zu Messwerten eines chemischen Experiments enthält plötzlich einen durch einen Softwarefehler verzerrten Wert, der nicht der realen Messung entspricht.",
        "In einem Datensatz zu Studienteilnehmenden sind bei vielen Personen die Angaben zum höchsten Bildungsabschluss leer geblieben, da dieses Feld optional war.",
        "Dieselbe Versuchsperson wurde in zwei unterschiedlichen Teilerhebungen einmal mit Großbuchstaben und einmal mit Kleinbuchstaben im Namensfeld erfasst, sodass beim Zusammenführen zwei getrennte Profile entstehen.",
        "Durch ein technisches Problem beim Datenexport wurde derselbe Interviewdatensatz versehentlich doppelt in die Tabelle übernommen.",
        "Ein Feld für das Erhebungsdatum enthält den Eintrag '31.14.2024', der kein gültiges Kalenderdatum darstellt."
    ],
    options=[
        "Genauigkeit",
        "Vollständigkeit",
        "Konsistenz",
        "Eindeutigkeit",
        "Gültigkeit"
    ],
    correct_mapping={
        "Eine Exceltabelle zu Messwerten eines chemischen Experiments enthält plötzlich einen durch einen Softwarefehler verzerrten Wert, der nicht der realen Messung entspricht.": "Genauigkeit",
        "In einem Datensatz zu Studienteilnehmenden sind bei vielen Personen die Angaben zum höchsten Bildungsabschluss leer geblieben, da dieses Feld optional war.": "Vollständigkeit",
        "Dieselbe Versuchsperson wurde in zwei unterschiedlichen Teilerhebungen einmal mit Großbuchstaben und einmal mit Kleinbuchstaben im Namensfeld erfasst, sodass beim Zusammenführen zwei getrennte Profile entstehen.": "Konsistenz",
        "Durch ein technisches Problem beim Datenexport wurde derselbe Interviewdatensatz versehentlich doppelt in die Tabelle übernommen.": "Eindeutigkeit",
        "Ein Feld für das Erhebungsdatum enthält den Eintrag '31.14.2024', der kein gültiges Kalenderdatum darstellt.": "Gültigkeit"
    }
)
```

## Frage 3

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question3 = [
    {
        "question": "Ein Datensatz zur Körpergröße von erwachsenen Studienteilnehmenden ist technisch korrekt formatiert (Zahl, keine Sonderzeichen, richtige Spalte), enthält jedoch einen Eintrag von '3,50 Metern'. Um welche Art von Qualitätsproblem handelt es sich hierbei vor allem?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Ein semantisches Problem: Der Wert ist zwar syntaktisch korrekt formatiert, aber inhaltlich unmöglich bzw. unplausibel.",
                "correct": True,
                "feedback": """✓ Richtig! Syntax und Semantik sind zwei unterschiedliche Qualitätsebenen: Syntaktisch ist der Wert einwandfrei (eine gültige Zahl im richtigen Format), aber inhaltlich ist er nicht plausibel, da kein erwachsener Mensch 3,50 Meter groß ist. Genau solche Fälle zeigen, dass korrekte Formatierung allein nicht ausreicht, um Datenqualität zu gewährleisten."""
            },
            {
                "answer": "Ein syntaktisches Problem, da die Maschinenlesbarkeit des Datensatzes beeinträchtigt ist.",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Maschinenlesbarkeit ist hier nicht beeinträchtigt – der Wert lässt sich technisch problemlos verarbeiten. Das Problem liegt auf der inhaltlichen, nicht auf der formalen Ebene."""
            },
            {
                "answer": "Es handelt sich um kein Qualitätsproblem, da der Wert korrekt formatiert vorliegt.",
                "correct": False,
                "feedback": """× Nicht korrekt. Korrekte Formatierung schützt nicht automatisch vor inhaltlich unplausiblen Werten. Auch formal einwandfreie Daten können ein ernstzunehmendes Qualitätsproblem darstellen."""
            },
            {
                "answer": "Ein Problem der Lizenzierung, da unklare Werte rechtlich nicht veröffentlicht werden dürfen.",
                "correct": False,
                "feedback": """× Nicht korrekt. Lizenzfragen betreffen die rechtliche Nutzbarkeit von Daten, nicht die inhaltliche Plausibilität einzelner Werte. Dieses Problem ist ein Datenqualitäts-, kein Lizenzproblem."""
            }
        ]
    }
]
display_quiz(question3, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 4

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question4 = [
    {
        "question": "Welche der folgenden sind typische, automatisierbare Prüfungen zur Bewertung von Datenqualität? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Bereichsprüfung: Kontrolle, ob numerische Werte innerhalb eines erwarteten Wertebereichs liegen.",
                "correct": True,
                "feedback": """✓ Richtig! Eine Bereichsprüfung erkennt Ausreißer, die außerhalb eines plausiblen Wertebereichs liegen, z. B. unrealistisch hohe oder niedrige Messwerte."""
            },
            {
                "answer": "Nullwertprüfung: Kontrolle, ob und wie viele leere Felder in einer Spalte vorhanden sind.",
                "correct": True,
                "feedback": """✓ Richtig! Diese Prüfung stellt sicher, dass fehlende Werte erkannt werden – entweder, indem keine Nullwerte zugelassen werden, oder indem ein maximal akzeptabler Anteil definiert wird."""
            },
            {
                "answer": "Datentypprüfung: Kontrolle, ob ein Feld den erwarteten Datentyp aufweist (z. B. Zahl statt Text).",
                "correct": True,
                "feedback": """✓ Richtig! Diese Prüfung ist besonders wichtig, wenn Daten ohne Spaltenüberschriften importiert werden, da sich dabei unbemerkt die Spaltenreihenfolge verschieben kann."""
            },
            {
                "answer": "Stilprüfung: Kontrolle, ob eine einheitliche Zitierweise in der zugehörigen Publikation verwendet wurde.",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Zitierweise einer Publikation betrifft nicht die Qualität des Datensatzes selbst, sondern die Textgestaltung eines begleitenden Artikels. Dies ist keine der im Data Engineering üblichen Datenqualitätsprüfungen."""
            },
            {
                "answer": "Eindeutigkeitsprüfung: Kontrolle, ob Werte in einer ID-Spalte wirklich einzigartig sind.",
                "correct": True,
                "feedback": """✓ Richtig! Diese Prüfung stellt sicher, dass es z. B. in einer ID-Spalte keine doppelten Einträge gibt, was für die eindeutige Zuordnung von Datensätzen essenziell ist."""
            }
        ]
    }
]
display_quiz(question4, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 5

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question5 = [
    {
        "question": "In einem Finanzdatensatz tauchen üblicherweise Transaktionen zwischen 10 und 2.000 Euro auf. Plötzlich erscheint ein einzelner Eintrag über 500.000 Euro. Welche Art von automatisierter Prüfung würde diese Abweichung am ehesten aufdecken?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Eine Bereichsprüfung, da der Wert deutlich außerhalb des üblichen, erwarteten Wertebereichs liegt.",
                "correct": True,
                "feedback": """✓ Richtig! Genau für solche Fälle ist die Bereichsprüfung gedacht: Werte, die den typischen Rahmen deutlich sprengen, werden markiert – unabhängig davon, ob es sich um einen Fehler oder einen tatsächlich besonderen Fall handelt, der genauer untersucht werden sollte."""
            },
            {
                "answer": "Eine Kategorieprüfung, da ein neuer Betragstyp eingeführt wurde.",
                "correct": False,
                "feedback": """× Nicht korrekt. Kategorieprüfungen betreffen Werte, die zu einer festen, begrenzten Gruppe von zulässigen Einträgen gehören sollen (z. B. Länderkürzel), nicht numerische Ausreißer bei Beträgen."""
            },
            {
                "answer": "Eine Nullwertprüfung, da ein fehlender Wert vorliegt.",
                "correct": False,
                "feedback": """× Nicht korrekt. In diesem Fall liegt kein fehlender, sondern ein vorhandener, aber unplausibel hoher Wert vor. Eine Nullwertprüfung würde hier nicht greifen."""
            },
            {
                "answer": "Eine Aktualitätsprüfung, da der Eintrag zu einem ungewöhnlichen Zeitpunkt erfolgte.",
                "correct": False,
                "feedback": """× Nicht korrekt. Aktualitätsprüfungen betreffen die Frage, wie lange die letzte Datenaktualisierung zurückliegt, nicht die Plausibilität einzelner Werte."""
            }
        ]
    }
]
display_quiz(question5, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 6

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz2 = DragDropQuiz()

quiz2.create_matching_quiz(
    title="Ordnen Sie die folgenden Beschreibungen der passenden Stufe des Medaillon-Schemas zu:",
    descriptions=[
        "Die Daten werden möglichst unverändert aus der Originalquelle übernommen, um Nachvollziehbarkeit und Historie zu bewahren.",
        "Fehlerhafte oder doppelte Einträge werden entfernt, Formate vereinheitlicht und erste Qualitätsprüfungen durchgeführt.",
        "Die Daten werden gezielt aggregiert und für eine konkrete Analyse oder Visualisierung aufbereitet."
    ],
    options=[
        "Bronze-Stufe",
        "Silber-Stufe",
        "Gold-Stufe"
    ],
    correct_mapping={
        "Die Daten werden möglichst unverändert aus der Originalquelle übernommen, um Nachvollziehbarkeit und Historie zu bewahren.": "Bronze-Stufe",
        "Fehlerhafte oder doppelte Einträge werden entfernt, Formate vereinheitlicht und erste Qualitätsprüfungen durchgeführt.": "Silber-Stufe",
        "Die Daten werden gezielt aggregiert und für eine konkrete Analyse oder Visualisierung aufbereitet.": "Gold-Stufe"
    }
)
```

## Frage 7

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question7 = [
    {
        "question": "Ein Datensatz zu Pflanzenwachstum enthält eine Tabelle, in der für jede Pflanze eine eigene Spalte existiert und die gemessenen Werte (Höhe, Woche, Behandlungsgruppe) in den Zeilen darunter vermischt eingetragen sind. Was müsste verändert werden, damit die Tabelle dem Tidy-Data-Prinzip entspricht?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die Tabelle müsste so umstrukturiert werden, dass jede Variable (z. B. Pflanze, Woche, Höhe, Behandlungsgruppe) eine eigene Spalte bildet und jede Beobachtung eine eigene Zeile.",
                "correct": True,
                "feedback": """✓ Richtig! Das Tidy-Data-Prinzip verlangt, dass jede Variable in einer eigenen Spalte steht, jede Beobachtung eine eigene Zeile bildet und jeder Wert eindeutig einer Variable und einer Beobachtung zugeordnet werden kann. Wenn stattdessen jede Pflanze eine eigene Spalte bildet, sind Variablen und Beobachtungen vermischt, was die maschinelle Weiterverarbeitung erschwert."""
            },
            {
                "answer": "Die Tabelle müsste in ein Bildformat statt eines Tabellenformats umgewandelt werden.",
                "correct": False,
                "feedback": """× Nicht korrekt. Das Tidy-Data-Prinzip betrifft die interne Struktur einer Tabelle, nicht das Dateiformat. Ein Bildformat wäre für die maschinelle Weiterverarbeitung sogar deutlich ungeeigneter."""
            },
            {
                "answer": "Es müssten zusätzliche Farbmarkierungen eingefügt werden, um besondere Werte hervorzuheben.",
                "correct": False,
                "feedback": """× Nicht korrekt. Rein visuelle Formatierungen wie Farbmarkierungen werden beim Tidy-Data-Prinzip sogar ausdrücklich vermieden, da sie die maschinelle Weiterverarbeitung erschweren können."""
            },
            {
                "answer": "Es müsste eine zusätzliche Berechnungsspalte mit dem Durchschnittswert aller Pflanzen ergänzt werden.",
                "correct": False,
                "feedback": """× Nicht korrekt. Berechnungen sollten gerade nicht direkt im Rohdatensatz vorgenommen werden, da dies die spätere maschinelle Weiterverarbeitung erschweren kann. Solche Auswertungen gehören eher in einen separaten Analyseschritt."""
            }
        ]
    }
]
display_quiz(question7, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 8

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question8 = [
    {
        "question": "Welche Aspekte sollten vor der Veröffentlichung von Forschungsdaten rechtlich bzw. organisatorisch geprüft werden? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Wer die Rechte an den Daten innehat (z. B. Urheberrecht oder Datenbankherstellerrecht).",
                "correct": True,
                "feedback": """✓ Richtig! Da es in Deutschland kein allgemeines Eigentum an Daten gibt, muss im Einzelfall geprüft werden, welche Schutzrechte (Urheberrecht, Datenbankherstellerrecht) bestehen und bei wem diese liegen."""
            },
            {
                "answer": "Ob Vorgaben von Förderorganisationen zum Umgang mit den Forschungsdaten bestehen.",
                "correct": True,
                "feedback": """✓ Richtig! Förderorganisationen wie die DFG oder europäische Programme stellen eigene Anforderungen an Dokumentation, Archivierung und Veröffentlichung, die auch nachträglich noch relevant sein können."""
            },
            {
                "answer": "Ob die Daten personenbezogene Informationen enthalten.",
                "correct": True,
                "feedback": """✓ Richtig! Enthaltene personenbezogene Daten können einer Veröffentlichung entgegenstehen oder zusätzliche Schutzmaßnahmen erfordern, weshalb dies frühzeitig geprüft werden sollte."""
            },
            {
                "answer": "Wie viele Wörter das zugehörige Abstract der geplanten Publikation umfasst.",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Wortanzahl eines Abstracts ist keine rechtliche oder organisatorische Voraussetzung für die Veröffentlichung von Forschungsdaten."""
            },
            {
                "answer": "Ob Vorgaben des Zieljournals oder -repositoriums zu Format, Metadaten und Lizenzierung erfüllt sind.",
                "correct": True,
                "feedback": """✓ Richtig! Journale und Repositorien stellen unterschiedliche Anforderungen an Datenformat, Metadaten und Lizenzierung, die vor einer Veröffentlichung abgeglichen werden sollten."""
            }
        ]
    }
]
display_quiz(question8, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 9

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question9 = [
    {
        "question": "Für die Lizenzierung von Forschungsdaten wird häufig zwischen reinen Datensätzen/Datenbanken und Daten mit Werkqualität unterschieden. Welche Zuordnung von empfohlenen Lizenzen ist korrekt?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Für reine Datensätze/Datenbanken wird häufig eine Public-Domain-Widmung wie CC0 empfohlen, für Daten mit Werkqualität eine Namensnennungslizenz wie CC BY 4.0.",
                "correct": True,
                "feedback": """✓ Richtig! Diese Unterscheidung wird u. a. von der DFG empfohlen: Reine Datensätze profitieren von einer möglichst unkomplizierten Public-Domain-Widmung (CC0), während bei Daten mit Werkqualität eine Namensnennung (CC BY 4.0) sinnvoll ist, um die Urheberschaft kenntlich zu machen."""
            },
            {
                "answer": "Für reine Datensätze/Datenbanken wird eine Namensnennungslizenz wie CC BY 4.0 empfohlen, für Daten mit Werkqualität CC0.",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Zuordnung ist genau umgekehrt: CC0 eignet sich eher für reine Datensätze, CC BY 4.0 eher für Daten mit Werkqualität."""
            },
            {
                "answer": "Für beide Datenarten wird ausschließlich eine kommerzielle Lizenz empfohlen.",
                "correct": False,
                "feedback": """× Nicht korrekt. Sowohl CC0 als auch CC BY 4.0 sind offene, nicht-kommerzielle Lizenzmodelle. Eine kommerzielle Lizenz wird in diesem Kontext nicht empfohlen."""
            },
            {
                "answer": "Die Art der Lizenz spielt keine Rolle, solange die Daten überhaupt veröffentlicht werden.",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Lizenzwahl ist entscheidend für die rechtssichere Nachnutzung der Daten durch Dritte und sollte daher bewusst und passend zur Art der Daten getroffen werden."""
            }
        ]
    }
]
display_quiz(question9, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 10

Die folgenden drei Fragen prüfen grundlegende rechtliche Aussagen zur Publikation von Forschungsdaten. Entscheiden Sie jeweils, ob die Aussage richtig oder falsch ist.

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question10 = [
    {
        "question": "In Deutschland existiert ein allgemeines gesetzliches Eigentumsrecht an Daten.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": False,
                "feedback": """× Nicht korrekt. Im deutschen Recht gibt es kein allgemeines Eigentum an Daten. Stattdessen können Forschungsdaten unterschiedlichen, spezifischeren Schutzrechten unterliegen, etwa dem Urheberrecht oder dem Datenbankherstellerrecht."""
            },
            {
                "answer": "Falsch",
                "correct": True,
                "feedback": """✓ Richtig! Die Aussage ist falsch. Ein allgemeines Eigentum an Daten existiert im deutschen Recht nicht. Stattdessen muss im Einzelfall geprüft werden, ob und welche spezifischen Schutzrechte (z. B. Urheberrecht, Datenbankherstellerrecht) an den jeweiligen Daten bestehen."""
            }
        ]
    }
]
display_quiz(question10, colors=colors.jupyterquiz, max_width=1000)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question10b = [
    {
        "question": "Eine einmal vergebene Lizenz für veröffentlichte Forschungsdaten lässt sich in der Regel problemlos nachträglich ändern oder widerrufen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": False,
                "feedback": """× Nicht korrekt. Genau das Gegenteil ist der Fall: Eine einmal vergebene Lizenz lässt sich in der Regel nicht nachträglich ändern oder widerrufen. Deshalb sollte die Lizenzwahl sorgfältig und in Abstimmung mit allen Rechteinhaber:innen erfolgen, bevor die Daten veröffentlicht werden."""
            },
            {
                "answer": "Falsch",
                "correct": True,
                "feedback": """✓ Richtig! Die Aussage ist falsch. Eine einmal vergebene Lizenz kann in der Regel nicht nachträglich geändert oder widerrufen werden, da Dritte die Daten bereits unter den ursprünglichen Bedingungen genutzt haben könnten. Die Lizenzwahl sollte daher vor der Veröffentlichung sorgfältig abgestimmt werden."""
            }
        ]
    }
]
display_quiz(question10b, colors=colors.jupyterquiz, max_width=1000)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question10c = [
    {
        "question": "Empirische Untersuchungen zeigen, dass verpflichtende Archivierungsrichtlinien von Journalen die tatsächliche Verfügbarkeit von Forschungsdaten deutlich stärker erhöhen als unverbindliche Empfehlungen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": True,
                "feedback": """✓ Richtig! Studien zeigen, dass verpflichtende Richtlinien (wie die Joint Data Archiving Policy) die tatsächliche Bereitstellung von Forschungsdaten deutlich erhöhen, während rein unverbindliche Empfehlungen kaum Wirkung zeigen. Dies verdeutlicht, wie wichtig verbindliche Vorgaben für die tatsächliche Umsetzung von Open-Data-Prinzipien sind."""
            },
            {
                "answer": "Falsch",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Aussage ist richtig: Verpflichtende Archivierungsrichtlinien zeigen nachweislich eine deutlich stärkere Wirkung auf die tatsächliche Datenverfügbarkeit als unverbindliche Empfehlungen."""
            }
        ]
    }
]
display_quiz(question10c, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 11

**Frage:** Sie übernehmen einen alten, kaum dokumentierten Datensatz aus einem bereits abgeschlossenen Projekt, der nachträglich veröffentlicht werden soll.

1. Welche Schritte würden Sie zur Prüfung der Datenqualität unternehmen, bevor Sie den Datensatz für publikationsreif halten?
2. Welche rechtlichen bzw. organisatorischen Fragen müssten Sie vorher klären, bevor eine Veröffentlichung überhaupt möglich ist?

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('einarbeiten-1')
```

````{admonition} Reflexionshinweise
:class: solution, dropdown

**1. Schritte zur Qualitätsprüfung:**

- Zunächst den Projektkontext nachvollziehen: Aus welchem Projekt stammen die Daten, wer war beteiligt, in welchem Zeitraum wurden sie erhoben?
- Zwischen Rohdaten und bereits aufbereiteten Forschungsdaten unterscheiden und für beide den Dokumentationsstand prüfen.
- Die fünf zentralen Qualitätskriterien prüfen: Genauigkeit, Vollständigkeit, Konsistenz, Eindeutigkeit und Gültigkeit.
- Typische automatisierte Prüfungen anwenden, soweit möglich: Bereichsprüfung, Nullwertprüfung, Datentypprüfung, Eindeutigkeitsprüfung.
- Prüfen, ob die Datenstruktur dem Tidy-Data-Prinzip entspricht (eine Variable pro Spalte, eine Beobachtung pro Zeile) und ob Rohdatensätze frei von Berechnungen oder rein visuellen Formatierungen sind.
- Wenn möglich, eine für die Herkunft und Entstehung zuständige Person (z. B. ehemalige Projektleitung) einbeziehen, um Unklarheiten zu klären.

**2. Zu klärende rechtliche/organisatorische Fragen:**

- Wer die Rechte an den Daten hält (Urheberrecht, Datenbankherstellerrecht, Nutzungsrechte der Institution).
- Ob personenbezogene Daten enthalten sind und ob diese anonymisiert oder ausgeschlossen werden müssen.
- Ob Vorgaben des ursprünglichen Förderers (z. B. zu Archivierungsdauer oder Repositoriumswahl) noch gelten und erfüllt sind.
- Ob institutionelle Vorgaben oder Kooperationsvereinbarungen die Veröffentlichung regeln.
- Ob fachspezifische Standards oder Repositorien für die jeweilige Disziplin existieren und genutzt werden sollten.
- Unter welcher Lizenz die Daten veröffentlicht werden sollen – diese Entscheidung sollte vor der Veröffentlichung sorgfältig und abgestimmt getroffen werden, da sie i. d. R. nicht nachträglich revidierbar ist.

Da mehrere dieser Fragen nicht allein von einer einzelnen Person zu klären sind, kann die frühzeitige Einbindung von FDM-Services, Rechtsabteilung oder (ehemaligen) Projektverantwortlichen die nachträgliche Veröffentlichung erheblich erleichtern.
````
