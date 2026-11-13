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

(datenmanagement:assessment)=
# 🏆 Selbsttest: Datenmanagement
````{admonition} Hinweis
:class: hinweis
Diese Übungsaufgaben dienen Ihrer Selbsteinschätzung und helfen Ihnen, das im Kapitel Gelernte zu reflektieren.

Sie können die Fragen in beliebiger Reihenfolge beantworten und auch mehrfach versuchen.

**So funktioniert es:**
- Wählen Sie bei jeder Frage die Antwort(en), die Sie für richtig halten
- Lesen Sie das Feedback zu den einzelnen Antwortoptionen sorgfältig durch
- Die Erklärungen helfen Ihnen, Ihr Verständnis zu vertiefen – auch bei korrekten Antworten

Es erfolgt keine Bewertung oder Speicherung Ihrer Ergebnisse. Nutzen Sie dieses Assessment, um Wissenslücken zu identifizieren und gegebenenfalls die entsprechenden Abschnitte des Kapitels noch einmal zu bearbeiten.

**Geschätzte Zeit**: 10 Minuten

Viel Erfolg!
````


## Frage 1

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import DragDropQuiz

quiz = DragDropQuiz()

quiz.create_matching_quiz(
    title="Ordnen Sie jede Angabe dem Bestandteil eines Datenmanagementplans zu, in dem sie üblicherweise gemacht wird:",
    descriptions=[
        "Wie die Daten im Projekt entstehen, um welche Datentypen es sich handelt und welches Datenvolumen zu erwarten ist.",
        "Welche Metadatenstandards zur Beschreibung der Daten genutzt werden und welche Werkzeuge man braucht, um die Daten zu nutzen.",
        "Wer im Projekt für das Datenmanagement verantwortlich ist, welche Projektpartner beteiligt sind und wer das Vorhaben fördert.",
        "Wo die Daten während der Projektlaufzeit liegen, wie Backups erfolgen und wer Zugriff darauf hat.",
        "Ob personenbezogene Daten enthalten sind, welche Lizenzen gelten und welche Urheber- und Schutzrechte zu beachten sind."
    ],
    options=[
        "Projektkontext",
        "Datenbeschreibung",
        "Dokumentation",
        "Speicherung",
        "Rechtliche Aspekte"
    ],
    correct_mapping={
        "Wer im Projekt für das Datenmanagement verantwortlich ist, welche Projektpartner beteiligt sind und wer das Vorhaben fördert.": "Projektkontext",
        "Wie die Daten im Projekt entstehen, um welche Datentypen es sich handelt und welches Datenvolumen zu erwarten ist.": "Datenbeschreibung",
        "Welche Metadatenstandards zur Beschreibung der Daten genutzt werden und welche Werkzeuge man braucht, um die Daten zu nutzen.": "Dokumentation",
        "Wo die Daten während der Projektlaufzeit liegen, wie Backups erfolgen und wer Zugriff darauf hat.": "Speicherung",
        "Ob personenbezogene Daten enthalten sind, welche Lizenzen gelten und welche Urheber- und Schutzrechte zu beachten sind.": "Rechtliche Aspekte"
    }
)
```

## Frage 2

Wählen Sie **alle** zutreffenden Aussagen.

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question3 = [
    {
        "question": "Welche Aussagen zu Datenmanagementplänen (DMP) treffen laut Kapitel zu?",
        "type": "many_choice",
        "answers": [
            {
                "answer": "Ein DMP dokumentiert Verfahrensweisen, Arbeitsschritte und Zuständigkeiten in Bezug auf die Forschungsdaten eines Projekts.",
                "correct": True,
                "feedback": "✓ Richtig! Neben der Beschreibung der Daten selbst gehört auch das „Wer macht was und wie“ in den DMP."
            },
            {
                "answer": "Weil ein DMP aktualisiert werden kann, lassen sich damit auch Änderungen im Projektablauf festhalten.",
                "correct": True,
                "feedback": "✓ Richtig! Diese Aktualisierbarkeit macht den DMP zugleich zu einem Werkzeug des Projektmanagements."
            },
            {
                "answer": "Drittmittelgeber erwarten zunehmend Aussagen darüber, wie in einem Forschungsprojekt mit Daten umgegangen wird.",
                "correct": True,
                "feedback": "✓ Richtig! Genau deshalb ist der DMP für viele Projekte ein fester Bestandteil der Planung."
            },
            {
                "answer": "Der DMP wird gemeinsam mit den Forschungsdaten veröffentlicht.",
                "correct": True,
                "feedback": "✓ Richtig! Er ist damit Teil dessen, was Nachnutzende zu den Daten zu sehen bekommen."
            },
            {
                "answer": "Wurde während der Projektlaufzeit kein DMP angelegt, kann bei einer nachträglichen Veröffentlichung von Forschungsdaten darauf verzichtet werden.",
                "correct": False,
                "feedback": "× Nicht korrekt. Das Kapitel hält fest: Wenn im Lauf des Projekts noch kein DMP begonnen wurde, muss spätestens zur nachträglichen Forschungsdatenpublikation einer angelegt werden. Im Beispielprojekt wurde er nachträglich verfasst."
            },
            {
                "answer": "Ein DMP beschränkt sich auf die Beschreibung der Datenformate und des Datenvolumens.",
                "correct": False,
                "feedback": "× Nicht korrekt. Formate und Volumen gehören zur Datenbeschreibung, sie sind aber nur einer von mehreren Bestandteilen. Hinzu kommen u. a. Projektkontext, Speicherung, rechtliche Aspekte und Aufbewahrung."
            }
        ]
    }
]
display_quiz(question3, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 3

Wählen Sie **alle** zutreffenden Aussagen.

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question6 = [
    {
        "question": "Sie ordnen die Daten eines abgeschlossenen Projekts vor der Veröffentlichung. Was gehört nach dem Kapitel dazu?",
        "type": "many_choice",
        "answers": [
            {
                "answer": "Zuerst festlegen, welche Daten überhaupt veröffentlicht werden sollen.",
                "correct": True,
                "feedback": "✓ Richtig! Die Auswahl der zu veröffentlichenden Daten ist der erste Schritt der Ordnung."
            },
            {
                "answer": "Je nach Umfang Daten zu sinnvollen Bündeln zusammenfügen oder aufteilen und dabei auch eine Zusammenfassung in ZIP-Paketen mitdenken.",
                "correct": True,
                "feedback": "✓ Richtig! Die Clusterung wird schon beim Anlegen des DMP mitgedacht und hängt stark von der Art der Daten ab."
            },
            {
                "answer": "Prüfen, ob Daten und Dateien bereits nach einem erkennbaren Schema benannt sind.",
                "correct": True,
                "feedback": "✓ Richtig! Ob Benennungen ein erkennbares Schema haben, ist eine der Prüffragen vor der Publikation."
            },
            {
                "answer": "Prüfen, ob Dateien in proprietären Formaten vorliegen, und abwägen, ob eine Konvertierung sinnvoll ist.",
                "correct": True,
                "feedback": "✓ Richtig! Das Kapitel formuliert dies als Abwägung, nicht als Automatismus."
            },
            {
                "answer": "Alle im Projekt entstandenen Dateien müssen unverändert veröffentlicht werden; eine Auswahl entfällt.",
                "correct": False,
                "feedback": "× Nicht korrekt. Das Kapitel nennt die Auswahl der zu veröffentlichenden Daten ausdrücklich als ersten Schritt."
            }
        ]
    }
]
display_quiz(question6, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 4

Die folgenden vier Aussagen betreffen Datenmanagementplan, Dateibenennung und Metadaten. Entscheiden Sie jeweils, ob die Aussage richtig oder falsch ist.

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question7a = [
    {
        "question": "Ein DMP wird einmal zu Projektbeginn geschrieben und anschließend nicht mehr verändert, damit er verlässlich bleibt.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": False,
                "feedback": "× Nicht korrekt. Gerade die Aktualisierbarkeit ist ein Vorteil des DMP: So lassen sich Änderungen im Projektablauf festhalten."
            },
            {
                "answer": "Falsch",
                "correct": True,
                "feedback": "✓ Richtig! Gerade die Aktualisierbarkeit ist ein Vorteil des DMP: So lassen sich Änderungen im Projektablauf festhalten."
            }
        ]
    }
]
display_quiz(question7a, colors=colors.jupyterquiz, max_width=1000)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question7b = [
    {
        "question": "Bei der Vergabe von Metadaten sind disziplinspezifische Konventionen optional, solange irgendein Standard verwendet wird.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": False,
                "feedback": "× Nicht korrekt. Metadaten sollen möglichst umfangreich und standardisiert sowie unter Beachtung der Konventionen der Disziplin vergeben werden, aus der die Forschungsdaten stammen."
            },
            {
                "answer": "Falsch",
                "correct": True,
                "feedback": "✓ Richtig! Metadaten sollen möglichst umfangreich und standardisiert sowie unter Beachtung der Konventionen der Disziplin vergeben werden, aus der die Forschungsdaten stammen."
            }
        ]
    }
]
display_quiz(question7b, colors=colors.jupyterquiz, max_width=1000)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question7c = [
    {
        "question": "Die Bündelung von Forschungsdaten zu Paketen hat den Vorteil, dass die im Projekt etablierte Dateibenennung nicht geändert werden muss.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": True,
                "feedback": "✓ Richtig! Beispielsweise lassen sich verschiedene Untersuchungen mit einem Messgerät A in einem Paket A zusammenfassen, ohne einzelne Dateien umzubenennen."
            },
            {
                "answer": "Falsch",
                "correct": False,
                "feedback": "× Nicht korrekt. Die Aussage ist richtig. Beispielsweise lassen sich verschiedene Untersuchungen mit einem Messgerät A in einem Paket A zusammenfassen, ohne einzelne Dateien umzubenennen."
            }
        ]
    }
]
display_quiz(question7c, colors=colors.jupyterquiz, max_width=1000)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question7d = [
    {
        "question": "Der Name eines Datenpakets im DMP und auf der Veröffentlichungsplattform kann unabhängig voneinander gewählt werden.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": False,
                "feedback": "× Nicht korrekt. Die Bezeichnung im DMP und auf der Plattform sollte übereinstimmen. Man sollte sich eine sinnvolle Ordnung überlegen und diese beibehalten."
            },
            {
                "answer": "Falsch",
                "correct": True,
                "feedback": "✓ Richtig! Die Bezeichnung im DMP und auf der Plattform sollte übereinstimmen. Man sollte sich eine sinnvolle Ordnung überlegen und diese beibehalten."
            }
        ]
    }
]
display_quiz(question7d, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 5

**Szenario:** Sie sollen die Daten eines abgeschlossenen Projekts nachträglich veröffentlichen. Während der Projektlaufzeit wurde weder ein Datenmanagementplan noch eine README-Datei angelegt. Die Daten liegen als Tabellen, Texte und Bilddateien in uneinheitlich benannten Ordnern vor.

1. Wie gehen Sie bei der Ordnung der Daten und der Dateibenennung vor?
2. Welche Aspekte muss der Datenmanagementplan enthalten, den Sie nachträglich anlegen?
3. Wie beschreiben Sie die Daten darüber hinaus, damit Dritte sie später korrekt interpretieren können?

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('datenmanagement-1')
```

````{admonition} Reflexionshinweise
:class: solution, dropdown

**1. Ordnung und Benennung:**

- Auswählen, welche Daten veröffentlicht werden sollen; je nach Umfang zu sinnvollen Bündeln zusammenfügen oder aufteilen (ggf. als ZIP-Pakete).
- Prüfen, ob die Benennung einem erkennbaren Schema folgt und ob proprietäre Formate vorliegen (Konvertierung abwägen).
- Ziel: Die Daten sollen auch projektextern verständlich sein.
- Die im Projekt gewachsene Struktur und Benennung nach Möglichkeit übernehmen; nachträgliches Umbenennen ist fehleranfällig. Pakete können der Publikation entsprechend benannt werden. Die einmal gewählte Benennung konsequent beibehalten, auch im DMP und auf der Plattform.

**2. Bestandteile des DMP:**

- Projektkontext (Verantwortlichkeiten, Datenmanagement, Projektpartner, Förderer)
- Datenbeschreibung (Entstehung, Datentypen, Formate, Datenvolumen)
- Dokumentation (Metadatenstandards, Qualitätssicherung, erforderliche Werkzeuge)
- Speicherung (Speicherung während des Projekts, Backups, Zugriffsrechte, Datensicherheit)
- Rechtliche Aspekte (personenbezogene und sensible Daten, Genehmigungen, Zugänglichkeit, Lizenzen, Urheber- und Schutzrechte, Leitlinien der Institutionen und Förderer)
- Aufbewahrung (Auswahl, Nachnutzung, Infrastruktur, Sperrfristen)
- Der DMP wird gemeinsam mit den Daten veröffentlicht und kann aktualisiert werden; ein Tool wie RDMO kann beim Erstellen helfen.

**3. Beschreibung der Daten:**

- Metadaten möglichst umfangreich und standardisiert vergeben, nach den Konventionen der Disziplin (z. B. fachübergreifend DataCite, Dublin Core, schema.org; fachspezifisch über NFDI-Konsortien).
- Eine README-Datei (einfache .txt-Datei) als einfachste Form der Dokumentation beilegen, mit allgemeinen Informationen, Weitergabe und Zugang (z. B. Lizenz, Zitierweise), Daten- und Dateiübersicht, methodischen Informationen und dateispezifischen Informationen (z. B. Variablen, fehlende Werte).
````
