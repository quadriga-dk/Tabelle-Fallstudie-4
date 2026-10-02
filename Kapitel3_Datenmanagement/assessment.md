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

# 🏆Selbsttest: Datenmanagement
````{admonition} Hinweis
:class: hinweis, dropdown
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
        "question": "Welche der folgenden Bestandteile gehören zur Erstellung eines Datenmanagementplans (DMP) im Rahmen einer nachträglichen Datenpublikation? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Auswahl und Clusterung der zu veröffentlichenden Forschungsdaten.",
                "correct": True,
                "feedback": """✓ Richtig! Zunächst muss entschieden werden, welche Daten überhaupt veröffentlicht und wie sie sinnvoll gebündelt werden (z. B. als Gesamt-ZIP oder in einzelnen Paketen)."""
            },
            {
                "answer": "Eine einheitliche Dateibenennung nach einem erkennbaren Schema.",
                "correct": True,
                "feedback": """✓ Richtig! Die Prüfung und ggf. Anpassung der Dateibenennung ist ein zentraler Bestandteil, damit Daten auch projekt-extern verständlich bleiben."""
            },
            {
                "answer": "Die Vergabe von Metadaten nach den Konventionen der jeweiligen Fachdisziplin.",
                "correct": True,
                "feedback": """✓ Richtig! Metadaten müssen vergeben werden, sofern dies nicht bereits geschehen ist – möglichst orientiert an etablierten disziplinspezifischen Standards."""
            },
            {
                "answer": "Die FAIRifizierung der Daten und Metadaten zur Maximierung der Interoperabilität.",
                "correct": True,
                "feedback": """✓ Richtig! Daten und Metadaten sollten möglichst vollständig beschrieben werden, wobei nach Möglichkeit auf Standards zurückgegriffen wird, um die Interoperabilität zu erhöhen."""
            },
            {
                "answer": "Die Erstellung eines Marketingkonzepts zur Bewerbung der Datenpublikation.",
                "correct": False,
                "feedback": """× Nicht korrekt. Ein Marketingkonzept ist kein Bestandteil eines Datenmanagementplans. Die DMP-Bestandteile betreffen die Organisation, Beschreibung und Dokumentation der Daten selbst, nicht deren Vermarktung."""
            },
            {
                "answer": "Das Anlegen einer README-Datei zur Dokumentation der Daten.",
                "correct": True,
                "feedback": """✓ Richtig! Eine README-Datei gehört ebenfalls zu den Bestandteilen, da sie als einfache, grundlegende Form der Datendokumentation dient."""
            }
        ]
    }
]
display_quiz(question1, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 2

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question2 = [
    {
        "question": "Was unterscheidet eine README-Datei am ehesten von der FAIRifizierung eines Datensatzes?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Die README ist eine einfache, frei formulierte Dokumentationsdatei für menschliche Leser:innen, während die FAIRifizierung eine systematischere, standardbasierte Beschreibung zur Maximierung der maschinellen Interoperabilität anstrebt.",
                "correct": True,
                "feedback": """✓ Richtig! Die README gilt als die einfachste Form der Datendokumentation und dient vor allem dem Verständnis durch Menschen. Die FAIRifizierung geht darüber hinaus: Sie zielt auf eine möglichst vollständige, standardisierte Beschreibung ab, die auch die maschinelle Verarbeitung und Verknüpfung der Daten erleichtert."""
            },
            {
                "answer": "Beide Begriffe bezeichnen exakt denselben Arbeitsschritt und können synonym verwendet werden.",
                "correct": False,
                "feedback": """× Nicht korrekt. Es handelt sich um zwei unterschiedliche, sich ergänzende Schritte: Eine README ersetzt nicht die standardisierte, disziplinspezifische Beschreibung, die im Rahmen der FAIRifizierung angestrebt wird."""
            },
            {
                "answer": "Die README betrifft nur Rohdaten, während die FAIRifizierung nur für bereits publizierte Forschungsdaten gilt.",
                "correct": False,
                "feedback": """× Nicht korrekt. Diese Unterscheidung wird im Kapitel nicht getroffen. Beide Maßnahmen können grundsätzlich auf denselben Datensatz angewendet werden, unabhängig von seinem Publikationsstatus."""
            },
            {
                "answer": "Die FAIRifizierung ist ausschließlich eine rechtliche Anforderung, die README hingegen eine rein technische.",
                "correct": False,
                "feedback": """× Nicht korrekt. Weder die README noch die FAIRifizierung sind primär rechtliche Anforderungen – beide dienen der besseren Dokumentation und Nachnutzbarkeit von Forschungsdaten."""
            }
        ]
    }
]
display_quiz(question2, colors=colors.jupyterquiz, max_width=1000)
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
        "question": "Warum wird empfohlen, bei der Vergabe von Metadaten die Konventionen der jeweiligen Fachdisziplin zu beachten, anstatt einen einzigen allgemeinen Standard für alle Fachrichtungen zu verwenden?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Weil sich in verschiedenen Fachdisziplinen bereits etablierte, spezialisierte Metadatenstandards entwickelt haben, die die jeweiligen fachspezifischen Informationsbedürfnisse und Interoperabilitätsanforderungen besser abbilden als ein allgemeiner Standard.",
                "correct": True,
                "feedback": """✓ Richtig! Fachdisziplinen wie die Sozialwissenschaften oder die Biodiversitätsforschung haben eigene Standards entwickelt (z. B. DDI oder Darwin Core), die auf die jeweiligen fachlichen Anforderungen zugeschnitten sind. Die Verwendung dieser etablierten Standards erleichtert den fachspezifischen Austausch und die Nachnutzung innerhalb der jeweiligen Community."""
            },
            {
                "answer": "Weil allgemeine, fachübergreifende Metadatenstandards grundsätzlich nicht existieren.",
                "correct": False,
                "feedback": """× Nicht korrekt. Es gibt durchaus fachübergreifende Standards wie das DataCite Metadata Schema. Die Empfehlung zur disziplinspezifischen Orientierung schließt solche übergreifenden Standards nicht aus, sondern ergänzt sie um fachspezifische Tiefe, wo sinnvoll."""
            },
            {
                "answer": "Weil fachspezifische Metadatenstandards gesetzlich vorgeschrieben sind.",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Nutzung disziplinspezifischer Standards ist eine fachliche Empfehlung zur besseren Nachnutzbarkeit, keine gesetzliche Pflicht."""
            },
            {
                "answer": "Weil allgemeine Standards technisch nicht mit Repositorien kompatibel sind.",
                "correct": False,
                "feedback": """× Nicht korrekt. Technische Inkompatibilität wird im Kapitel nicht als Grund genannt. Der Kerngedanke ist, dass fachspezifische Standards die besonderen inhaltlichen Anforderungen einer Disziplin präziser abbilden können."""
            }
        ]
    }
]
display_quiz(question3, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 4

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie jedem Bestandteil eines Datenmanagementplans die passende Beschreibung zu:",
    descriptions=[
        "Festlegen, welche Daten veröffentlicht werden sollen und wie sie sinnvoll zu Paketen gebündelt werden",
        "Ein einheitliches, nachvollziehbares Schema zur Benennung von Dateien festlegen",
        "Beschreibung der Daten nach den Konventionen der jeweiligen Fachdisziplin",
        "Möglichst vollständige, standardisierte Beschreibung zur Maximierung der Interoperabilität",
        "Eine einfache Dokumentationsdatei, die Nachnutzenden das Verständnis der Daten ermöglicht"
    ],
    options=[
        "Auswahl und Clusterung",
        "Dateibenennung",
        "Metadaten",
        "FAIRifizierung",
        "README"
    ],
    correct_mapping={
        "Festlegen, welche Daten veröffentlicht werden sollen und wie sie sinnvoll zu Paketen gebündelt werden": "Auswahl und Clusterung",
        "Ein einheitliches, nachvollziehbares Schema zur Benennung von Dateien festlegen": "Dateibenennung",
        "Beschreibung der Daten nach den Konventionen der jeweiligen Fachdisziplin": "Metadaten",
        "Möglichst vollständige, standardisierte Beschreibung zur Maximierung der Interoperabilität": "FAIRifizierung",
        "Eine einfache Dokumentationsdatei, die Nachnutzenden das Verständnis der Daten ermöglicht": "README"
    }
)
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
        "question": "Welche der folgenden Empfehlungen gelten als Best Practice bei der nachträglichen Erstellung eines Datenmanagementplans aus Sicht von Forschenden? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Bestehende Projektstrukturen und Benennungslogiken sollten möglichst übernommen werden, statt sie komplett neu zu erfinden.",
                "correct": True,
                "feedback": """✓ Richtig! Strukturen und Benennungen, die im Projekt bereits entstanden sind, folgen in der Regel einer eigenen Logik. Diese möglichst zu übernehmen, spart Aufwand und erhält die Nachvollziehbarkeit."""
            },
            {
                "answer": "Die Dateibenennung sollte frühzeitig und sorgfältig festgelegt werden, da nachträgliche Anpassungen mühsam sind und zu Verständigungsproblemen führen können.",
                "correct": True,
                "feedback": """✓ Richtig! Eine zentrale Erfahrung ist, dass eine spätere Anpassung der Dateibenennung sehr aufwendig ist. Wird früh auf ein einheitliches Schema geachtet, lassen sich solche Probleme vermeiden."""
            },
            {
                "answer": "Überlegungen zur Bereitstellungsform (z. B. als Gesamt-ZIP oder in Teil-Paketen) sollten bereits frühzeitig mitgedacht werden.",
                "correct": True,
                "feedback": """✓ Richtig! Die Entscheidung über die Form der Bereitstellung (einzeln, als Gesamt-ZIP oder in Teil-Paketen) hängt eng mit der Auswahl und Clusterung der Daten zusammen und sollte daher früh bedacht werden."""
            },
            {
                "answer": "Versionierung und Dateibenennung sind nur bei der Erstveröffentlichung eines Datensatzes relevant, nicht aber bei einer nachträglichen Aufarbeitung.",
                "correct": False,
                "feedback": """× Nicht korrekt. Im Gegenteil: Gerade bei einer nachträglichen Aufarbeitung sind Versionierung und Dateibenennung besonders gefragte Kompetenzen, da hier oft uneinheitliche oder unvollständige Ausgangsstrukturen vorliegen."""
            },
            {
                "answer": "Es ist unproblematisch, wenn verschiedene Projektpartner Dateien völlig unabhängig voneinander und ohne Abstimmung benennen.",
                "correct": False,
                "feedback": """× Nicht korrekt. Unterschiedliche, nicht abgestimmte Benennungen durch mehrere Partner führen in der Praxis häufig dazu, dass am Ende viel nachträglich vereinheitlicht werden muss – ein Umstand, der durch frühzeitige Absprache vermeidbar wäre."""
            }
        ]
    }
]
display_quiz(question5, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 6

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question6 = [
    {
        "question": "Ein Forschungsteam möchte mehrere Jahre nach Projektende Daten nachträglich veröffentlichen und stellt fest, dass verschiedene ehemalige Projektpartner ihre Dateien jeweils nach eigenen, unterschiedlichen Schemata benannt haben. Was legt die im Kapitel vermittelte Praxiserfahrung nahe?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Solche uneinheitlichen Benennungen müssen in der Regel nachträglich mühsam vereinheitlicht werden – ein Aufwand, der durch eine frühzeitige, abgestimmte Namenskonvention vermeidbar gewesen wäre.",
                "correct": True,
                "feedback": """✓ Richtig! Genau diese Erfahrung wird im Kapitel beschrieben: Wenn mehrere Partner unabhängig voneinander Dateien benennen, muss am Ende oft viel 'glattgezogen' werden. Diese Problematik unterstreicht, wie wichtig eine früh abgestimmte Benennungslogik für spätere Publikationsvorhaben ist."""
            },
            {
                "answer": "Uneinheitliche Dateibenennungen verschiedener Partner stellen in der Praxis kein nennenswertes Problem dar.",
                "correct": False,
                "feedback": """× Nicht korrekt. Das Gegenteil wird beschrieben: Uneinheitliche Benennungen durch verschiedene Partner erfordern typischerweise einen hohen nachträglichen Abstimmungs- und Korrekturaufwand."""
            },
            {
                "answer": "In einem solchen Fall sollte auf die Erstellung eines Datenmanagementplans grundsätzlich verzichtet werden.",
                "correct": False,
                "feedback": """× Nicht korrekt. Gerade in einem solchen Fall ist ein DMP hilfreich, um die Organisation und Vereinheitlichung der Daten strukturiert anzugehen, anstatt ihn deswegen auszulassen."""
            },
            {
                "answer": "Die Dateibenennung sollte in diesem Fall komplett den einzelnen Partnern überlassen bleiben, ohne eine gemeinsame Lösung anzustreben.",
                "correct": False,
                "feedback": """× Nicht korrekt. Die vermittelte Erfahrung spricht gerade dafür, eine gemeinsame, abgestimmte Lösung anzustreben, um Verständigungsprobleme zu vermeiden."""
            }
        ]
    }
]
display_quiz(question6, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 7

Die folgenden drei Fragen prüfen grundlegende Aussagen zum Management von Forschungsdaten. Entscheiden Sie jeweils, ob die Aussage richtig oder falsch ist.

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question7 = [
    {
        "question": "Es ist eine sinnvolle Praxis, bei der nachträglichen Organisation von Forschungsdaten bereits bestehende Projektstrukturen möglichst zu nutzen, anstatt sie komplett zu verwerfen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": True,
                "feedback": """✓ Richtig! Bestehende Strukturen und Benennungen sind in der Regel nicht willkürlich entstanden, sondern folgen einer eigenen, projektinternen Logik. Diese möglichst zu übernehmen, spart Aufwand und erhält die Nachvollziehbarkeit für alle Beteiligten."""
            },
            {
                "answer": "Falsch",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Aussage ist richtig: Es wird empfohlen, bestehende Strukturen soweit wie möglich zu übernehmen, da sie bereits einer sinnvollen, projektinternen Logik folgen."""
            }
        ]
    }
]
display_quiz(question7, colors=colors.jupyterquiz, max_width=1000)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question8 = [
    {
        "question": "Laut den im Kapitel beschriebenen Praxiserfahrungen lässt sich eine nachträgliche Anpassung der Dateibenennung in der Regel schnell und unkompliziert durchführen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": False,
                "feedback": """× Nicht korrekt. Das Gegenteil wird beschrieben: Eine nachträgliche Anpassung der Dateibenennung gilt als mühsam und ist eine der zentralen Herausforderungen bei der retrospektiven Datenaufbereitung."""
            },
            {
                "answer": "Falsch",
                "correct": True,
                "feedback": """✓ Richtig! Die Aussage ist falsch. Eine nachträgliche Anpassung der Dateibenennung wird als mühsam beschrieben, insbesondere wenn mehrere Partner unterschiedliche Schemata verwendet haben. Dies unterstreicht den Wert einer frühzeitigen, einheitlichen Benennungskonvention."""
            }
        ]
    }
]
display_quiz(question8, colors=colors.jupyterquiz, max_width=1000)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question9 = [
    {
        "question": "Eine README-Datei ersetzt vollständig die Notwendigkeit, Metadaten nach disziplinspezifischen Standards zu vergeben.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": False,
                "feedback": """× Nicht korrekt. Eine README-Datei ist zwar eine wichtige, aber nur die einfachste Form der Datendokumentation. Sie ersetzt nicht die Vergabe von Metadaten nach etablierten, disziplinspezifischen Standards – beide Maßnahmen ergänzen sich."""
            },
            {
                "answer": "Falsch",
                "correct": True,
                "feedback": """✓ Richtig! Die Aussage ist falsch. README und disziplinspezifische Metadaten erfüllen unterschiedliche, sich ergänzende Funktionen: Die README bietet eine einfache, menschenlesbare Übersicht, während strukturierte Metadaten nach Fachstandards die systematische Auffindbarkeit und maschinelle Verarbeitung ermöglichen."""
            }
        ]
    }
]
display_quiz(question9, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 8

**Frage:** Sie erstellen rückwirkend einen Datenmanagementplan für ein abgeschlossenes Forschungsprojekt, an dem mehrere Partnerinstitutionen beteiligt waren.

1. Welche Bestandteile müsste Ihr Datenmanagementplan mindestens umfassen?
2. Welche zwei Best-Practice-Hinweise aus Sicht von Forschenden würden Sie dabei besonders beachten, und warum?

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('datenmanagement-1')
```

````{admonition} Reflexionshinweise
:class: solution, dropdown

**1. Notwendige Bestandteile des DMP:**

- **Auswahl und Clusterung:** Festlegen, welche Daten veröffentlicht werden sollen und wie sie sinnvoll gebündelt werden (z. B. als Gesamt-ZIP oder in Teil-Paketen).
- **Dateibenennung:** Prüfung bzw. Festlegung eines einheitlichen, nachvollziehbaren Benennungsschemas.
- **Metadaten:** Beschreibung der Daten nach den Konventionen der jeweiligen Fachdisziplin.
- **FAIRifizierung:** Möglichst vollständige, standardisierte Beschreibung zur Maximierung der Interoperabilität.
- **README:** Eine einfache Dokumentationsdatei, die Nachnutzenden das grundlegende Verständnis der Daten ermöglicht.

**2. Mögliche Best-Practice-Hinweise:**

- **Bestehende Strukturen übernehmen:** Da mehrere Partnerinstitutionen beteiligt waren, lohnt es sich, so weit wie möglich auf bereits vorhandene Projektstrukturen und Logiken zurückzugreifen, anstatt bei null zu beginnen. Das spart Aufwand und erhält Nachvollziehbarkeit.
- **Frühzeitige Abstimmung der Dateibenennung:** Da verschiedene Partner oft unterschiedliche Benennungsschemata verwenden, sollte möglichst früh eine gemeinsame Konvention abgestimmt werden. Eine nachträgliche Vereinheitlichung ist erfahrungsgemäß mühsam und zeitaufwendig, besonders bei mehreren beteiligten Institutionen.

Beide Hinweise sind besonders relevant bei Projekten mit mehreren Partnerinstitutionen, da hier das Risiko uneinheitlicher, nicht abgestimmter Vorgehensweisen deutlich höher ist als bei Einzelprojekten.
````
