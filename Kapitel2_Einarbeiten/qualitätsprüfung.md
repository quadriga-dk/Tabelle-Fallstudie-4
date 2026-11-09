(einarbeiten:qualitätsprüfung)=
# Qualitätsprüfung

Nachdem der Projektkontext nachvollzogen wurde, müssen die zu publizierenden Daten einer Qualitätsprüfung unterzogen werden, um sicherzustellen, dass die Daten in der Art und Weise wie sie vorliegen den Ansprüchen genügen. Dies gilt in Bezug auf Vollständigkeit, Plausibilität und die Einhaltung der guten wissenschaftlichen Praxis (<a href="https://www.dfg.de/de/grundlagen-themen/grundlagen-und-prinzipien-der-foerderung/gwp" class="external-link" target="_blank">GWP</a>).

```{figure} /assets/1.2_qualitaetssicherung.png
---
align: center
width: 33%
---
Die Kompetenz 1.2 Qualitätssicherung des QUADRIGA Datenkompetenzframeworks.
```
*Quellenangabe: Ausschnitt aus dem Modell "QUADRIGA Datenkompetenzframework" von Petras et al. unter der Lizenz <a href="https://creativecommons.org/licenses/by/4.0/legalcode" class="external-link" target="_blank">CC BY 4.0</a> via <a href="https://zenodo.org/records/19470557" class="external-link" target="_blank">Zenodo</a>.*

## Ausgangslage

Die Qualität der Forschungsdaten ist für deren Publikation entscheidend. In der ebenfalls im QUADRIGA Datenkompetenzzentrum erstellten OER "Reproduzierbarkeit von Datenanalysen: Ein Fallbeispiel aus dem Nationalen Bildungsbericht" finden Sie im Kapitel <a href="https://quadriga-dk.github.io/Tabelle-Fallstudie-1/Markdown/4_Qualit%C3%A4tsbewertung.html" class="external-link" target="_blank">Qualitätsbewertung</a> eine detallierte Übersicht von Qualitätsmerkmalen von Daten und Metadaten. Darin werden u. a. die 10 nachfolgenden Qualitätsmerkmale genannt, die disziplinübergreifend zur Bewertung verwendet werden können.

- **Fehlerfreiheit:** Die Daten und Metadaten sind fehlerfrei. Somit sind nur korrekte Werte in der Datei vorhanden {cite}`pipino_data_2002,vaddepalli_taxonomy_2023`.

- **Aktualität:** Die Daten und Metadaten sind auf dem neuesten Stand und werden in regelmäßigen Intervallen überprüft. Das Aktualisierungsintervall ist in den Metadaten mit angegeben. Die Datei enthält eine Versionsnummer, aus welcher erkenntlich wird, auf welchem zeitlichen Stand die Datei ist {cite}`pipino_data_2002,vaddepalli_taxonomy_2023`.

- **Genauigkeit:** Die Daten und Metadaten sind so präzise wie möglich angegeben. Demnach wird auf Rundungen von Zahlen verzichtet. Die Metadaten enthalten alle relevanten Details zur Datei {cite}`behkamal_metrics-driven_2014,bruns_leitfaden_2019,vetro_open_2016`.

- **Konformität:** Die Daten und Metadaten entsprechen den domänenspezifischen Standards. Diese beziehen sich auf Datumsangaben, Zeichenkodierung, etc. Zudem sind alle Informationen enthalten, welche durch verwendetes Vokabular und Betitelung impliziert werden {cite}`behkamal_metrics-driven_2014,vetro_open_2016`.

- **Konsistenz:** Daten und Metadaten sind widerspruchsfrei. Dies gilt für die Daten selbst und auch in Bezug auf andere Datensätze {cite}`behkamal_metrics-driven_2014,pipino_data_2002`.

- **Vertrauenswürdigkeit:** Der Ursprung der Daten ist kenntlich gemacht. Zudem sollte eine Evaluation bezüglich der Glaubwürdigkeit des Herausgebers erfolgen {cite}`bruns_leitfaden_2019,pipino_data_2002`.

- **Transparenz:** Veränderungen an den Daten ist für Dritte ersichtlich (beispielsweise durch die Angabe einer Versionsnummer) {cite}`bruns_leitfaden_2019`.

- **Verständlichkeit:** Die Daten sind so strukturiert und bezeichnet, dass Außenstehende diese leicht verstehen können. Es wird nur einfaches Vokabular verwendet, welches kein besonderes Fachwissen voraussetzt {cite}`behkamal_metrics-driven_2014,vetro_open_2016,pipino_data_2002`.

- **Vollständigkeit:** Die Daten sind vollständig (z. B. sind alle Datenfelder befüllt). Falls die Daten unvollständig sind, wird auf die Unvollständigkeit hingewiesen {cite}`behkamal_metrics-driven_2014,vetro_open_2016,pipino_data_2002`.

- **Zugänglichkeit:** Die Daten können auf einfache Weise abgerufen werden. Außerdem besteht eine permanente Verlinkung aller Referenzen und Links (z.B. mittels Verwendung permanenter URIs) {cite}`behkamal_metrics-driven_2014,vetro_open_2016,pipino_data_2002,vaddepalli_taxonomy_2023`.

## Vorgehen

Das Ziel der Prüfung der Datenqualität ist eine Entscheidung für oder gegen ihre Publikation, nicht ihre Aufarbeitung. Je nach Umfang der Daten ist beispielsweise das Prüfen einzelner Tabellenfelder nicht möglich und auch nicht sinnvoll. Schauen Sie stichprobenartig einzelne Werte an. Entsprechen diese den erwarteten Ergebnissen? Gibt es leere Felder? Werden Wertebereiche überschritten?  

Die Datenstruktur sollte konsistent, Variablen einheitlich benannt und formatiert sein sowie eindeutige Identifikatoren verwendet werden. Orientieren Sie sich an der **Tidy-Data-Struktur**: Jede Variable wird in einer eigenen Spalte, jede Beobachtung in einer eigenen Zeile und jeder einzelne Wert eindeutig einer Variable und einer Beobachtung zugeordnet. Dadurch wird eine konsistente Weiterverarbeitung und Auswertung der Daten erleichtert. Insbesondere in Rohdatensätzen sollten zudem keine Berechnungen oder rein visuellen Formatierungen vorgenommen werden, da diese die maschinelle Weiterverarbeitung erschweren können. Weitere Informationen dazu finden Sie in der oben erwähnten OER im Unterkapitel <a href="https://quadriga-dk.github.io/Tabelle-Fallstudie-1/Markdown/6_1_Datenstruktur.html" class="external-link" target="_blank">Datenstruktur</a>.

### Praktische Umsetzung

Weitergehende Qualitäts- und Strukturprüfungen können grundsätzlich als automatisierte Skripte implementiert werden. Besonders geeignet sind hierfür Programmiersprachen wie Python, mit denen beispielsweise Wertebereiche, Datentypen, fehlende Werte, Duplikate oder die Einhaltung bestimmter Formate systematisch überprüft werden können. Solche Prüfungen lassen sich wiederholt auf einen Datensatz anwenden und dadurch reproduzierbarer und weniger fehleranfällig gestalten als eine ausschließlich manuelle Kontrolle. Für viele Anwendungsfälle existieren darüber hinaus spezialisierte Werkzeuge, die solche Prüfungen vereinfachen oder um zusätzliche Funktionen ergänzen {cite}`wickham2014tidy,fowler2017frictionless`.

Eine Übersicht verschiedener Werkzeuge für die Datenqualitätsprüfung bietet beispielsweise die Zusammenstellung von Tools for Data (s. Abb. 2.5). Die dort aufgeführten Werkzeuge lassen sich unter anderem den Bereichen Data Testing, Data Observability, Data Lineage und Data Catalog zuordnen.

```{figure} /assets/data-quality-tools-market-landscape.png
---
align: center
width: 75%
name: data-quality-tools
---
Übersicht von Datenqualitätstools auf dem Markt (Quelle: https://toolsfordata.com/lists/data-quality-tools/ abgerufen am 02.09.2026)
```
- Unter **Data Testing** werden Werkzeuge zusammengefasst, mit denen konkrete Regeln und Erwartungen an Daten überprüft werden, beispielsweise ob eine Spalte ausschließlich gültige Werte enthält oder keine Duplikate aufweist. 
- **Data Observability** erweitert diesen Ansatz um die fortlaufende Überwachung von Daten und die Erkennung von Anomalien, beispielsweise ungewöhnlichen Veränderungen in Datenbeständen. 
- **Data Lineage** beschreibt hingegen die Nachverfolgung, aus welchen Quellen Daten stammen und welche Verarbeitungsschritte zwischen den verschiedenen Datenständen durchgeführt wurden. 
- Ein **Data Catalog** dient schließlich dazu, Datenbestände und die zugehörigen Metadaten systematisch zu erfassen, auffindbar zu machen und zu dokumentieren {cite}`toolsfordata2026`.

Ein Beispiel für ein Open-Source-Werkzeug aus dem Bereich Data Testing ist <a href="https://greatexpectations.io/" class="external-link" target="_blank">Great Expectations</a>. Dabei handelt es sich um eine Python-Bibliothek, mit der Erwartungen an die Struktur und den Inhalt von Daten formuliert und automatisiert überprüft werden können. So lässt sich beispielsweise festlegen, dass eine Spalte einen bestimmten Datentyp besitzen, keine fehlenden Werte enthalten oder nur Werte innerhalb eines vorgegebenen Bereichs aufweisen darf. Great Expectations kann dabei unter anderem auf Dateien, Datenbanken und DataFrames angewendet werden {cite}`gxgreatexpectations`.

## Zusammenfassung

Die inhaltliche Überprüfung der Datenqualität ist für Fachfremde durchaus herausfordernd und kann viel Zeit in Anspruch nehmen. Daher hilft es, sich an den in diesem Unterkapitel genannten, allgemeinen Kriterien zur Prüfung von Datenqualität zu orientieren. In dem Beispielszenario dieser OER lagen die Daten bereits in einer herausragenden Qualität vor und mussten daher keinem langen Prüfungsverfahren unterzogen werden.

Bei der Einarbeitung in ein Projekt entsteht in der Regel ein Bild von möglichen Fragestellungen, Methodiken, Analysen und Ergebnissen. Dieses Verständnis kann genutzt werden, um die Forschungsdaten auf ihre Qualität zu prüfen. Die Aufbereitung von Daten eines fachfremden Projekts ist nicht das Ziel der Qualitätsprüfung. Zu prüfen ist stattdessen, ob die Forschungsdaten in einer guten Qualität vorliegen um einen Mehrwert für die wissenschaftliche Community erbringen zu können.

---

**Literatur**

```{bibliography}
:filter: docname in docnames
```
