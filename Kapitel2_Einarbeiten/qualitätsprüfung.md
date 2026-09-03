(einarbeiten:qualitätsprüfung)=
# Qualitätsprüfung

In einem ersten Schritt müssen die zu publizierenden Daten einer Qualitätsprüfung unterzogen werden: genügen die Daten in der Art und Weise wie sie vorliegen den Ansprüchen? Dies gilt in Bezug auf Vollständigkeit, Plausibilität und die Einhaltung der guten wissenschaftlichen Praxis (GWP) [Link].

```{figure} /assets/1.2_qualitaetssicherung.png
---
align: center
width: 33%
---
Die Kompetenz 1.2 Qualitätssicherung des QUADRIGA Datenkompetenzframeworks.
```
*Quellenangabe: Ausschnitt aus dem Modell "QUADRIGA Datenkompetenzframework" von Petras et al. unter der Lizenz <a href="https://creativecommons.org/licenses/by/4.0/legalcode" class="external-link" target="_blank">CC BY 4.0</a> via <a href="https://zenodo.org/records/19470557" class="external-link" target="_blank">Zenodo</a>.*

## Was ist mit "Qualität" gemeint?

Die Qualität der Daten lässt sich in zwei verschiedene Unterkategorien aufteilen: Syntax und Semantik.

Mit Syntax ist gemeint, dass die Datensätze korrekt und richtig formatiert sind, sodass die  <a href="https://forschungsdaten.info/fdm-allgemein/veroeffentlichen-und-archivieren/faire-daten" class="external-link" target="_blank">FAIR</a>-Prinzipien eingehalten werden. In einer vergangenen <a href="https://quadriga-dk.github.io/Tabelle-Fallstudie-1/Markdown/4_Qualit%C3%A4tsbewertung.html" class="external-link" target="_blank">Fallstudie</a> wurde dies bereits behandelt. Um die Einhaltung der FAIR-Prinzipien sicherzustellen ist demnach besonders wichtig, dass die Datensätze maschinenlesbar sind und relevante Informationen zur Auffindbarkeit nicht im Datensatz selbst, sondern in den Metadaten hinterlegt sind. Doch was wenn die Daten, welche sich im Datensatz befinden zwar korrekt formatiert sind, allerdings einen Wert angenommen haben, welchen sie eigentlich gar nicht haben dürften.

Eine detallierte Übersicht von Qualitätsmerkmalen von Daten und Metadaten finden Sie <a href="https://quadriga-dk.github.io/Tabelle-Fallstudie-1/Markdown/4_Qualit%C3%A4tsbewertung.html" class="external-link" target="_blank">hier</a>.

Fünf besonders wichtige Kriterien für die Gewährleistung der Datenintegrität sind:

- 1. **Genauigkeit:** Abgleich der Daten mit der tatsächlichen Realität. Wenn beispielsweise ein plötzlicher Anstieg der Klickzahlen durch automatisierte Bots auf einer Website nicht herausgefiltert wird, spiegeln die Daten am Ende des Tages nicht die Realität wieder und sind ungenau.

- 2. **Vollständigkeit:** Bezieht sich auf die Frage, ob alle erforderlichen Felder in einem Datensatz ausgefüllt sind. Wenn bei einer Umfrage Name und E-Mail-Adresse keine Pflichtfelder sind, füllen manche Teilnehmer diese nicht aus, was zu einem unvollständigen Gesamtbild des Kunden führt. 

- 3. **Konsistenz:** Bezeichnet die Einheitlichkeit von Daten über verschiedene Systeme hinweg. Wenn das Einkaufsteam Postleitzahlen 5-stellig erfasst, das Marketingteam dieselben Postleitzahlen aber 9-stellig sammelt, passen die Kundeprofile beim Zusammenführen der Datenbanken nicht zusammen.

- 4. **Eindeutigkeit:** Vermeidung von Duplikaten. Hat ein Unternehmen beispielsweise 50.000 Datensätze, von denen aber 20 % Duplikate sind (weil Kunden das Formular mehrfach ausgefüllt haben), besitzt das Unternehmen in Wahrheit 20 % weniger eindeutige Datensätze. 

- 5. **Gültigkeit:** Die Konformität der Daten mit vordefinierten syntaktischen Vorgaben, Formatdefinitionen und zulässigen Wertebereichen. Ein ungültiger Wer für ein Datim wäre zum Beispiel "32.13.2025" {cite}`ramasamy2020big`.

Um diese zu erfüllen, lohnt es sich anzuschauen, welche Methoden für die Datenbereinigung im <a href="https://www.ibm.com/de-de/think/topics/data-engineering" class="external-link" target="_blank">Data Engineering</a> üblich sind und auch für Forschende von Bedeutung sein könnten. Hierfür gibt es einige typische Tests, die Sie, angepasst an die von Ihnen erwarteten Ergebnisse, implementieren können.

- **Bereichsprüfung:** Diese Prüfung konzentriert sich primär auf numerische Datensätze, bei denen ein bestimmter Wertebereich (von X bis Y) erwartet wird. Sie kann über Anomalie-Erkennungsmodelle implementiert werden. Wenn ein Wert den typischen Rahmen sprengt (z.B. wenn plötzlich eine Transaktion über eine Million Euro statt der üblichen 1.000 Euro aufläuft), schlägt das System an. Solche Abweichungen müssen nicht zwingend "kaputte" Daten sein; sie können auch auf fehlerhafte Prozesse hinweisen

- **Kategorieprüfungen:** Hierbei wird geprüft, ob Werte zu einer vordefinierten, sich selten ändernden Gruppe von Einträgen gehören. Ein klassisches Beispiel sind Unterscheidungszeichen bei deutschen KfZ-Kennzeichen (z.B. "B" für *Berlin* oder "HH" für *Hamburg*) . Wenn ein Prozess ohne Absprache eine neue Kategorie einführt, die dem Datensystem unbekannt ist (in diesem Fall ein Zeichen, welches es in Deutschland nicht gibt), meldet die Kategorieprüfung diesen Fehler.

- **Aktualitätsprüfung:**  Diese Prüfung betrifft den Aspekt der Pünktlichkeit und Aktualität (Timelines) von Daten. Es wird gemessen, wie viel Zeit seit dem letzten erfolgreichen Laden der Daten vergangen ist. Wenn ein Bericht beispielsweise zwei Tage lang nicht aktualisiert wurde, führt dies oft zu Frustration bei den Endnutzern, die mit aktuellen Daten arbeiten wollen. Meist wird hierbei eine automatische Warnung ausgelöst, sobald die Verzögerung einen bestimmten Grenzwert überschreitet. Da Sie allerdings mit hoher Wahrscheinlichkeit keine Echtzeitdaten publizieren, spielt dieser Test für Sie keine wirkliche Rolle. Ähnliches gilt für die **Volumenprüfung**, bei der die Anzahl der täglich geladenen Zeilen (Row Count) überwacht wird. Da die Datenmenge an normalen Tagen meist relativ stabil ist (oft mit Ausnahme des Wochenendes), deutet ein plötzlicher, drastischer Anstieg (z. B. das 3- bis 10-fache Volumen) auf ein Problem hin.

- **Nullwertprüfung:** Da sich Nullwerte in Datenbanken oft unvorhersehbar verhalten, ist dieser Test essenziell. Er stellt entweder sicher, dass überhaupt keine Nullwerte in einer Spalte existieren dürfen, oder er definiert einen maximal zulässigen prozentualen Anteil an leeren Feldern. Bei Bedarf können fehlende Werte auch automatisch mit Standard-Platzhaltern gefüllt werden.

- **Datentypprüfung:** Es wird überprüft, ob die Daten den erwarteten Typ aufweisen (z. B. ob ein Feld ein Datum oder eine Ganzzahl ist). Dies ist besonders kritisch, wenn Daten aus Dateien ohne Spaltenüberschriften (Header) importiert werden, da sich dort die Spaltenreihenfolge unbemerkt verschieben kann. Durch den Test wird verhindert, dass Daten mit ungültigen Formaten im weiteren Datenverarbeitungsprozess verarbeitet werden.

- **Eindeutigkeitsprüfung:** Diese Prüfung stellt sicher, dass Werte in einer Spalte (wie ID-Felder) absolut eindeutig sind und keine Duplikate enthalten {cite}`cai2015challenges,ramasamy2020big`.

## Medaillon-Schema

Im Data Engineering können diese Tests verwendet werden, um die Datenqualität innerhalb des sogenannten *Medaillon-Schemas* aufzuwerten.

```{figure} /assets/Medaillon-Schema.png
---
align: center
width: 50%
name: medaillon
---
Visualisierung des Medaillon Schemas
```

Das Medaillon-Schema ist ein im Data Engineering verbreitetes Schichtenmodell zur strukturierten Verarbeitung und schrittweisen Aufbereitung von Daten. Dabei werden Daten aus einer Rohdatenquelle über mehrere Verarbeitungsstufen hinweg in einen zunehmend bereinigten, geprüften und für die Analyse aufbereiteten Zustand überführt. Die Bezeichnung orientiert sich an den drei Stufen Bronze, Silber und Gold.

Auf der Bronze-Stufe werden die Daten zunächst möglichst unverändert aus ihren ursprünglichen Quellen übernommen. Ziel ist es, die Rohdaten sowie ihre ursprüngliche Struktur und Historie zu erhalten. In dieser Stufe stehen daher weniger die unmittelbare Nutzbarkeit für Analysen als vielmehr die Nachvollziehbarkeit und Bewahrung der ursprünglichen Daten im Vordergrund. Informationen zur Datenherkunft und zum Zeitpunkt der Erfassung können dabei ebenfalls erhalten bleiben.

Anschließend werden die Daten auf der Silber-Stufe bereinigt und überprüft. Fehlerhafte oder doppelte Datensätze können entfernt, uneinheitliche Formate vereinheitlicht und festgelegte Standards umgesetzt werden. Zudem werden die Daten hinsichtlich ihrer Qualität geprüft. Dadurch entsteht ein konsistenterer Datenbestand, der sich insbesondere für die weitere Exploration und Verarbeitung eignet. Datenqualitätstests, beispielsweise zur Vollständigkeit, Gültigkeit oder Eindeutigkeit, können dabei eingesetzt werden, um fehlerhafte Daten frühzeitig zu erkennen.

Auf der Gold-Stufe werden die Daten schließlich gezielt für konkrete Analyse- und Anwendungsszenarien aufbereitet. Dazu können Daten aggregiert, Kennzahlen berechnet oder geeignete Darstellungen für die Analyse und Visualisierung erzeugt werden. Während die Bronze- und Silber-Stufen somit vor allem die Erhaltung und Verbesserung der Datenqualität unterstützen, steht auf der Gold-Stufe die fachliche Nutzbarkeit und Interpretation der Daten im Vordergrund {cite}`mohna2022ai,armbrust2020delta`.

Obwohl die Bezeichnung Medaillon-Schema in der Forschungspraxis nicht üblich ist, besteht eine Verbindung zu Konzepten des Forschungsdatenmanagements und der Open Science. In der Forschung wird insbesondere die **Datenprovenienz** (eng. Data Provenance) dokumentiert, um nachvollziehbar zu machen, aus welchen Quellen genutzte Daten stammen und welche Verarbeitungsschritte zu einem wissenschaftlichen Ergebnis geführt haben. Die Dokumentation solcher Verarbeitungsschritte ist zugleich eine wichtige Voraussetzung für **reproduzierbare Forschung**, da Ergebnisse nicht allein von den Ausgangsdaten, sondern auch von deren Aufbereitung, verwendeten Programmen, Parametern und weiteren Verarbeitungsschritten abhängen.

Ein mögliches Problem in der Wissenschaftspraxis besteht darin, dass bei einer Veröffentlichung vor allem die finalen, für die Analyse verwendeten Daten und Ergebnisse sichtbar sind. Sind die zugrunde liegenden Ausgangsdaten und Verarbeitungsschritte nicht ausreichend dokumentiert, wird es schwieriger nachzuvollziehen, wie aus den ursprünglichen Daten die veröffentlichten Ergebnisse entstanden sind. Eine gute Forschungsdatenpraxis sollte daher neben den relevanten Daten auch deren Verarbeitung und (sofern verwendet und rechtlich möglich) den zugehörigen Code dokumentieren und möglichst dauerhaft über ein Repositorium zugänglich machen {cite}`mpdlDataQuality`.


## Strukturierung von Forschungsdaten

Neben der Prüfung einzelner Werte ist auch die strukturelle Gestaltung eines Datensatzes für dessen Qualität und Nachnutzbarkeit von Bedeutung. Eine konsistente Datenstruktur erleichtert insbesondere die maschinelle Verarbeitung und die Verknüpfung verschiedener Datensätze. Dazu sollten Variablen einheitlich benannt und formatiert sowie eindeutige Identifikatoren verwendet werden. Auch fehlende Werte sollten nach einem einheitlichen Schema gekennzeichnet und Formate, beispielsweise für Datumsangaben, konsequent eingehalten werden. Eine häufig empfohlene Struktur ist dabei das sogenannte **Tidy-Data-Prinzip**: Jede Variable wird in einer eigenen Spalte, jede Beobachtung in einer eigenen Zeile und jeder einzelne Wert eindeutig einer Variable und einer Beobachtung zugeordnet. Dadurch wird eine konsistente Weiterverarbeitung und Auswertung der Daten erleichtert. Insbesondere in Rohdatensätzen sollten zudem keine Berechnungen oder rein visuellen Formatierungen vorgenommen werden, da diese die maschinelle Weiterverarbeitung erschweren können. Detailliertere Informationen finden Sie  <a href="https://quadriga-dk.github.io/Tabelle-Fallstudie-1/Markdown/6_1_Datenstruktur.html" class="external-link" target="_blank">hier</a>.

## Praktische Umsetzung

Die beschriebenen Qualitäts- und Strukturprüfungen können grundsätzlich selbst als automatisierte Skripte implementiert werden. Besonders geeignet sind hierfür Programmiersprachen wie Python, mit denen beispielsweise Wertebereiche, Datentypen, fehlende Werte, Duplikate oder die Einhaltung bestimmter Formate systematisch überprüft werden können. Solche Prüfungen lassen sich wiederholt auf einen Datensatz anwenden und dadurch reproduzierbarer und weniger fehleranfällig gestalten als eine ausschließlich manuelle Kontrolle. Für viele Anwendungsfälle existieren darüber hinaus spezialisierte Werkzeuge, die solche Prüfungen vereinfachen oder um zusätzliche Funktionen ergänzen {cite}`wickham2014tidy,fowler2017frictionless`.

Eine Übersicht verschiedener Werkzeuge für die Datenqualitätsprüfung bietet beispielsweise die Zusammenstellung von Tools for Data. Die dort aufgeführten Werkzeuge lassen sich unter anderem den Bereichen Data Testing, Data Observability, Data Lineage und Data Catalog zuordnen.

```{figure} /assets/data-quality-tools-market-landscape.png
---
align: center
width: 50%
name: data-quality-tools
---
Übersicht von Datenqualitätstools auf dem Markt (Quelle: https://toolsfordata.com/lists/data-quality-tools/ abgerufen am 02.09.2026)
```
- Unter **Data Testing** werden Werkzeuge zusammengefasst, mit denen konkrete Regeln und Erwartungen an Daten überprüft werden, beispielsweise ob eine Spalte ausschließlich gültige Werte enthält oder keine Duplikate aufweist. 
- **Data Observability** erweitert diesen Ansatz um die fortlaufende Überwachung von Daten und die Erkennung von Anomalien, beispielsweise ungewöhnlichen Veränderungen in Datenbeständen. 
- **Data Lineage** beschreibt hingegen die Nachverfolgung, aus welchen Quellen Daten stammen und welche Verarbeitungsschritte zwischen den verschiedenen Datenständen durchgeführt wurden. 
- Ein **Data Catalog** dient schließlich dazu, Datenbestände und die zugehörigen Metadaten systematisch zu erfassen, auffindbar zu machen und zu dokumentieren {cite}`toolsfordata2026`.

Ein Beispiel für ein Open-Source-Werkzeug aus dem Bereich Data Testing ist <a href="https://greatexpectations.io/" class="external-link" target="_blank">Great Expectations</a>. Dabei handelt es sich um eine Python-Bibliothek, mit der Erwartungen an die Struktur und den Inhalt von Daten formuliert und automatisiert überprüft werden können. So lässt sich beispielsweise festlegen, dass eine Spalte einen bestimmten Datentyp besitzen, keine fehlenden Werte enthalten oder nur Werte innerhalb eines vorgegebenen Bereichs aufweisen darf. Great Expectations kann dabei unter anderem auf Dateien, Datenbanken und DataFrames angewendet werden {cite}`gxgreatexpectations`.

Neben solchen codebasierten Verfahren gibt es auch Werkzeuge, die eine Datenbereinigung über eine grafische Benutzeroberfläche ermöglichen. Ein Beispiel hierfür ist <a href="https://openrefine.org/" class="external-link" target="_blank">OpenRefine</a>, eine Open-Source-Software zur Bereinigung, Formatierung und Anreicherung von Datensätzen. Die tabellarische Oberfläche erinnert an eine Tabellenkalkulation, bietet jedoch weitergehende Funktionen zur systematischen Bearbeitung größerer Datensätze. OpenRefine kann unter anderem verschiedene Dateiformate einlesen und eignet sich insbesondere zur Standardisierung und Bereinigung bereits vorhandener, unstrukturierter oder inkonsistenter Daten {cite}`openrefine`.

Die praktische Anwendung lässt sich anhand der von QUADRIGA bereitgestellten <a href="https://quadriga-dk.github.io/Bewegtes-Bild-Fallstudie-2/bereinigung/openRefine/0_datenbereinigung.html" class="external-link" target="_blank">Fallstudie</a> zu studentischen Filmen der Filmuniversität Babelsberg nachvollziehen. Dort wird OpenRefine eingesetzt, um einen bestehenden Datensatz schrittweise zu sichten und zu bereinigen. Unter anderem werden Spalten und Einträge bereinigt und Jahresangaben sowie Filmtitel standardisiert. Die Fallstudie zeigt damit exemplarisch, wie die zuvor beschriebenen Anforderungen an Konsistenz, Standardisierung und Nachnutzbarkeit in einem konkreten Forschungsdatensatz umgesetzt werden können.



**Lösung**
Die Daten müssen händisch und stichprobenartig geprüft werden. *Können wir hier mit Software zur Qualitätsprüfung arbeiten?*

Folgende Fragen können dabei helfen:
- genügen die Daten in der Art und Weise wie sie vorliegen den Ansprüchen (an GwP (welche Punkte genau?), Vollständigkeit, Plausibilität etc.)
- Sind die Daten vollständig oder sind Lücken ersichtlich? *Sind das nicht Fragen der Datenerhebung und Validierung?* *Wie prüfe ich das bei mir fremden, mglw. fachfremden Daten (es lassen sich doch nur übliche Lücken und Fehler erkennen)*
- Sind die Metadaten aussagekräftig und die Daten gut dokumentiert?

*Bei der Einarbeitung in ein Projekt entsteht in der Regel automatisch ein Bild von möglichen Fragestellungen, Methodiken, Analysen und Ergebnissen. Diese Fragen können genutzt werden, um die Daten auf ihre Qualität zu prüfen.* 


## Beispiel Szenario 

In dem in diesem Szenario abgebildeten Fall ist eine Qualitätsprüfung nicht notwendig gewesen, weil die Daten bereits gut aufgearbeitet vorlagen.

## Learnings (generisch)

Die inhaltliche Überprüfung der Datenqualität ist für Fachfremde durchaus herausfordernd. Daher hilft es, sich an den in diesem Unterkapitel genannten, allgemeinen Kriterien zur Prüfung von Datenqualität zu orientieren.


*weiterdenken: was passiert, wenn die Daten nicht den Ansprüchen genügen? Sollten sie dann aufbereitet werden? Oder entfallen dann alle Schritte und ein nachträgliches Publizieren ist nicht möglich?*

---

**Literatur**

```{bibliography}
:filter: docname in docnames
```
