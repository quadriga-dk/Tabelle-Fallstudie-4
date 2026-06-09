(datenmanagement:organisation)=
# Organisation

Dieses Unterkapitel bezieht sich auf die Kompetenz "3.1 Organisation" des QUADRIGA Datenkompetenzframeworks:

*Bild der Kompetenz 3.1 Organisation einfügen*

Dies bedeutet, dass die im Projekt entstandenen Forschungsdaten an dieser Stelle geordnet und organisiert werden müssen. Wenn zum Beispiel noch kein Datenmanagementplan (DMP) vorliegt, muss nun einer angelegt werden.  
Dieses Lehrbuch führt Sie Schritt für Schritt durch das Anlegen eines DMP am Beispiel des DMP für das Projekt Q-LCA, der mit dem Tool <a href="https://rdmo.fdm-bb.de/" class="external-link" class="external-link" target="_blank">RDMO</a> (Instanz Brandenburg) verfasst wurde. 

---

**Aufbau jeder Lerneinheit/jedes Unterkapitels:**

**Problem**
Problembeschreibung, z. B. Vorliegende Daten müssen auf ihre Qualität überprüft werden.

**Lösung**
Problemlösung skizzieren, z. B. Die Daten müssen geprüft werden.

**Beispiel Szenario Michael** 
Speziellen Fall unseres Szenarios schildern, z. B. In dem in diesem Szenario abgebildeten Fall ist eine Qualitätsprüfung nicht notwendig, weil die Daten bereits gut aufgearbeitet vorliegen.

**Learnings (generisch)** 
*können möglicherweise auch ins Resümee*
Ableitung von generischen Lösungen, die interdisziplinär oder wenigstens über das Beispielszenario hinaus Anwendung finden können.

---

Datenmanagement
Management im Sinne von Ordnung; dabei so ordnen, dass sie auch interdisziplinär bzw. projekt-extern verstanden werden 
·	DMP
·	DMP anlegen, wenn keiner vorhanden ist (
·	Datenauswahl
·	Auswahl und Clustertung der zu veröffentlichenden Forschungsdaten
·	Datenbenennung
·	Benennung der Daten nach Schema
·	Dateiformate konvertieren? (in nicht-proprietär -> möglich? Sinnvoll?) https://ianus-fdz.de/langzeitarchivierung/
·	Metadaten
·	Angabe von Metadaten nach Konventionen der Disziplin (XPlanung, XBau?)/ generischen Standards (DC; DCAT-AP.de?)
·	FAIRifizierung
·	Vollständigkeit der Beschreibung, Maximierung der Interoperabilität (was kann standardisiert werden -> nach ISO)
·	README
·	README zur Dokumentation anlegen



## Datenmanagementplan

### Problem

Es gibt keinen Datenmanagementplan für die im Projekt entstandenen Forschungsdaten.

### Lösung

Ein DMP muss angelegt werden.
*Tools für DMP nennen/verlinken; Wie lässt sich sonst noch ein DMP anlegen etc.*

### Beispiel Szenario Q-LCA 

Ein DMP musste nachträglich geschrieben werden. Entscheidung für Repo (Wir haben uns für RDMO Brandenburg entschieden (weil bei uns entwickelt), Auswahl DFG Checkliste v5 (warum?)) https://rdmo.fdm-bb.de/ 

### Learnings (generisch)
*können möglicherweise auch ins Resümee*

·	Struktur soweit wie möglich aus dem Projekt übernehmen (Strukturen und Benennungen sind nicht ohne Grund entstanden und folgen einer Logik)
·	Für Quadriga mitnehmen: Dateibenennung im Nachhinein mühsam, aufpassen, dass keine Verständigungsprobleme entstehen.
·	auch die Bereitstellung war ein Thema (als ZIP, Gesamt-ZIP, Teil-ZIP) -> logische Ordnung und Clusterung
·	Versionierung und Dateibenennung Kompetenzen, die gebraucht werden, wenn man nachträglich aufarbeitet



(Bitte beachten Sie: Um selbst einen DMP anzulegen, müssen Sie sich registrieren - z. B. für den <a href="https://rdmo.fdm-bb.de/account/signup/" class="external-link" target="_blank">Brandenburger RDMO-Dienst</a>. Falls Sie sich nicht registrieren wollen oder können, werden Sie durch Beispielbilder trotzdem in der Lage sein, dem Erstellen eines Datenmanagementplans zu folgen.)
Schritte sind u. a.:
- Auswahl und Ordnung (Auswahl und Clusterung der zu veröffentlichenden Forschungsdaten) -> Die Entscheidung über die Bereitstellung der Dateien (als Gesamt-ZIP, ZIP-"Pakete", einzeln) muss getroffen werden
- Dateibenennung (Benennung der Forschungsdaten nach einem Schema) -> Hier gilt es mitzunehmen, dass die Dateibenennung im Nachhinein sehr mühsam ist und das aufzupassen ist, dass keine Verständigungsprobleme auftauchen
- Metadaten (Angabe von Metadaten nach Konventionen der Disziplin)
- FAIRifizierung/FAIRification (Vollständigkeit der Beschreibung, Maximierung der Interoperabilität (was kann standardisiert werden -> nach ISO), *hier u. a. auch Formate*) -> dazu auch FAIRification von FD-Objekten: https://datascience.codata.org/articles/dsj-2021-004 
- README (README-Datei zur Dokumentation Anlegen)

```{admonition} Weitere Informationen
:class: seealso

Das Rhein-Ruhr Zentrum für wissenschaftliche Datenqualität (<a href="https://www.dkz2r.de/" class="external-link" target="_blank">DKZ.2R</a>) hat ein so genanntes <a href="https://zenodo.org/records/17855527" class="external-link" target="_blank">Cheat Sheet</a> erstellt, auf dem wichtige Informationen zur Struktur und Benennung von Daten auf einer A4-Seite zusammengefasst sind.

```

**Literatur**

```{bibliography}
:filter: docname in docnames
:list: bullet
```

