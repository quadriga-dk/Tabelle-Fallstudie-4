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

(einarbeiten:assessment)=
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

**Geschätzte Zeit**: 30 Minuten

Viel Erfolg!
````


## Frage 1

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question3 = [
    {
        "question": "Sie sollen für ein Institut entscheiden, ob ein umfangreicher Datensatz aus einem fachfremden, abgeschlossenen Projekt (mehrere tausend Tabellenzeilen) veröffentlicht werden kann. Wie gehen Sie bei der Qualitätsprüfung am besten vor?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Sie nutzen Ihr im Einarbeiten gewonnenes Verständnis des Projekts und prüfen stichprobenartig, ob Werte den Erwartungen entsprechen, ob Felder leer sind und ob Wertebereiche überschritten werden – am Ende steht eine Entscheidung für oder gegen die Publikation.",
                "correct": True,
                "feedback": "✓ Richtig! Das Ziel der Prüfung ist laut Kapitel eine Publikationsentscheidung. Bei großen Datenmengen ist eine Prüfung jedes einzelnen Feldes weder möglich noch sinnvoll; Stichproben anhand allgemeiner Qualitätskriterien sind der vorgesehene Weg."
            },
            {
                "answer": "Sie prüfen jede einzelne Tabellenzelle, denn nur eine lückenlose Kontrolle erfüllt die Anforderungen der Guten Wissenschaftlichen Praxis.",
                "correct": False,
                "feedback": "× Nicht korrekt. Das Kapitel hält ausdrücklich fest, dass das Prüfen einzelner Tabellenfelder bei großem Umfang nicht möglich und auch nicht sinnvoll ist. Die Gute Wissenschaftliche Praxis wird als Maßstab genannt, verlangt aber keine Vollkontrolle jeder Zelle."
            },
            {
                "answer": "Sie korrigieren gefundene Fehler und vereinheitlichen die Struktur, sodass der Datensatz anschließend in einwandfreiem Zustand vorliegt.",
                "correct": False,
                "feedback": "× Nicht korrekt. Die Aufarbeitung der Daten ist nicht das Ziel der Qualitätsprüfung – schon gar nicht bei einem fachfremden Projekt. Geprüft wird, ob die Daten in guter Qualität vorliegen und damit einen Mehrwert für die wissenschaftliche Community bieten können."
            },
            {
                "answer": "Sie verzichten auf eine eigene Prüfung, da Daten aus einem Forschungsprojekt einer Institution ohnehin als qualitätsgesichert gelten.",
                "correct": False,
                "feedback": "× Nicht korrekt. Das Kapitel verlangt vor der Publikation ausdrücklich eine Qualitätsprüfung (Vollständigkeit, Plausibilität, Gute Wissenschaftliche Praxis). Auch ein Hinweis auf die Herkunft allein ersetzt sie nicht – die Vertrauenswürdigkeit ist nur eines von zehn Merkmalen."
            }
        ]
    }
]
display_quiz(question3, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 2

Wählen Sie **alle** zutreffenden Aussagen.

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question4 = [
    {
        "question": "Welche Aussagen zur Struktur eines Datensatzes entsprechen den Empfehlungen des Kapitels (Tidy-Data-Struktur)?",
        "type": "many_choice",
        "answers": [
            {
                "answer": "Jede Variable steht in einer eigenen Spalte, jede Beobachtung in einer eigenen Zeile.",
                "correct": True,
                "feedback": "✓ Richtig! Das ist der Kern der Tidy-Data-Struktur: Variablen bilden Spalten, Beobachtungen bilden Zeilen."
            },
            {
                "answer": "Jeder einzelne Wert ist eindeutig genau einer Variable und einer Beobachtung zugeordnet.",
                "correct": True,
                "feedback": "✓ Richtig! Genau das macht die Struktur eindeutig und erleichtert eine konsistente Weiterverarbeitung und Auswertung."
            },
            {
                "answer": "In Rohdatensätzen sollten keine Berechnungen oder rein visuellen Formatierungen enthalten sein.",
                "correct": True,
                "feedback": "✓ Richtig! Berechnungen und rein optische Gestaltung können die maschinelle Weiterverarbeitung erschweren, besonders in Rohdaten."
            },
            {
                "answer": "Variablen sollten einheitlich benannt und formatiert sein, und es sollten eindeutige Identifikatoren verwendet werden.",
                "correct": True,
                "feedback": "✓ Richtig! Auch dies gehört laut Kapitel zu einer konsistenten Datenstruktur."
            },
            {
                "answer": "Farbliche Markierungen auffälliger Werte erhöhen die Nachnutzbarkeit, da Auffälligkeiten so sofort erkennbar sind.",
                "correct": False,
                "feedback": "× Nicht korrekt. Rein visuelle Formatierungen sind für Menschen hilfreich, für die maschinelle Weiterverarbeitung aber ein Hindernis – gerade in Rohdatensätzen sollten sie vermieden werden."
            },
            {
                "answer": "Es ist unproblematisch, mehrere Werte in einer Zelle zusammenzufassen, solange sie durch ein Trennzeichen getrennt sind.",
                "correct": False,
                "feedback": "× Nicht korrekt. Tidy Data verlangt, dass jeder einzelne Wert eindeutig einer Variable und einer Beobachtung zugeordnet ist. Zusammengefasste Werte widersprechen dem und erschweren die Auswertung."
            }
        ]
    }
]
display_quiz(question4, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 3

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question5 = [
    {
        "question": "Ein Forschungsteam hat über Jahre hinweg mit erheblichem Aufwand eine umfangreiche Datenbank mit Beobachtungsdaten aufgebaut und strukturiert. Welche Aussage zum rechtlichen Schutz trifft nach dem Kapitel am ehesten zu?",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Wegen der wesentlichen Investition in Erstellung und Strukturierung kann das Datenbankherstellerrecht greifen – geschützt wäre die Zusammenstellung der Daten, nicht die einzelnen Datenwerte.",
                "correct": True,
                "feedback": "✓ Richtig! Das Datenbankherstellerrecht knüpft an die wesentliche Investition in die Datenbank an und schützt deren Zusammenstellung. Einzelne Daten sind dadurch nicht geschützt."
            },
            {
                "answer": "Das Team besitzt automatisch ein umfassendes Eigentum an den Daten, da es sie erhoben hat. Über jeden einzelnen Wert kann es allein verfügen.",
                "correct": False,
                "feedback": "× Nicht korrekt. Im deutschen Recht existiert laut Kapitel kein allgemeines Eigentum an Daten. Rechte ergeben sich nur aus spezifischen Schutzrechten, und auch das Datenbankherstellerrecht schützt nicht die einzelnen Werte."
            },
            {
                "answer": "Da die Daten in einem Forschungsverhältnis entstanden sind, liegen die Rechte ausschließlich bei den Urheber:innen; die Institutionen haben keine Ansprüche.",
                "correct": False,
                "feedback": "× Nicht korrekt. Werden Daten im Rahmen eines Arbeits- oder Forschungsverhältnisses erzeugt, können zusätzlich Nutzungsrechte der beteiligten Institutionen bestehen. Bei Drittmittelprojekten können zudem die Antragsunterlagen Aufschluss über die Rechteinhaber geben."
            },
            {
                "answer": "Solange die Datenbank keine personenbezogenen Daten enthält, ist keine weitere Rechteprüfung nötig.",
                "correct": False,
                "feedback": "× Nicht korrekt. Personenbezug ist nur ein Aspekt. Zu prüfen sind außerdem vertragliche Vereinbarungen, Geheimhaltungspflichten, Rechte Dritter sowie mögliche Schutzrechte wie Urheber- und Datenbankherstellerrecht."
            }
        ]
    }
]
display_quiz(question5, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 4

Wählen Sie **alle** zutreffenden Aussagen.

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question6 = [
    {
        "question": "Ein Team möchte seine Forschungsdaten zusammen mit einem Fachartikel veröffentlichen. Welche Aussagen zu Policies von Journals und Verlagen treffen laut Kapitel zu?",
        "type": "many_choice",
        "answers": [
            {
                "answer": "Manche Verlage schreiben die Hinterlegung der Daten in einem anerkannten Repositorium als Voraussetzung für die Artikelpublikation vor, andere empfehlen das Datenteilen nur.",
                "correct": True,
                "feedback": "✓ Richtig! Die Policies reichen von bloßer Empfehlung bis zur verbindlichen Hinterlegungspflicht."
            },
            {
                "answer": "Verpflichtende Archivierungsrichtlinien erhöhen die tatsächliche Verfügbarkeit von Daten deutlich stärker als unverbindliche Empfehlungen.",
                "correct": True,
                "feedback": "✓ Richtig! Empirische Untersuchungen zeigen, dass unverbindliche Empfehlungen kaum Wirkung entfalten."
            },
            {
                "answer": "Die Joint Data Archiving Policy (JDAP) erlaubt ein Embargo von bis zu einem Jahr sowie Ausnahmen für sensible Daten, etwa bei personenbezogenen Informationen.",
                "correct": True,
                "feedback": "✓ Richtig! Das JDAP-Standardtextmuster sieht diese Flexibilität ausdrücklich vor."
            },
            {
                "answer": "Anforderungen an Metadaten, Dateiformate, DOI-Vergabe oder Lizenzierung unterscheiden sich erheblich zwischen einzelnen Journals und Repositorien.",
                "correct": True,
                "feedback": "✓ Richtig! Deshalb muss vorab geprüft werden, ob die vorhandenen Datensätze den Anforderungen des gewählten Journals oder Repositoriums genügen."
            },
            {
                "answer": "Inzwischen verfügen praktisch alle Journale über eine explizite Datenpolicy, sodass sich Policies zentral und einheitlich katalogisieren lassen.",
                "correct": False,
                "feedback": "× Nicht korrekt. Das Kapitel beschreibt die Policy-Landschaft als weiterhin uneinheitlich: Viele Journale haben noch keine explizite Datenpolicy, und die fehlende Standardisierung erschwert eine zentrale Katalogisierung."
            },
            {
                "answer": "Ein Data Availability Statement (DAS) verpflichtet Autor:innen, die Daten ohne Einschränkung öffentlich zugänglich zu machen.",
                "correct": False,
                "feedback": "× Nicht korrekt. Ein DAS gibt lediglich Auskunft darüber, wo und unter welchen Bedingungen die Daten verfügbar sind – es ist keine Pflicht zur uneingeschränkten Veröffentlichung."
            }
        ]
    }
]
display_quiz(question6, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 5

Die folgenden vier Aussagen betreffen Vorgaben und rechtliche Vorbereitung einer Datenpublikation. Entscheiden Sie jeweils, ob die Aussage richtig oder falsch ist.

```{code-cell} ipython3
:tags: [remove-input]
from jupyterquiz import display_quiz

import sys
sys.path.append("..")
from quadriga import colors

question7a = [
    {
        "question": "Eine Creative-Commons-Lizenz, die bei der Veröffentlichung vergeben wurde, kann bei veränderten Nachnutzungswünschen in der Regel jederzeit geändert oder zurückgenommen werden.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": False,
                "feedback": "× Nicht korrekt. Eine einmal vergebene Lizenz kann in der Regel nicht nachträglich geändert oder widerrufen werden. Deshalb sollte die Lizenzwahl vor der Veröffentlichung sorgfältig und in Abstimmung mit allen Rechteinhaber:innen erfolgen."
            },
            {
                "answer": "Falsch",
                "correct": True,
                "feedback": "✓ Richtig! Eine einmal vergebene Lizenz kann in der Regel nicht nachträglich geändert oder widerrufen werden. Deshalb sollte die Lizenzwahl vor der Veröffentlichung sorgfältig und in Abstimmung mit allen Rechteinhaber:innen erfolgen."
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
        "question": "Die DFG empfiehlt, Forschungsdaten gemäß den Regeln der Guten Wissenschaftlichen Praxis für mindestens fünf Jahre zu archivieren.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": False,
                "feedback": "× Nicht korrekt. Empfohlen werden mindestens zehn Jahre. Zudem sollen Daten – sofern keine rechtlichen oder vertraglichen Einschränkungen bestehen – möglichst zeitnah und nachnutzbar veröffentlicht werden."
            },
            {
                "answer": "Falsch",
                "correct": True,
                "feedback": "✓ Richtig! Empfohlen werden mindestens zehn Jahre. Zudem sollen Daten – sofern keine rechtlichen oder vertraglichen Einschränkungen bestehen – möglichst zeitnah und nachnutzbar veröffentlicht werden."
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

question7d = [
    {
        "question": "Gibt es für ein Veröffentlichungsvorhaben keine Vorgaben des Förderers, entfällt die Prüfung institutioneller Vorgaben, da diese nur ergänzend zu Förderervorgaben gelten.",
        "type": "multiple_choice",
        "answers": [
            {
                "answer": "Richtig",
                "correct": False,
                "feedback": "× Nicht korrekt. Institutionelle Vorgaben (z. B. Forschungsdaten-Leitlinien der Hochschulen) sowie Vereinbarungen mit weiteren Beteiligten wirken eigenständig und müssen gesondert geprüft werden. Im Beispielszenario gab es keine Förderervorgaben, dennoch waren die Hochschulpolicies relevant."
            },
            {
                "answer": "Falsch",
                "correct": True,
                "feedback": "✓ Richtig! Institutionelle Vorgaben (z. B. Forschungsdaten-Leitlinien der Hochschulen) sowie Vereinbarungen mit weiteren Beteiligten wirken eigenständig und müssen gesondert geprüft werden. Im Beispielszenario gab es keine Förderervorgaben, dennoch waren die Hochschulpolicies relevant."
            }
        ]
    }
]
display_quiz(question7d, colors=colors.jupyterquiz, max_width=1000)
```

## Frage 6

**Szenario:** Sie übernehmen die Aufgabe, die Daten eines abgeschlossenen Drittmittelprojekts aus einer Ihnen fachfremden Disziplin nachträglich in einem Repositorium zu veröffentlichen. Mehrere Projektmitarbeitende haben die Einrichtung bereits verlassen; die Projektleitung steht Ihnen jedoch zur Verfügung. Es liegen weder eine README noch ein Datenmanagementplan vor.

1. Wie verschaffen Sie sich zunächst einen Überblick über Projekt und Daten?
2. Wie gehen Sie bei der Qualitätsprüfung vor und was ist deren Ziel?
3. Welche rechtlichen und organisatorischen Aspekte klären Sie vor der Veröffentlichung, und an wen wenden Sie sich bei offenen Fragen?

```{code-cell} ipython3
:tags: [remove-input]
import sys
sys.path.append("../quadriga")
from assessment import create_answer_box

create_answer_box('einarbeiten-1')
```

````{admonition} Reflexionshinweise
:class: solution, dropdown

**1. Überblick verschaffen:**

- Ursprungskontext nachvollziehen: Aus welchem Projekt stammen die Daten, wer war beteiligt, wann und über welchen Zeitraum wurden sie erhoben, welche Daten liegen in welcher Form vor?
- Die Projektleitung als Ansprechperson einbeziehen; deren Aufzeichnungen und Kontakte zu ehemaligen Mitarbeitenden sind ein Schlüssel zum Verständnis.
- Zwischen Roh- und Forschungsdaten unterscheiden und für beide Format, Entstehung (Methodik) und Dokumentations-/Publikationsstand klären, z. B. in einer Tabelle zur Provenienz (Name, Beschreibung, Ergebnis der Untersuchung, Dateiformat).
- Fehlende README und Datenmanagementplan müssen von Ihnen angelegt werden.

**2. Qualitätsprüfung:**

- Orientierung an den allgemeinen Qualitätsmerkmalen (z. B. Fehlerfreiheit, Genauigkeit, Konformität, Konsistenz, Vollständigkeit) und der Guten Wissenschaftlichen Praxis.
- Stichprobenartig prüfen: Entsprechen Werte den Erwartungen? Gibt es leere Felder? Werden Wertebereiche überschritten? Struktur nach Tidy-Data-Prinzip, keine Berechnungen/visuellen Formatierungen in Rohdaten.
- Ziel ist die Entscheidung für oder gegen die Publikation, nicht die Aufarbeitung der Daten. Geprüft wird, ob die Daten einen Mehrwert für die wissenschaftliche Community bieten können.

**3. Rechtliches und Organisatorisches:**

- Rechte an den Daten (Urheberrecht, Nutzungsrechte der Institutionen, Datenbankherstellerrecht; kein allgemeines Dateneigentum), Personenbezug, vertragliche Vereinbarungen, Geheimhaltungspflichten, Rechte Dritter.
- Vorgaben (ehemaliger) Förderer aus den Antragsunterlagen, institutionelle Leitlinien, Empfehlungen der Fachcommunity sowie Policies des Zielrepositoriums/Journals (Metadaten, Formate, Lizenz).
- Lizenzwahl vorab und in Abstimmung mit allen Rechteinhaber:innen, da sie später in der Regel nicht geändert oder widerrufen werden kann (reine Datensätze häufig CC0, Daten mit Werkqualität häufig CC BY 4.0).
- Bei offenen Fragen: Förderinstitution, Rechtsabteilung oder FDM-Service der eigenen Institution.
````
