(datenmanagement:organisation)=
# Organisation

Dieses Unterkapitel bezieht sich auf die Kompetenz "3.1 Organisation" des QUADRIGA Datenkompetenzframeworks - wie Abb. 3.3 zeigt.  
Das bedeutet, dass die im Projekt entstandenen Forschungsdaten an dieser Stelle geordnet und organisiert werden müssen, sodass sie auch projekt-extern bzw. interdisziplinär verstanden werden. Wenn im Lauf des Projektes noch kein Datenmanagementplan (DMP) begonnen wurde, muss nun einer angelegt werden.

```{figure} /assets/3.1_organisation.png
---
align: center
width: 33%
---
Die Kompetenz 3.1 Organisation des QUADRIGA Datenkompetenzframeworks.
```
*Quellenangabe: Ausschnitt aus dem Modell "QUADRIGA Datenkompetenzframework" von Petras et al. unter der Lizenz <a href="https://creativecommons.org/licenses/by/4.0/legalcode" class="external-link" target="_blank">CC BY 4.0</a> via <a href="https://zenodo.org/records/19470557" class="external-link" target="_blank">Zenodo</a>.*

---

## Ausgangslage

Die Daten müssen vor der Publikation geordnet und strukturiert werden. Zuerst müssen dazu jene Daten ausgewählt werden, die veröffentlicht werden sollen. Je nach Umfang sollten diese zudem geclustert werden. Darüber hinaus muss die Benennung der Daten und Dateien geprüft werden. Sind sie bereits nach einem (erkennbaren) Schema benannt? Wenn nicht, sollte das erwogen werden. Zudem sollten die Dateiformate geprüft werden: Liegen sie in proprietären Formaten vor oder nicht? Ist es sinnvoll, sie zu konvertieren, wenn sie in proprietären Formaten vorliegen?  
An dieser Stelle hilft es, sich zu fragen, ob die Daten so strukturiert und benannt sind, dass sie für Außenstehende verständlich sind.

## Vorgehen

*Hier könnten generische Lösungen präsentiert werden: Benennung nach welchen Schemata -> Beispiele, Listen, Links*

```{admonition} Weitere Informationen
:class: seealso
Das Rhein-Ruhr Zentrum für wissenschaftliche Datenqualität (<a href="https://www.dkz2r.de/" class="external-link" target="_blank">DKZ.2R</a>) hat ein so genanntes <a href="https://zenodo.org/records/17855527" class="external-link" target="_blank">Cheat Sheet</a> erstellt, auf dem wichtige Informationen zur Struktur und Benennung von Daten auf einer A4-Seite zusammengefasst sind.
```

Das oben genannte Datenmanagement wird mit der Anlage eines DMP erreicht. Wie Sie einen DMP anlegen, wird Schritt für Schritt im folgenden Abschnitt gezeigt.
*Folgende Tools kommen dazu in betracht: Tools für DMP nennen/verlinken; Wie lässt sich sonst noch ein DMP anlegen etc.*


## Beispiel Szenario Q-LCA 

*Nochmal eingehen auf Auswahl und clusterung der daten*
*Eingehen auf Datenbenennung*

Im Beispielszenario 'Q-LCA Forschungsdatenveröffentlichung' 
Ein DMP musste nachträglich geschrieben werden. Entscheidung für Repo (Wir haben uns für RDMO Brandenburg entschieden (weil bei uns entwickelt - diese Begründung reicht natürlich nicht;) ), Auswahl DFG Checkliste v5 (warum?)) https://rdmo.fdm-bb.de/ 

### Datenmanagementplan

Dieses Unterkapitel führt Sie Schritt für Schritt durch das Anlegen eines DMP am Beispiel des DMP für das Projekt Q-LCA, der mit dem Tool <a href="https://rdmo.fdm-bb.de/" class="external-link" class="external-link" target="_blank">RDMO</a> (Instanz Brandenburg) verfasst wurde.  
Bitte beachten Sie: Um selbst einen DMP anzulegen, müssen Sie sich registrieren - z. B. für den <a href="https://rdmo.fdm-bb.de/account/signup/" class="external-link" target="_blank">Brandenburger RDMO-Dienst</a>. Falls Sie sich nicht registrieren wollen oder können, werden Sie durch Beispielbilder trotzdem in der Lage sein, dem Erstellen eines Datenmanagementplans zu folgen.

Schritte sind u. a.:
- Auswahl und Ordnung (Auswahl und Clusterung der zu veröffentlichenden Forschungsdaten) -> Die Entscheidung über die Bereitstellung der Dateien (als Gesamt-ZIP, ZIP-"Pakete", einzeln) muss getroffen werden
- Dateibenennung (Benennung der Forschungsdaten nach einem Schema) -> Hier gilt es mitzunehmen, dass die Dateibenennung im Nachhinein sehr mühsam ist und das aufzupassen ist, dass keine Verständigungsprobleme auftauchen
- Metadaten (Angabe von Metadaten nach Konventionen der Disziplin)
- FAIRifizierung/FAIRification (Vollständigkeit der Beschreibung, Maximierung der Interoperabilität (was kann standardisiert werden -> nach ISO), *hier u. a. auch Formate*) -> dazu auch FAIRification von FD-Objekten: https://datascience.codata.org/articles/dsj-2021-004 
- README (README-Datei zur Dokumentation Anlegen)


## Learnings

- Struktur soweit wie möglich aus dem Projekt übernehmen (Strukturen und Benennungen sind nicht ohne Grund entstanden und folgen einer Logik)
- Für Quadriga mitnehmen: Dateibenennung im Nachhinein mühsam, aufpassen, dass keine Verständigungsprobleme entstehen.
- auch die Bereitstellung war ein Thema (als ZIP, Gesamt-ZIP, Teil-ZIP) -> logische Ordnung und Clusterung
- Versionierung und Dateibenennung Kompetenzen, die gebraucht werden, wenn man nachträglich aufarbeitet

---

**Literatur**

```{bibliography}
:filter: docname in docnames
:list: bullet
```

