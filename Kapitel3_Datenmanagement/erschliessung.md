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

## Ausgangslage

Im Rahmen der Erschließung der Daten, müssen **Metadaten** vergeben werden, wenn das an anderer Stelle noch nicht geschehen ist. Dies sollte nach den Konventionen der Disziplin geschehen, aus der die Forschungsdaten stammen.  
Die Daten und Metadaten sollten eine **FAIRifizierung** durchlaufen, d. h. möglichst vollständig beschrieben werden. Dazu sollte, wo es möglich ist, auf Standards zurückgegriffen werden.   
Auch eine **README** gehört zu einer guten Datenbeschreibung. Darin sollten Sie alles dokumentieren, was Nachnutzende über die Daten wissen wollen.

## Vorgehen

**Metadaten**
Recherchieren Sie, ob es disziplinspezifische Vorgaben für Metadaten gibt.

<span style="color:red">*Angebot machen, auf welchen Seiten das recherchiert werden kann.*</span>

Die folgende Übersicht zeigt Beispiele etablierter Metadatenstandards verschiedener Fachdisziplinen.
| Disziplin | Metadatenstandard | Organisation | Quelle |
|---|---|---|---|
| Astronomie | IVOA Technical Specifications | IVOA | {cite}`ivoa_2026` |
| Bauwesen/Stadtplanung | XPlanung (ergänzt durch XBau)¹ | XLeitstelle | {cite}`xleitstelle_2018` |
| Biodiversität | Darwin Core | TDWG | {cite}`wieczorek_et_al_2012` |
| Fachübergreifend | DataCite Metadata Schema | DataCite | {cite}`datacite_2026` |
| Geisteswissenschaften | TEI (Text Encoding Initiative) | TEI Consortium | {cite}`tei_consortium_2026` |
| Geodaten | ISO 19115 | ISO | {cite}`iso_19115_2014` |
| Klimaforschung | CF Conventions | CF Conventions Community | {cite}`cf_conventions_2026` |
| Kulturerbe | CIDOC CRM | CIDOC CRM SIG / ISO | {cite}`iso_21127_2023` |
| Medizin | CDISC (u. a. CDASH, SDTM, ODM) | CDISC | {cite}`cdisc_2026` |
| Sozialwissenschaften | DDI (Data Documentation Initiative) | DDI Alliance | {cite}`ddi_alliance_2026` |

¹ XBau ist ein eigener Standard für Baugenehmigungsverfahren, ergänzend zu XPlanung.

Eine übergreifende Übersicht bietet zudem <a href="https://fairsharing.org" class="external-link" target="_blank">FAIRsharing</a> {cite}`sansone_et_al_2019`.

**FAIRifizierung**
Prüfen Sie, ob die Beschreibung der Daten vollständig ist. Maximieren Sie nach Möglichkeit die Interoperabilität der Daten. Recherchieren Sie, was standardisiert beschrieben werden kann (z. B. nach ISO). 

<span style="color:red">*Angebot machen, wie das geprüft werden kann, z. B. durch Checklisten, Webseiten etc.*</span>

**README**
Legen Sie eine README an.

<span style="color:red">*Beispiele für gute README bereitstellen. Hilfe zum Schreiben einer guten README zusammenstellen bzw. auf bestehende Listen verweisen.*</span>


Eine README-Datei ist die einfachste Form der Datendokumentation und soll sicherstellen, dass Daten auch später oder von anderen Personen korrekt interpretiert werden können {cite}`hassenstein_jung_2025`.

Die folgende Vorlage kann als Orientierung für den Aufbau einer README-Datei dienen.

```{admonition} Beispiel: Vorlage für eine README-Datei
:class: hinweis, dropdown
Diese README.txt-Datei wurde am JJJJ-MM-TT von NAME erstellt <Hinweistexte stehen in spitzen Klammern und können vor dem Speichern gelöscht werden>

ALLGEMEINE INFORMATIONEN
1. Titel des Projekts:
2. Angaben zu den Autor:innen
   A. Kontaktinformationen Projektleitung: Name: Institution: Adresse: E-Mail:
   B. Kontaktinformationen Ko-Autor:innen: Name: Institution: Adresse: E-Mail:
   C. Alternative Kontaktperson: Name: Institution: Adresse: E-Mail:
3. Datum der Datenerhebung (Einzeldatum, Zeitraum oder ungefähres Datum) <empfohlenes Format JJJJ-MM-TT; bei mehreren Dateien entsprechend einzeln angeben>:
4. Geografischer Ort der Datenerhebung: <Breiten-/Längengrad oder Stadt/Region, Bundesland, Land; bei mehreren Datenquellen entsprechend angeben>:
5. Angaben zu Förderquellen, die die Datenerhebung unterstützt haben:

WEITERGABE-/ZUGANGSINFORMATIONEN
1. Lizenzen/Einschränkungen bezüglich der Daten:
2. Links zu Publikationen, die die Daten zitieren oder nutzen:
3. Links zu weiteren öffentlich zugänglichen Fundorten der Daten:
4. Links/Beziehungen zu ergänzenden Datensätzen: <weitere unterstützende Datenquellen, die zur Analyse oder Klassifikation herangezogen wurden>
5. Wurden die Daten aus einer anderen Quelle abgeleitet? Falls ja, Quelle(n) angeben: <Zitationen der Originalquellen>
6. Empfohlene Zitierweise für das Projekt:

DATEN- UND DATEIÜBERSICHT
1. Dateiliste: <alle Dateien (bzw. Ordner) im Datensatz mit kurzer Inhaltsbeschreibung auflisten>
2. Beziehung zwischen den Dateien, falls relevant:
3. Zusätzliche verwandte Daten, die erhoben, aber nicht in dieses Datenpaket aufgenommen wurden:
4. Gibt es mehrere Versionen des Datensatzes? <Falls ja: Name der aktualisierten Datei(en); warum und wann wurde die Datei aktualisiert?>

METHODISCHE INFORMATIONEN
1. Beschreibung der Methoden zur Datenerhebung/-generierung: <Links/Verweise auf Publikationen oder Dokumentation zu Versuchsaufbau bzw. verwendeten Protokollen>
2. Methoden der Datenverarbeitung: <wie wurden die übermittelten Daten aus den Rohdaten erzeugt?>
3. Geräte- oder softwarespezifische Informationen zur Interpretation der Daten: <vollständiger Name und Version der Software sowie benötigte Pakete/Bibliotheken>
4. Standards und Kalibrierungsinformationen, falls zutreffend:
5. Umgebungs-/Versuchsbedingungen:
6. Beschreibung durchgeführter Qualitätssicherungsmaßnahmen:
7. Beteiligte Personen bei Probenahme, Verarbeitung, Analyse und/oder Einreichung:

DATENSPEZIFISCHE INFORMATIONEN FÜR: [DATEINAME] <diesen Abschnitt für jeden Datensatz/Ordner/Datei wiederholen>
1. Anzahl der Variablen:
2. Anzahl der Fälle/Zeilen:
3. Variablenliste: <Variablennamen, Beschreibungen, Einheiten und ggf. Wertelabels>
4. Codes für fehlende Daten: <Code/Symbol und Definition>
5. Spezielle Formate oder verwendete Abkürzungen:
```
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


