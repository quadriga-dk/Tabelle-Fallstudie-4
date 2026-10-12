(datenmanagement:erschliessung)=
# Erschließung

Dieses Unterkapitel fokussiert die Kompetenz "3.2 Erschließung" des QUADRIGA Datenkompetenzframeworks. Dies umfasst die an Standards orientierte Auszeichnung bzw. Beschreibung von Daten.

```{figure} /assets/3.2_erschliessung.png
---
align: center
width: 33%
---
Die Kompetenz 3.2 Erschließung des QUADRIGA Datenkompetenzframeworks.
```
*Quellenangabe: Ausschnitt aus dem Modell "QUADRIGA Datenkompetenzframework" von Petras et al. unter der Lizenz <a href="https://creativecommons.org/licenses/by/4.0/legalcode" class="external-link" target="_blank">CC BY 4.0</a> via <a href="https://zenodo.org/records/19470557" class="external-link" target="_blank">Zenodo</a>.*

---

Schritte sind u. a.:
- Metadaten (Angabe von Metadaten nach Konventionen der Disziplin)
- FAIRifizierung/FAIRification (Vollständigkeit der Beschreibung, Maximierung der Interoperabilität (was kann standardisiert werden -> nach ISO), *hier u. a. auch Formate*) -> dazu auch FAIRification von FD-Objekten: https://datascience.codata.org/articles/dsj-2021-004 
- README (README-Datei zur Dokumentation Anlegen)

## Ausgangslage

Im Rahmen der Erschließung der Daten, müssen **Metadaten** vergeben werden, wenn das an anderer Stelle noch nicht geschehen ist. Dies sollte nach den Konventionen der Disziplin geschehen, aus der die Forschungsdaten stammen.  
Die Daten und Metadaten sollten eine **FAIRifizierung** durchlaufen, d. h. möglichst vollständig beschrieben werden. Dazu sollte, wo es möglich ist, auf Standards zurückgegriffen werden.   
Auch eine **README** gehört zu einer guten Datenbeschreibung. Darin sollten Sie alles dokumentieren, was Nachnutzende über die Daten wissen sollten.

## Vorgehen

**Metadaten**

Recherchieren Sie, ob es disziplinspezifische Vorgaben für Metadaten gibt. Eine gute <a href="https://rdamsc.bath.ac.uk/" class="external-link" target="_blank">Übersicht</a> über Metadatenstandards hat die englische Universität Bath angelegt. 

Die folgende Übersicht zeigt zudem beispielhaft einige etablierte Metadatenstandards verschiedener Fachdisziplinen.

| Disziplin | Metadatenstandard | Organisation | Quelle |
|---|---|---|---|
| Astronomie | IVOA Technical Specifications | IVOA | {cite}`ivoa_2026` |
| Bauwesen/Stadtplanung | XPlanung (ergänzt durch XBau) | XLeitstelle | {cite}`xleitstelle_2018` |
| Biodiversität | Darwin Core | TDWG | {cite}`wieczorek_et_al_2012` |
| Fachübergreifend | DataCite Metadata Schema | DataCite | {cite}`datacite_2026` |
| Geisteswissenschaften | TEI (Text Encoding Initiative) | TEI Consortium | {cite}`tei_consortium_2026` |
| Geodaten | ISO 19115 | ISO | {cite}`iso_19115_2014` |
| Klimaforschung | CF Conventions | CF Conventions Community | {cite}`cf_conventions_2026` |
| Kulturerbe | CIDOC CRM | CIDOC CRM SIG / ISO | {cite}`iso_21127_2023` |
| Medizin | CDISC (u. a. CDASH, SDTM, ODM) | CDISC | {cite}`cdisc_2026` |
| Sozialwissenschaften | DDI (Data Documentation Initiative) | DDI Alliance | {cite}`ddi_alliance_2026` |

Eine übergreifende Übersicht bietet zudem <a href="https://fairsharing.org" class="external-link" target="_blank">FAIRsharing</a> {cite}`sansone_et_al_2019`.

---

**FAIRifizierung**

Prüfen Sie, ob die Beschreibung der Daten vollständig ist. Maximieren Sie nach Möglichkeit die Interoperabilität der Daten. Recherchieren Sie, was standardisiert beschrieben werden kann (z. B. nach ISO). 

`````{admonition} Weitere Informationen
:class: tip

Die FAIRifizierung von Forschungsdaten kann sowohl mithilfe von Checklisten und Reifegradmodellen als auch mit automatisierten Prüfwerkzeugen unterstützt werden. Eine ausführliche Einführung in die FAIR-Prinzipien sowie weitere Hintergrundinformationen finden Sie bereits in der <a href="https://quadriga-dk.github.io/Tabelle-Fallstudie-1/Markdown/3_1_FairPrinzipien.html" class="external-link" target="_blank">1. Fallstudie, Kapitel 3.1 „FAIR-Prinzipien“</a>. Dort werden unter anderem folgende Ansätze vorgestellt:

- **Checkliste:** die kompakte FAIR-Checkliste von Jones und Grootveld (2017)
- **Webtool:** das deutschsprachige <a href="https://forschungsdaten-thueringen.de/fair-assessment-tool/articles/fair-assessment-tool.html" class="external-link" target="_blank">FAIR Assessment Tool</a> des Thüringer Kompetenznetzwerks Forschungsdatenmanagement (TKFDM), basierend auf dem FAIR Assessment Tool der Australian Research Data Commons
- **FAIR Data Maturity Model:** das detaillierte Reifegradmodell der <a href="https://www.rd-alliance.org/groups/fair-data-maturity-model-wg/outputs/?output=94549" target="_blank">Research Data Alliance</a> (RDA), auf <a href="https://zenodo.org/records/5834115" target="_blank">Deutsch</a> verfügbar über das Projekt <a href="https://www.ecodm.de/" target="_blank">EcoDM</a>

Neben manuellen Checklisten und Reifegradmodellen stehen auch automatisierte Prüfwerkzeuge zur Verfügung. Diese bewerten die FAIRness eines Datensatzes anhand eines Persistent Identifiers (PID) oder einer URL und geben unmittelbar Rückmeldung darüber, welche FAIR-Kriterien bereits erfüllt sind und wo Verbesserungsbedarf besteht.

- <a href="https://www.f-uji.net/" class="external-link" target="_blank">F-UJI</a> – automatische FAIR-Bewertung anhand eines PID oder einer URL
- <a href="https://fair-checker.france-bioinformatique.fr/" class="external-link" target="_blank">FAIR-Checker</a> – automatische Analyse der FAIR-Metadaten eines Datensatzes
- <a href="https://fairaware.dans.knaw.nl/" class="external-link" target="_blank">FAIR-Aware</a> – unterstützt Forschende bei der Selbstbewertung anhand eines kurzen Fragenkatalogs
`````

---

**README**

Eine README-Datei ist die einfachste Form der Datendokumentation und soll sicherstellen, dass Daten auch später oder von anderen Personen korrekt interpretiert werden können {cite}`hassenstein_jung_2025`. Sie sollte einer Datenpublikation als einfache Datei im Format .txt beigelegt werden. Alternativ können Sie die Daten im Repositorium beschreiben, wenn das möglich ist.

Die folgende Vorlage kann als Orientierung für den Aufbau einer README-Datei dienen.

```{admonition} Beispiel: Vorlage für eine README-Datei
:class: hinweis, dropdown

**ALLGEMEINE INFORMATIONEN**

- Titel des Projekts
- Autor:innen und Kontaktinformationen
- Zeitraum und Ort der Datenerhebung
- Angaben zum Förderprojekt

**WEITERGABE UND ZUGANG**

- Lizenz
- Empfohlene Zitierweise
- Zugehörige Publikationen

**DATEN- UND DATEIÜBERSICHT**

- Beschreibung der Dateien
- Datei- und Ordnerstruktur
- Versionen

**METHODISCHE INFORMATIONEN**

- Datenerhebung
- Datenverarbeitung
- Verwendete Software
- Qualitätssicherung

**DATEISPEZIFISCHE INFORMATIONEN**

- Variablen
- Fehlende Werte
- Besonderheiten
```
*Vorlage aus dem Englischen übersetzt und gekürzt nach* {cite}`ucsb_library_2024` *(CC BY 4.0).*

Als ergänzende Hilfestellung stellt <a href="https://data.research.cornell.edu/data-management/sharing/readme/" class="external-link" target="_blank">Cornell Data Services</a> eine ausführliche Anleitung sowie eine frei verfügbare Vorlage für README-Dateien bereit.

```{admonition} Weitere Materialien
class: seealso
Vor allem die Methodischen Informationen variieren naturgemäß stark zwischen den Fachrichtungen. Einzelne NFDI-Konsortien haben daher eigene Tempaltes für READMEs erstellt, so zum Beispiel die <a href="https://zenodo.org/records/21619429" class="external-link" target="_blank">NFDI4Chem</a>. 
```


## Beispiel Szenario Q-LCA 

*Speziellen Fall unseres Szenarios schildern, z. B. In dem in diesem Szenario abgebildeten Fall ist eine Qualitätsprüfung nicht notwendig, weil die Daten bereits gut aufgearbeitet vorliegen.*

## Learnings

*können möglicherweise auch ins Resümee*
*Ableitung von generischen Lösungen, die interdisziplinär oder wenigstens über das Beispielszenario hinaus Anwendung finden können.*

---

**Literatur**

```{bibliography}
:filter: docname in docnames
```


