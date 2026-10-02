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

# 🏆Selbsttest: Publikation
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
        "question": "Was unterscheidet ein fachspezifisches Repositorium am ehesten von einem generischen Repositorium wie Zenodo?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Ein fachspezifisches Repositorium ist auf die Standards und Bedarfe einer bestimmten wissenschaftlichen Disziplin zugeschnitten, während ein generisches Repositorium disziplinübergreifend und ohne fachliche Spezialisierung nutzbar ist.",
                "correct": True,
                "feedback": """✓ Richtig! Fachspezifische Repositorien richten sich an eine bestimmte Wissenschaftscommunity und orientieren sich an deren Standards. Generische Repositorien wie Zenodo bieten hingegen eine disziplinunabhängige Lösung, die besonders dann sinnvoll ist, wenn kein passendes Fachrepositorium existiert."""
            },
            {
                "answer": "Ein fachspezifisches Repositorium ist immer kostenpflichtig, ein generisches Repositorium immer kostenlos.",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Kostenstruktur hängt vom jeweiligen Anbieter ab und wird nicht pauschal nach Repositorientyp unterschieden. Zenodo ist beispielsweise als generisches Repositorium kostenfrei, während auch manche Fachrepositorien kostenfrei nutzbar sind."""
            },
            {
                "answer": "Nur fachspezifische Repositorien vergeben persistente Identifikatoren wie DOIs.",
                "correct": False,
                "feedback": """× Nicht korrekt. Auch generische Repositorien wie Zenodo vergeben automatisch DOIs für veröffentlichte Datensätze. Die Vergabe von PIDs ist kein unterscheidendes Merkmal zwischen den beiden Repositorientypen."""
            },
            {
                "answer": "Nur generische Repositorien erfüllen wissenschaftliche Qualitätsstandards.",
                "correct": False,
                "feedback": """× Nicht korrekt. Sowohl fachspezifische als auch generische Repositorien können wissenschaftliche Qualitätsstandards erfüllen. Die fachliche Spezialisierung, nicht die Qualität, ist der zentrale Unterschied."""
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
    title="Ordnen Sie die folgenden Beschreibungen dem passenden Repositorientyp zu:",
    descriptions=[
        "Wird von einer einzelnen Institution (z. B. einer Universität) betrieben und ist für Externe oft nur eingeschränkt zugänglich",
        "Ist auf eine bestimmte wissenschaftliche Disziplin zugeschnitten und orientiert sich an deren fachspezifischen Standards",
        "Ist disziplinübergreifend nutzbar und eignet sich besonders, wenn kein passendes Fachrepositorium existiert"
    ],
    options=[
        "Institutionelles Repositorium",
        "Fachspezifisches Repositorium",
        "Generisches Repositorium"
    ],
    correct_mapping={
        "Wird von einer einzelnen Institution (z. B. einer Universität) betrieben und ist für Externe oft nur eingeschränkt zugänglich": "Institutionelles Repositorium",
        "Ist auf eine bestimmte wissenschaftliche Disziplin zugeschnitten und orientiert sich an deren fachspezifischen Standards": "Fachspezifisches Repositorium",
        "Ist disziplinübergreifend nutzbar und eignet sich besonders, wenn kein passendes Fachrepositorium existiert": "Generisches Repositorium"
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
        "question": "Ein interdisziplinäres Forschungsteam möchte Daten veröffentlichen, findet jedoch kein passendes fachspezifisches Repositorium für sein Fachgebiet. Welche Option bietet sich am ehesten an?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Ein generisches Repositorium wie Zenodo oder Figshare, da diese disziplinübergreifend nutzbar sind.",
                "correct": True,
                "feedback": """✓ Richtig! Generische Repositorien bieten genau für solche Fälle eine unkomplizierte Lösung: Sie eignen sich für Forschende, für deren spezifisches Feld kein dediziertes Fachrepositorium existiert oder deren Institution keine eigene Infrastruktur bereitstellt."""
            },
            {
                "answer": "Die Veröffentlichung sollte in diesem Fall unterbleiben, bis ein passendes Fachrepositorium entsteht.",
                "correct": False,
                "feedback": """× Nicht korrekt. Das Fehlen eines fachspezifischen Repositoriums ist kein Hinderungsgrund für eine Veröffentlichung. Generische Repositorien bieten gerade für solche Fälle eine praktikable Alternative."""
            },
            {
                "answer": "Die Daten sollten stattdessen ausschließlich in einem privaten Cloud-Speicher ohne Qualitätsstandards abgelegt werden.",
                "correct": False,
                "feedback": """× Nicht korrekt. Private Cloud-Speicher ohne wissenschaftliche Qualitätsstandards erfüllen nicht die Anforderungen an ein Repositorium im Sinne des Forschungsdatenmanagements."""
            },
            {
                "answer": "Es sollte zwingend ein neues, eigenes Fachrepositorium für das betreffende Gebiet aufgebaut werden.",
                "correct": False,
                "feedback": """× Nicht korrekt. Der Aufbau eines komplett neuen Repositoriums ist weder notwendig noch im Kapitel als Lösung vorgesehen. Bestehende generische Repositorien bieten eine deutlich praktikablere Option."""
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
        "question": "Welche Aspekte sollten bei der Auswahl eines geeigneten Repositoriums berücksichtigt werden? Wählen Sie alle zutreffenden Aussagen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Ob das Repositorium über anerkannte Qualitätszertifikate wie CoreTrustSeal oder das nestor-Siegel verfügt.",
                "correct": True,
                "feedback": """✓ Richtig! Solche Zertifikate stellen die organisatorische Verlässlichkeit, das professionelle Datenmanagement und eine sichere IT-Infrastruktur eines Repositoriums sicher."""
            },
            {
                "answer": "Ob Verlage oder Journale, bei denen eine Publikation geplant ist, bestimmte Repositorien vorschreiben oder empfehlen.",
                "correct": True,
                "feedback": """✓ Richtig! Journale können die Ablage von Forschungsdaten in einem bestimmten, fachlich anerkannten Repositorium vorschreiben oder zumindest empfehlen, was die Auswahl beeinflussen sollte."""
            },
            {
                "answer": "Welche Nutzungs- und Lizenzbedingungen mit der Veröffentlichung im jeweiligen Repositorium verbunden sind.",
                "correct": True,
                "feedback": """✓ Richtig! Je nach eingeräumten Rechten und bestehenden Vereinbarungen kann eine weitere Veröffentlichung in einem anderen Repositorium erschwert oder ausgeschlossen sein, weshalb dies vorab geprüft werden sollte."""
            },
            {
                "answer": "Wie viele Mitarbeitende das Unternehmen bzw. die Institution hinter dem Repositorium insgesamt beschäftigt.",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Mitarbeiterzahl wird im Kapitel nicht als Auswahlkriterium genannt. Relevanter sind Aspekte wie Qualitätszertifikate, Zugänglichkeit, Lizenzbedingungen und die langfristige Verlässlichkeit des Trägers."""
            },
            {
                "answer": "Ob persistente Identifikatoren wie DOIs vergeben werden, um Inkonsistenzen bei einer Mehrfachveröffentlichung zu vermeiden.",
                "correct": True,
                "feedback": """✓ Richtig! Persistente Identifikatoren wie DOIs ermöglichen es, auf bereits anderswo veröffentlichte Daten zu verweisen und so Inkonsistenzen zwischen mehreren Repositorien zu vermeiden."""
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
        "question": "Warum bedeutet das Fehlen eines CoreTrustSeal- oder nestor-Siegels nicht automatisch, dass ein Repositorium von geringer Qualität ist?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Weil solche Zertifizierungen kostenpflichtig und im deutschsprachigen Raum sowie darüber hinaus noch nicht flächendeckend etabliert sind, sodass auch qualitativ hochwertige Repositorien ohne Zertifikat existieren können.",
                "correct": True,
                "feedback": """✓ Richtig! Zertifizierungen wie CoreTrustSeal oder nestor sind mit Kosten verbunden und bislang kein verbreiteter Standard. Zenodo ist beispielsweise nicht zertifiziert, gilt aber aufgrund seines renommierten, langfristig stabilen Trägers (CERN) dennoch als attraktives und verlässliches generisches Repositorium."""
            },
            {
                "answer": "Weil diese Zertifizierungen ausschließlich für fachspezifische, nicht aber für generische Repositorien vergeben werden.",
                "correct": False,
                "feedback": """× Nicht korrekt. Diese Einschränkung wird im Kapitel nicht genannt. Grundsätzlich können sowohl fachspezifische als auch generische Repositorien zertifiziert werden – es ist lediglich kein verbreiteter Standard."""
            },
            {
                "answer": "Weil diese Zertifikate inzwischen durch eine automatische, kostenlose Prüfung ersetzt wurden.",
                "correct": False,
                "feedback": """× Nicht korrekt. Eine solche automatische Ersatzprüfung wird im Kapitel nicht erwähnt. Die Zertifizierung erfolgt weiterhin über einen Selbstevaluierungs- und Begutachtungsprozess."""
            },
            {
                "answer": "Weil die Qualität eines Repositoriums ausschließlich von der Menge der dort gespeicherten Datensätze abhängt.",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Datenmenge wird im Kapitel nicht als Qualitätsindikator genannt. Relevanter sind organisatorische Verlässlichkeit, professionelles Datenmanagement und eine stabile IT-Infrastruktur."""
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
        "question": "Was versteht man unter dem Begriff 'Datenpublikation' in Abgrenzung zur bloßen Aufbewahrung von Forschungsdaten in einem Repositorium?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Datenpublikation bezeichnet den aktiven Prozess der finalen Prüfung, Dokumentation und Bereitstellung von Daten (inkl. Metadaten, PID und Lizenz), damit diese formal auffindbar und nachnutzbar werden – nicht nur die reine Speicherung.",
                "correct": True,
                "feedback": """✓ Richtig! Während die Aufbewahrung in einem Repositorium die technische Grundlage schafft, umfasst die Datenpublikation den aktiven Prozess der Fertigstellung: Metadaten und persistente Identifikatoren vergeben, FAIR-Konformität und gute wissenschaftliche Praxis prüfen sowie die finale Version hochladen und veröffentlichen."""
            },
            {
                "answer": "Datenpublikation bedeutet, dass Daten irgendwo auf einem Server gespeichert werden, unabhängig davon, ob sie für andere auffindbar oder nutzbar sind.",
                "correct": False,
                "feedback": """× Nicht korrekt. Reine Speicherung ohne Auffindbarkeit und Nachnutzbarkeit entspricht eher einer Archivierung im Hintergrund, nicht einer Publikation. Eine Datenpublikation zielt explizit auf öffentliche Zugänglichkeit und Nachnutzung ab."""
            },
            {
                "answer": "Datenpublikation ist ein rein rechtlicher Begriff, der sich ausschließlich auf die Vergabe einer Lizenz bezieht.",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Lizenzvergabe ist nur ein Teilaspekt. Datenpublikation umfasst darüber hinaus auch Metadaten, Dokumentation, Qualitätsprüfung und den eigentlichen Upload-Prozess."""
            },
            {
                "answer": "Datenpublikation beschreibt ausschließlich die Kommunikation der Veröffentlichung in sozialen Medien.",
                "correct": False,
                "feedback": """× Nicht korrekt. Die Kommunikation einer bereits erfolgten Veröffentlichung ist ein nachgelagerter, separater Schritt. Die Datenpublikation selbst bezieht sich auf die Fertigstellung und das eigentliche Veröffentlichen der Daten im Repositorium."""
            }
        ]
    }
]
display_quiz(question6, colors=colors.jupyterquiz, max_width=1000)
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
        "question": "In welche drei Teilbereiche lässt sich die Fertigstellung einer Datenpublikation gliedern, bevor Forschungsdaten final in einem Repositorium veröffentlicht werden?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Metadaten und PID (inkl. Dokumentation), FAIR-Assessment und gute wissenschaftliche Praxis (inkl. Zitationshinweis), sowie Versionierung und Upload.",
                "correct": True,
                "feedback": """✓ Richtig! Diese drei Teilbereiche fassen zusammen, was vor der eigentlichen Veröffentlichung geprüft werden muss: eine vollständige Beschreibung mit Metadaten und PID, die Einhaltung von FAIR-Prinzipien und guter wissenschaftlicher Praxis sowie die korrekte Versionierung und der eigentliche Upload."""
            },
            {
                "answer": "Marketingplanung, Budgetierung und interne Freigabe durch die Geschäftsführung.",
                "correct": False,
                "feedback": """× Nicht korrekt. Diese Begriffe stammen nicht aus dem im Kapitel beschriebenen Prozess der Datenpublikation, der sich auf Metadaten, FAIR-Konformität und den technischen Upload konzentriert."""
            },
            {
                "answer": "Datenerhebung, Datenanalyse und Dateninterpretation.",
                "correct": False,
                "feedback": """× Nicht korrekt. Diese Schritte gehören zum ursprünglichen Forschungsprozess, nicht zur nachgelagerten Fertigstellung der Datenpublikation, die in diesem Kapitel behandelt wird."""
            },
            {
                "answer": "Pressemitteilung, Social-Media-Post und Blogbeitrag.",
                "correct": False,
                "feedback": """× Nicht korrekt. Diese Formate gehören zur anschließenden Kommunikation einer bereits veröffentlichten Datenpublikation, nicht zur Fertigstellung der Publikation selbst."""
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
        "question": "Ein Forschungsteam möchte seine neu veröffentlichten Daten sowohl der eigenen Fachcommunity als auch einer breiteren, nicht-wissenschaftlichen Öffentlichkeit bekannt machen. Welche Kombination an Kommunikationswegen eignet sich dafür am ehesten?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Eine Mitteilung über fachspezifische Mailinglisten oder den Informationsdienst Wissenschaft (idw) für die Fachcommunity, kombiniert mit einer Pressemitteilung oder Social-Media-Beiträgen für die interessierte Öffentlichkeit.",
                "correct": True,
                "feedback": """✓ Richtig! Mailinglisten und der idw richten sich gezielt an die Fach- und wissenschaftliche Community, während Pressemitteilungen und Social-Media-Beiträge eher die interessierte Öffentlichkeit erreichen. Die Kombination beider Wege deckt somit beide Zielgruppen ab."""
            },
            {
                "answer": "Ausschließlich eine einzelne Mailingliste, da diese automatisch auch die breite Öffentlichkeit erreicht.",
                "correct": False,
                "feedback": """× Nicht korrekt. Mailinglisten richten sich laut Kapitel primär an die Fachcommunity, nicht an die breite, nicht-wissenschaftliche Öffentlichkeit. Für Letztere eignen sich andere Formate wie Pressemitteilungen oder Social Media besser."""
            },
            {
                "answer": "Ausschließlich eine Data Story, da diese alle denkbaren Zielgruppen gleichermaßen optimal erreicht.",
                "correct": False,
                "feedback": """× Nicht korrekt. Data Stories sind ein sinnvoller Kommunikationsweg, decken aber laut Kapitel nicht automatisch alle Zielgruppen gleichermaßen ab. Eine Kombination verschiedener, zielgruppenspezifischer Formate ist meist wirkungsvoller."""
            },
            {
                "answer": "Keine gesonderte Kommunikation ist notwendig, da die Veröffentlichung im Repositorium automatisch alle relevanten Zielgruppen erreicht.",
                "correct": False,
                "feedback": """× Nicht korrekt. Das Kapitel betont ausdrücklich, dass die Publikation der Daten aktiv kommuniziert werden sollte, damit Kolleg:innen und ggf. die interessierte Öffentlichkeit überhaupt davon erfahren."""
            }
        ]
    }
]
display_quiz(question8, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 9

Die folgenden drei Fragen prüfen grundlegende Aussagen zur Kommunikation von Datenpublikationen. Entscheiden Sie jeweils, ob die Aussage richtig oder falsch ist.

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question9 = [
    {
        "question": "Data Stories sind in der Regel lange, rein textbasierte Zusammenfassungen ohne Visualisierungen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": False,
                "feedback": """× Nicht korrekt. Data Stories sind gerade das Gegenteil: relativ kurze Zusammenfassungen, die komplexe Zusammenhänge unter Einbindung prägnanter Visualisierungen verständlich vermitteln."""
            },
            {
                "answer": "Falsch",
                "correct": True,
                "feedback": """✓ Richtig! Die Aussage ist falsch. Data Stories zeichnen sich gerade durch ihre Kürze und die Einbindung prägnanter Visualisierungen aus, um komplexe Erkenntnisse verständlich zu vermitteln."""
            }
        ]
    }
]
display_quiz(question9, colors=colors.jupyterquiz, max_width=1000)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question9b = [
    {
        "question": "Mailinglisten richten sich in erster Linie an die breite, nicht-wissenschaftliche Öffentlichkeit.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": False,
                "feedback": """× Nicht korrekt. Mailinglisten erreichen laut Kapitel primär die Fachcommunity, nicht die breite, nicht-wissenschaftliche Öffentlichkeit. Für Letztere eignen sich eher Formate wie Pressemitteilungen oder Social-Media-Beiträge."""
            },
            {
                "answer": "Falsch",
                "correct": True,
                "feedback": """✓ Richtig! Die Aussage ist falsch. Mailinglisten richten sich in erster Linie an die Fachcommunity, während die interessierte Öffentlichkeit eher über Pressemitteilungen oder Social Media erreicht wird."""
            }
        ]
    }
]
display_quiz(question9b, colors=colors.jupyterquiz, max_width=1000)
```

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question9c = [
    {
        "question": "Es kann sinnvoll sein, eine Datenpublikation über mehrere Kommunikationswege gleichzeitig bekannt zu machen.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": True,
                "feedback": """✓ Richtig! Je nachdem, welche Zielgruppen erreicht werden sollen, kann es sinnvoll sein, die Publikation auf mehreren Ebenen gleichzeitig zu kommunizieren – etwa über fachspezifische und öffentlichkeitswirksame Kanäle parallel."""
            },
            {
                "answer": "Falsch",
                "correct": False,
                "feedback": """× Nicht korrekt. Das Kapitel empfiehlt ausdrücklich, zu prüfen, welche Zielgruppen erreicht werden sollen, und weist darauf hin, dass eine Kommunikation auf mehreren Ebenen unter Umständen sinnvoll ist."""
            }
        ]
    }
]
display_quiz(question9c, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 10

**Frage:** Sie veröffentlichen Forschungsdaten aus einem interdisziplinären Projekt, für das kein fachspezifisches Repositorium existiert.

1. Welchen Repositorientyp würden Sie wählen und warum?
2. Was müssten Sie noch zusätzlich tun, damit die Daten als vollständig "publiziert" gelten – und nicht nur hochgeladen sind?
3. Über welche zwei Kommunikationswege würden Sie die Veröffentlichung bekannt machen, und welche Zielgruppen würden Sie damit jeweils erreichen?

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('publikation-1')
```

````{admonition} Reflexionshinweise
:class: solution, dropdown

**1. Wahl des Repositorientyps:**

Da kein fachspezifisches Repositorium existiert, bietet sich ein generisches Repositorium wie Zenodo oder Figshare an. Diese sind disziplinübergreifend nutzbar und eignen sich besonders für Fälle, in denen kein dediziertes Fachrepositorium zur Verfügung steht. Bei der Auswahl sollte zusätzlich auf Aspekte wie Qualitätszertifikate (sofern vorhanden), die Vergabe persistenter Identifikatoren (DOI) sowie etwaige Vorgaben von Journalen oder Verlagen geachtet werden.

**2. Notwendige Schritte zur vollständigen Publikation:**

Reines Hochladen reicht nicht aus. Zusätzlich sollten:
- vollständige Metadaten vergeben und ein persistenter Identifikator (PID/DOI) zugewiesen werden,
- die Einhaltung der FAIR-Prinzipien und der guten wissenschaftlichen Praxis geprüft werden (inkl. Zitationshinweis),
- eine korrekte Versionierung sichergestellt und der finale Upload durchgeführt werden,
- die Zugriffsrechte (z. B. "öffentlich") bewusst festgelegt werden.

**3. Mögliche Kommunikationswege:**

- Eine Mitteilung über eine fachspezifische Mailingliste oder den Informationsdienst Wissenschaft (idw), um die eigene Fach- und Wissenschaftscommunity zu erreichen.
- Eine Pressemitteilung auf der Institutionswebseite oder ein Social-Media-Beitrag, um zusätzlich die interessierte, nicht-wissenschaftliche Öffentlichkeit zu informieren.

Je nach Zielsetzung kann auch eine kurze Data Story sinnvoll sein, um zentrale Erkenntnisse visuell aufbereitet sowohl der Fachcommunity als auch einer breiteren Öffentlichkeit zugänglich zu machen.
````
