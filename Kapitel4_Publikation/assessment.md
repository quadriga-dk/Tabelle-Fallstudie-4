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

(publikation:assessment)=
# 🏆Selbsttest: Publikation

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
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question1 = [
    {
        "question": "Eine Linguistin möchte ihre Korpusdaten veröffentlichen. Für ihr kleines Forschungsfeld gibt es kein eigenes Repositorium, und ihre Hochschule betreibt keine eigene Infrastruktur dafür. Welche Art von Repositorium kommt für sie am ehesten in Frage?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Ein generisches Repositorium, das disziplinübergreifend arbeitet und keine fachliche Ausrichtung voraussetzt (z. B. Zenodo oder Figshare).",
                "correct": True,
                "feedback": "✓ Richtig! In diesem Fall ist ein generische Repositorien die richtige Wahl. Sie bieten eine unkomplizierte Lösung, wenn für das Forschungsfeld kein Fachrepositorium existiert oder die Heimatinstitution keine eigene Infrastruktur anbietet."
            },
            {
                "answer": "Ein institutionelles Repositorium, da jede Forschende ihre Daten grundsätzlich bei der eigenen Hochschule ablegt.",
                "correct": False,
                "feedback": "× Nicht korrekt. Institutionelle Repositorien werden von der Institution betrieben und sind auf die Bedürfnisse ihrer Mitarbeitenden ausgelegt. Betreibt die Hochschule keine solche Infrastruktur, steht diese Option nicht zur Verfügung."
            },
            {
                "answer": "Ein fachspezifisches Repositorium, das auf die Anforderungen der Fachcommunity zugeschnitten ist.",
                "correct": False,
                "feedback": "× Nicht korrekt. Fachspezifische Repositorien sind zwar auf eine Disziplin zugeschnitten und thematisch homogen – im Szenario existiert für das Forschungsfeld aber gerade keines."
            },
            {
                "answer": "re3data, weil dort die Daten dauerhaft gespeichert und veröffentlicht werden.",
                "correct": False,
                "feedback": "× Nicht korrekt. re3data ist ein globales Register, das wie eine Suchmaschine für Forschungsdatenrepositorien funktioniert. Es hilft beim Finden eines Repositoriums, speichert oder publiziert aber selbst keine Daten."
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
    title="Ordnen Sie jede Beschreibung der passenden Repositorienart bzw. Plattform zu:",
    descriptions=[
        "Ist auf eine Fachdisziplin ausgerichtet, thematisch homogen und auf die Anforderungen der jeweiligen Fachcommunity zugeschnitten.",
        "Globales, DFG-gefördertes Register, in dem sich Forschungsdatenrepositorien wie in einer Suchmaschine finden und nach Kategorien filtern lassen.",
        "Wird vom CERN betrieben, entstand im Rahmen des OpenAIRE-Projekts und vergibt für alle veröffentlichten Datensätze automatisch einen DOI.",
        "Kommerziell betriebenes Repositorium mit kostenfreier Basisversion, das viele Dateiformate direkt im Browser als Vorschau anzeigt.",
    ],
    options=[
        "Fachspezifisches Repositorium",
        "re3data",
        "Zenodo",
        "Figshare",
        "Informationsdienst Wissenschaft (idw)"
    ],
    correct_mapping={
        "Ist auf eine Fachdisziplin ausgerichtet, thematisch homogen und auf die Anforderungen der jeweiligen Fachcommunity zugeschnitten.": "Fachspezifisches Repositorium",
        "Globales, DFG-gefördertes Register, in dem sich Forschungsdatenrepositorien wie in einer Suchmaschine finden und nach Kategorien filtern lassen.": "re3data",
        "Wird vom CERN betrieben, entstand im Rahmen des OpenAIRE-Projekts und vergibt für alle veröffentlichten Datensätze automatisch einen DOI.": "Zenodo",
        "Kommerziell betriebenes Repositorium mit kostenfreier Basisversion, das viele Dateiformate direkt im Browser als Vorschau anzeigt.": "Figshare"
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
        "question": "Ein Team will seine Forschungsdaten „FAIRifizieren“. Welche Beschreibung trifft den Kern dieses Schritts am besten?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Daten und Metadaten werden nach den FAIR-Prinzipien gestaltet: möglichst vollständig beschrieben, wo immer möglich nach Standards, und einem Persistenten Identifikator (PID).",
                "correct": True,
                "feedback": "✓ Richtig! FAIRifizierung bedeutet die Anwendung der FAIR-Prinzipien auf Daten und Metadaten, bevor sie veröffentlicht werden. Der PID ist dabei besonders wichtig, aber nur ein Baustein."
            },
            {
                "answer": "Die Daten erhalten einen DOI; sobald dieser vergeben ist, gelten sie als FAIR.",
                "correct": False,
                "feedback": "× Nicht korrekt. Die Vergabe eines PID (z. B. eines DOI) ist für die FAIRifizierung zwar von besonderer Bedeutung, doch darüber hinaus muss die Beschreibung vollständig sein, und die Interoperabilität sollte maximiert werden."
            },
            {
                "answer": "Die Daten werden in ein Repositorium hochgeladen; die Plattform sorgt danach selbst dafür, dass sie den FAIR-Prinzipien entsprechen.",
                "correct": False,
                "feedback": "× Nicht korrekt. Laut Kapitel sollen bereits die hochzuladenden Daten und Metadaten eine FAIRifizierung durchlaufen. Das Repositorium liefert zwar oft automatisch den DOI, nimmt Ihnen die Beschreibung aber nicht ab."
            },
            {
                "answer": "Ein automatisiertes Prüfwerkzeug wird ausgeführt, das die Daten dann entsprechend den FAIR-Kriterien anpasst.",
                "correct": False,
                "feedback": "× Nicht korrekt. Automatisierte Werkzeuge wie F-UJI bewerten die FAIRness eines Datensatzes anhand eines PID oder einer URL und melden zurück, welche Kriterien erfüllt sind und wo Verbesserungsbedarf besteht. Die Verbesserung selbst bleibt Aufgabe der Forschenden."
            }
        ]
    }
]
display_quiz(question3, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 4

Wählen Sie **alle** zutreffenden Aussagen.

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question4 = [
    {
        "question": "Sie bereiten den Upload eines Datenpakets bei Zenodo vor. Welche Aussagen treffen laut Kapitel zu?",
        "type": "many_choice",
        "answers": [
            {
                "answer": "Eine Anmeldung über ORCID wird empfohlen, weil die Ersteller:innen eines Eintrags dadurch eindeutig identifiziert werden können.",
                "correct": True,
                "feedback": "✓ Richtig! Ein Konto lässt sich auf mehreren Wegen erstellen; ORCID wird wegen der eindeutigen Identifizierbarkeit der Urheber:innen empfohlen."
            },
            {
                "answer": "Der Beschreibung sollte ein Inhaltsverzeichnis (TOC) hinzugefügt werden, da es einen schnellen Überblick über die Dateien ermöglicht.",
                "correct": True,
                "feedback": "✓ Richtig! Das ist nicht nur bei großen Datenpaketen hilfreich."
            },
            {
                "answer": "Ein Eintrag kann zunächst als Entwurf gespeichert und vor der Veröffentlichung noch einmal auf korrekt hochgeladene Dateien und vollständige Angaben geprüft werden.",
                "correct": True,
                "feedback": "✓ Richtig! Der Entwurfsmodus („Save draft“) erlaubt es, Eintrag und Metadaten in Ruhe zu prüfen, bevor „Publish“ gewählt wird."
            },
            {
                "answer": "Für den Upload ist ausschließlich ein Konto möglich, das mit einer E-Mail-Adresse erstellt wurde.",
                "correct": False,
                "feedback": "× Nicht korrekt. Das Konto kann mit einer E-Mail-Adresse, über GitHub, ORCID oder OpenAIRE erstellt werden."
            },
            {
                "answer": "Innerhalb eines Uploads werden die Dateien nach ihrer Upload-Zeit angezeigt, sodass die Benennung der Dateien keine Rolle spielt.",
                "correct": False,
                "feedback": "× Nicht korrekt. Innerhalb eines Uploads wird nach Namen sortiert. Deshalb empfiehlt das Kapitel, mit Nummern zu arbeiten. Nur die Reihenfolge mehrerer Uploads richtet sich bei Zenodo nach dem Datum."
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
        "question": "Ein Team veröffentlicht einen Datensatz zusammen mit einer README-Datei und einem Forschungsdatenbericht. In beiden Dokumenten soll der DOI des Datensatzes selbst genannt werden. Beide Dokumente sind Teil der Veröffentlichung. Wie sollte das Team vorgehen?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Den benötigten DOI vor der Veröffentlichung reservieren und in die Dokumente eintragen, bevor diese hochgeladen werden.",
                "correct": True,
                "feedback": "✓ Richtig! Weil der DOI in Dokumenten genannt werden soll, die selbst Teil der Publikation sind, empfiehlt das Kapitel, sich die benötigten DOIs vorher zu reservieren. Für den Eintrag kann ein neuer DOI generiert oder ein bereits zugewiesener DOI angegeben werden."
            },
            {
                "answer": "Den Datensatz zunächst ohne DOI-Angabe veröffentlichen und den DOI später in einem separaten Schritt in die Dokumente einarbeiten.",
                "correct": False,
                "feedback": "× Nicht korrekt. Dann wären die veröffentlichten Dokumente zum Zeitpunkt der Publikation unvollständig. Das Kapitel empfiehlt stattdessen, den DOI im Voraus zu reservieren, damit er direkt in die Dokumente eingetragen werden kann."
            },
            {
                "answer": "Auf die Nennung des DOI in den Dokumenten verzichten, da der Datensatz über das Repositorium ohnehin auffindbar ist.",
                "correct": False,
                "feedback": "× Nicht korrekt. Der DOI ist ein Persistenter Identifikator und wichtiger Bestandteil der FAIRifizierung. Er soll in README bzw. Forschungsdatenbericht genannt werden können, weshalb er vorab reserviert werden sollte."
            },
            {
                "answer": "Den DOI eines anderen, bereits veröffentlichten Datensatzes des Repositoriums als Platzhalter verwenden.",
                "correct": False,
                "feedback": "× Nicht korrekt. Ein DOI identifiziert genau ein Objekt. Der Platzhalter würde auf einen anderen Datensatz verweisen. Erforderlich ist ein für diesen Datensatz reservierter DOI."
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

question7 = [
    {
        "question": "Ein Institut hat Messdaten veröffentlicht, die sowohl für Fachkolleg:innen als auch für die interessierte Öffentlichkeit relevant sind. Welches Vorgehen entspricht dem Kapitel am besten?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Zielgruppen festlegen, prüfen, welche Kommunikationswege zur Verfügung stehen, und gegebenenfalls auf mehreren Ebenen informieren, z. B. durch eine Pressemitteilung und zusätzlich durch Wege wie eine Data Story.",
                "correct": True,
                "feedback": "✓ Richtig! Klassische Formate wie die Pressemitteilung kommen auch für Datenpublikationen in Betracht. Neue Wege wie Data Stories ergänzen sie, indem sie die Publikation visuell hervorheben. Je nach Zielgruppe kann die Kommunikation auf mehreren Ebenen sinnvoll sein."
            },
            {
                "answer": "Data Stories ersetzen klassische Mitteilungen, da diese für Daten nicht vorgesehen sind.",
                "correct": False,
                "feedback": "× Nicht korrekt. Die klassischen Optionen gelten nicht ausschließlich für Datenpublikationen, können aber auch dafür genutzt werden. Data Stories sind eine zusätzliche, sich erst entwickelnde Möglichkeit."
            },
            {
                "answer": "Eine eigene Kommunikation ist nicht nötig, weil die Daten im Repositorium dauerhaft auffindbar sind.",
                "correct": False,
                "feedback": "× Nicht korrekt. Das Kapitel betont, dass die Publikation den Kolleg:innen und der wissenschaftlichen Community bekannt gemacht werden sollte. Je nach Art der Daten kann auch die interessierte Öffentlichkeit informiert werden."
            }
        ]
    }
]
display_quiz(question7, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 7

Die folgenden vier Aussagen betreffen Repositorien, den Upload und die Kommunikation. Entscheiden Sie jeweils, ob die Aussage richtig oder falsch ist.


```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question8b = [
    {
        "question": "Bei Zenodo muss im Entwurfsmodus mindestens eine Datei eingestellt sein; eine Dummy-Datei erlaubt es, die Metadaten in Ruhe auszufüllen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": True,
                "feedback": "✓ Richtig! Ohne Datei lässt sich der Upload nicht (zwischen)speichern. Eine Dummy-Datei löst dieses Problem."
            },
            {
                "answer": "Falsch",
                "correct": False,
                "feedback": "× Nicht korrekt. Die Aussage ist richtig. Ohne Datei lässt sich der Upload nicht (zwischen)speichern. Eine Dummy-Datei löst dieses Problem."
            }
        ]
    }
]
display_quiz(question8b, colors=colors.jupyterquiz, max_width=1000)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question8c = [
    {
        "question": "Formate wie Blogbeitrag oder Podcast dienen exklusiv der Veröffentlichung von Forschungsdaten.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": False,
                "feedback": "× Nicht korrekt. Diese Formate dienen nicht exklusiv der Datenveröffentlichung, lassen sich aber als Plattformen nutzen, um sie zu kommunizieren."
            },
            {
                "answer": "Falsch",
                "correct": True,
                "feedback": "✓ Richtig! Diese Formate dienen nicht exklusiv der Datenveröffentlichung, lassen sich aber als Plattformen nutzen, um sie zu kommunizieren."
            }
        ]
    }
]
display_quiz(question8c, colors=colors.jupyterquiz, max_width=1000)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question8d = [
    {
        "question": "Automatisierte FAIR-Prüfwerkzeuge können einen Datensatz bereits anhand seines Persistent Identifiers oder einer URL bewerten.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": True,
                "feedback": "✓ Richtig! Werkzeuge wie F-UJI bewerten die FAIRness anhand eines PID oder einer URL und geben unmittelbar Rückmeldung, welche Kriterien erfüllt sind."
            },
            {
                "answer": "Falsch",
                "correct": False,
                "feedback": "× Nicht korrekt. Die Aussage ist richtig. Werkzeuge wie F-UJI bewerten die FAIRness anhand eines PID oder einer URL und geben unmittelbar Rückmeldung, welche Kriterien erfüllt sind."
            }
        ]
    }
]
display_quiz(question8d, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 8

**Szenario:** Sie haben die Daten eines abgeschlossenen Projekts geordnet und dokumentiert und sollen sie nun veröffentlichen. Für das Forschungsfeld des Projekts gibt es kein eigenes Repositorium; Ihre Institution kann Ihnen nur eingeschränkt weiterhelfen.

1. Wie finden Sie ein geeignetes Repositorium, und welche Art von Repositorium kommt in Frage?
2. Was beachten Sie bei Vorbereitung, Upload und Veröffentlichung der Daten?
3. Wie machen Sie die Veröffentlichung bekannt?

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('publikation-1')
```

````{admonition} Reflexionshinweise
:class: solution, dropdown

**1. Repositorium finden und auswählen:**

- Erste Anlaufstelle: Bibliothek oder FDM-Team der Institution, auch für die Beratung zu externen Repositorien.
- Selbst suchen über re3data.
- Drei Arten: institutionell, fachspezifisch, generisch. Gibt es kein Fachrepositorium oder keine Infrastruktur der Institution, bietet sich ein generisches Repositorium an (z. B. Zenodo, Figshare).

**2. Vorbereitung, Upload, Veröffentlichung:**

- FAIRifizierung: Daten und Metadaten möglichst vollständig beschreiben, Standards nutzen, Interoperabilität herstellen, PID/DOI vergeben (Checklisten, Reifegradmodelle oder automatisierte Werkzeuge wie F-UJI können unterstützen).
- Datenpaket (Daten, Metadaten, Dokumentation, DMP) zusammenstellen; Konto anlegen (ORCID empfohlen); auf Reihenfolge und Dateibenennung achten.
- Metadatenfelder möglichst vollständig ausfüllen, TOC ergänzen, Sichtbarkeit („öffentlich“ als Standard) festlegen. Dummy-Datei für den Entwurf nutzen, Eintrag prüfen, dann veröffentlichen.
- DOI vorab reservieren, wenn er in README oder Forschungsdatenbericht genannt werden soll.

**3. Kommunikation:**

- Zielgruppen klären und verfügbare Wege prüfen.
- Klassische Wege: Pressemitteilung, Mailinglisten, idw, Social Media. Neue Wege für Daten: Data Stories, Datenhighlights. Ergänzend Blogbeitrag oder Podcast.
- Gegebenenfalls auf mehreren Ebenen kommunizieren.
````
