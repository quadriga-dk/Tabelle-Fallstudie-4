# Forschungsdatenpublikation: Ein Best-Practice-Beispiel zur retrospektiven Publikation von Daten für die Nachnutzung

````{margin}
```{admonition} Fragen oder Feedback
:class: frage-feedback

<a href="https://github.com/quadriga-dk/Tabelle-Fallstudie-4/issues/new?assignees=&labels=question&projects=&template=frage.yml" class="external-link" target="_blank">
    Stellen Sie eine Frage
</a> <br>
<a href="https://github.com/quadriga-dk/Tabelle-Fallstudie-4/issues/new?assignees=&labels=feedback&projects=&template=feedback.yml" class="external-link" target="_blank">
    Geben Sie uns Feedback
</a>

Mit Ihren Rückmeldungen können wir unser interaktives Lehrbuch gezielt an Ihre Bedürfnisse anpassen.



```
````

`````{margin}
````{admonition} Zitierhinweis
:class: citation-information
```{literalinclude} /CITATION.bib
:language: bibtex
```
Walter, P., Neuroth, H. & Plomin, J. (2026). _Forschungsdatenpublikation: Ein Best-Practice-Beispiel zur retrospektiven Publikation von Daten für die Nachnutzung. QUADRIGA Open Educational Resources: Tabelle 4._ 

````
`````

Diese Open Educational Resource (OER) führt Sie anhand eines konkreten Beispiels Schritt für Schritt durch das nachträgliche Publizieren von Forschungsdaten für die Nachnutzung. Dies geschieht ohne konkretes Nutzungsszenario, sodass die hier erarbeiteten Prozesse und Ergebnisse unabhängig vom gewählten Beispiel für alle Fachrichtungen von Interesse sein können.  

Die Lerneinheit orientiert sich an den Learnings, die sich durch die Begleitung zur Publikation und Dokumentation von Forschungsdaten des Projekts <a href="https://www.fh-potsdam.de/forschung-transfer/projekte/q-lca" class="external-link" target="_blank">Q-LCA</a> von <a href="https://orcid.org/0000-0001-7738-7627" class="external-link" target="_blank">Prof. Dr.-Ing. Michael Prytula</a> (Fachhochschule Potsdam) und <a href="https://orcid.org/0000-0003-2507-6469" class="external-link" target="_blank">Prof. Dipl.-Ing. Tim Rieniets</a> (Leibniz Universität Hannover) an der <a href="https://www.fh-potsdam.de/" class="external-link" target="_blank">Fachhochschule Potsdam</a> ergeben haben. Diese wurden abstrahiert und generisch formuliert, sodass die Erkenntnisse auch für andere Wissenschaftsdisziplinen umgesetzt werden können.

Als Grundlage dient das <a href="https://zenodo.org/records/14747822" class="external-link" target="_blank">QUADRIGA Datenkompetenzframework</a>, dessen Phasen den wissenschaftlichen Forschungsprozess abbilden. Auch der Prozess des nachträglichen Veröffentlichens von Forschungsdaten lässt sich mit diesem Modell fassen und organisieren, wobei dann nicht auf alle im Modell dargstellten Kompetenzen eingegangen werden muss (s. Kap. 1.3 [Nachträgliches Publizieren](nachpub:einleitung)).  

```{figure} /assets/collage_intro.png
---
align: center
width: 75%
---
Collage aus Bildern zu Themen, die in dieser OER behandelt werden (mit <a href="https://gemini.google.com/?utm_medium=paid-media&utm_campaign=nano_banana_pro_sem_bkws&gclsrc=aw.ds&gad_source=1&gad_campaignid=23262150693" class="external-link" target="_blank">Google Gemini</a> erstellte Collage aus in dieser OER verwendeten Abbildungen).
```
## Zielgruppe

Dieses Lehrbuch richtet sich an Forschende, die eigene, bisher unveröffentlichte Forschungsdaten veröffentlichen oder die Daten anderer Wissenschafler:innen aufarbeiten wollen. Darüber hinaus sind auch Forschungsdatenmanagement(FDM)-Beauftragte an Hochschulen angesprochen.  
Die Lerneinheiten des Datentyps Tabelle sind für alle wissenschaftlichen Disziplinen, Lernende und Lehrende geeignet, die mit Tabellen oder strukturierten Daten arbeiten und einzelne Kapitel nachnutzen wollen oder - in diesem Fall - Forschungsdaten nachträglich veröffentlichen wollen.

## Struktur der OER

Anders als andere im Datenkompetenzzentrum QUADRIGA entworfenen <a href="https://quadriga-dk.github.io/fallstudien/" class="external-link" target="_blank">Lerneinheiten</a>, handelt es sich bei dieser OER um ein Szenario und nicht um eine Fallstudie, da dieser Lerneinheit keine spezifische Forschungsfrage zugrunde liegt. Thematischer Fokus ist hier, wie Forschungsdaten aus früheren Projekten nachträglich und entsprechend den <a href="https://zenodo.org/records/6247015" class="external-link" target="_blank">FAIR-Prinzipien</a> publiziert werden können. Dabei ist das Szenario wie ein Walkthrough aufgebaut, das die Nutzer:innen Schritt für Schritt (vgl. Abb. 2) durch die Vorbereitungen zur Veröffentlichung führt, Fallstricke identifiziert und Lösungen anbietet.

Die folgende Abbildung zeigt die 3 Schritte dieses Szenarios, die den Hauptkapiteln entsprechen.

```{figure} /assets/steps_cs4.png
---
align: left
width: 75%
---
Visualisierung der 3 Schritte dieses Lehrbuchs.
```

In dieser OER werden die folgenden Schritte durchlaufen, die als elementar in der nachträglichen Datenpublikation bezeichnet werden können und die mit den Datenflussphasen und Kompetenzen aus dem QUADRIGA Datenkompetenzframework übereinstimmen (s. Kap. 1.3 {ref}`Nachträgliches Publizieren<nachpub:einleitung>`).

- Im **1. Schritt** gilt es, sich in das Projekt einzuarbeiten und den Ablauf zur Publikation zu planen (Datenflussphase *1. Planung*). Dazu wird eine Qualitätsprüfung durchgeführt, um sicherzustellen, dass die Daten in der Art und Weise wie sie vorliegen, den Ansprüchen genügen sowie (mögliche) Vorgaben und juristische Aspekte beleuchtet (s. Kap. 2 {ref}`Planung<eplanung:einleitung>`).
- Im **2. Schritt** folgt mit dem Datenmanagement die Datenflussphase *3. Organisation und Erschließung*. Dabei werden die Daten für eine Publikation geordnet und ein Datenmanagementplan angelegt (s. Kap. 3 {ref}`Datenmanagement<datenmanagement:einleitung>`). 
- Im **3. Schritt** werden die Kompetenzen *5.1 Aufbewahrung*, *5.2 Publikation* und *5.3 Kommunikation* von Forschungsdaten behandelt, indem u. a. ein Repositorium zur Datenveröffentlichung ausgewählt wird und Kommunikationskanäle vorgestellt werden (s. Kap. 4 {ref}`Publikation<publikation:einleitung>`).

