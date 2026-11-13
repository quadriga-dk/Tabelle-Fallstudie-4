(datenmanagement:erschliessung)=
# Erschließung

Dieses Unterkapitel fokussiert die Kompetenz *3.2 Erschließung* des QUADRIGA Datenkompetenzframeworks. Dies umfasst die an Standards orientierte Auszeichnung bzw. Beschreibung von Daten.

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

Im Rahmen der Erschließung der Daten müssen **Metadaten** vergeben werden, wenn das an anderer Stelle noch nicht geschehen ist. Dies sollte möglichst umfangreich und standardisiert sowie unter Beachtung der Konventionen der Disziplin erfolgen, aus der die Forschungsdaten stammen.  
Auch eine **README** gehört zu einer guten Datenbeschreibung. Darin sollten Sie alles dokumentieren, was Nachnutzende über die Daten wissen sollten.

## Vorgehen

**Metadaten**

Recherchieren Sie, ob es disziplinspezifische Vorgaben für Metadaten gibt. Eine Übersicht über etablierte Standards finden Sie beispielsweise:
- im <a href="https://rdamsc.bath.ac.uk/" class="external-link" target="_blank">Metadata Standards Catalog</a> der englischen Universität Bath 
- und auf der Webseite von <a href="https://fairsharing.org/" class="external-link" target="_blank">FAIRsharing</a>.

Fachübergreifende Metadatenstandards sind z. B.:
- das <a href="https://schema.datacite.org/" class="external-link" target="_blank">DataCite Schema</a> von DataCite
- die <a href="https://www.dublincore.org/specifications/dublin-core/dcmi-terms/" class="external-link" target="_blank">Dublin Core</a> genannten Schemata ("terms/namespace" und "elements/1.1/namespace") der Dublin Core Metadata Initiative (DCMI)
- das Vokabular von <a href="https://schema.org/" class="external-link" target="_blank">schema.org</a>

Darüber hinaus finden Sie Informationen zu fachspezifischen Standards bei den Konsortien der Nationalen Forschungsdateninfrastruktur (<a href="https://www.nfdi.de/konsortien/" class="external-link" target="_blank">NFDI</a>) sowie deren Sektion <a href="https://www.nfdi.de/section-metadata/" class="external-link" target="_blank">(Meta)data, Terminology, Provenance</a>.

Einen Überblick über das Thema Metadaten und Metadatenstandards finden Sie zudem auf der Informationsseite <a href="https://forschungsdaten.info/fdm-allgemein/beschreiben-und-dokumentieren/metadaten-und-metadatenstandards" class="external-link" target="_blank">forschungsdaten.info</a>

---

**README**

Eine README-Datei ist die einfachste Form der Datendokumentation und soll sicherstellen, dass Daten auch später oder von anderen Personen korrekt interpretiert werden können {cite}`hassenstein_jung_2025`. Sie sollte einer Datenpublikation als einfache Datei im Format .txt beigelegt werden. Alternativ können Sie die Daten im Repositorium beschreiben, wenn das möglich ist.

Die folgende Vorlage kann als Orientierung für den Aufbau einer README-Datei dienen. Es ist die aus dem Englischen übersetzte und gekürzte Version eines README-Templates der UCSB (s. Lizenzhinweis unter dem Kasten) {cite}`ucsb_library_2024`.

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

---

Lizenzhinweis: Vorlage "README template" des Research Data Services (<a href="https://www.library.ucsb.edu/research-data-services" class="external-link" target="_blank">RDS</a>) der University of California, Santa Barbara (UCSB) unter der Lizenz <a href="https://creativecommons.org/licenses/by/4.0/" class="external-link" target="_blank">CC BY 4.0</a> via <a href="https://zenodo.org/records/10828379" class="external-link" target="_blank">Zenodo</a>.

---

```{admonition} Weitere Materialien
:class: seealso
Vor allem die Methodischen Informationen variieren naturgemäß stark zwischen den Fachrichtungen. Einzelne NFDI-Konsortien haben daher eigene Templates für READMEs erstellt, so zum Beispiel die <a href="https://zenodo.org/records/21619429" class="external-link" target="_blank">NFDI4Chem</a>. 
```

---

**Literatur**

```{bibliography}
:filter: docname in docnames
```


