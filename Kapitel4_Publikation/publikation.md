(publikation:publikation)=
# Publikation

Nachdem im vorigen Unterkapitel ein Repositorium für die Datenpublikation ausgewählt wurde, gilt es nun, die Daten darin zu publizieren. Dazu werden Methoden und Standards entsprechend der Kompetenz *5.2 Publikation* (s. Abb. 4.6) vorgestellt.

```{figure} /assets/5.2_publikation.png
---
align: center
width: 33%
---
Die Kompetenz '5.2 Publikation' des QUADRIGA Datenkompetenzframeworks.
```
*Quellenangabe: Ausschnitt aus dem Modell "QUADRIGA Datenkompetenzframework" von Petras et al. unter der Lizenz <a href="https://creativecommons.org/licenses/by/4.0/legalcode" class="external-link" target="_blank">CC BY 4.0</a> via <a href="https://zenodo.org/records/19470557" class="external-link" target="_blank">Zenodo</a>.*


## Ausgangslage 

Die Forschungsdaten für die im vorherigen Unterkapitel ein Repositorium ausgewählt wurde, müssen nun final geprüft und hochgeladen werden. Die Plattform für das Publizieren und Teilen von Daten entspricht in dem hier geschilderten Fall dem Auswählen eines Repositoriums.

Die hier zu beachtenden Punkte lassen sich in 3 Teile gliedern. Diese sind zum größten Teil Prüfschritte, da Sie, wenn Sie dieser Anleitung gefolgt sind, alle Aspekte bereits erledigt haben sollten. 

1. Metadaten und PID (inkl. Dokumentation)
2. FAIR-Assessment und GwP (inkl. Zitationshinweis)
3. Versionierung und Upload


### 3. Upload und Veröffentlichung auf Zenodo

Wenn Sie sich für <a href="https://zenodo.org/" class="external-link" target="_blank">Zenodo</a> als Repositorium entschieden haben, können Sie Ihre Forschungsdaten dort in wenigen Schritten veröffentlichen.

1. **Daten für den Upload vorbereiten:** Stellen Sie zunächst ein Datenpaket zusammen, das die zu veröffentlichenden Forschungsdaten, die zugehörigen Metadaten und die zugehörige Dokumentation enthält. Wenn Sie dieser Anleitung gefolgt sind, haben Sie die Daten bereits in Kapitel 3 [Datenmanagement](datenmanagement:einleitung) geordnet und durch einen DMP beschrieben. Dieser gehört ebenfalls in das Datenpaket.

2. **Zenodo-Konto erstellen:** Für den Upload benötigen Sie ein Zenodo-Konto. Dieses kann mit einer E-Mail-Adresse, über GitHub, ORCID oder OpenAIRE erstellt werden. Die Anmeldung über ORCID wird empfohlen, da die Ersteller:innen eines Zenodo-Eintrags dadurch eindeutig identifiziert werden können.

```{figure} /assets/zenodo_login.png
---
align: center
width: 75%
---
Screenshot des Logins zu Zenodo.
```
*Quellenangabe: Screenshot des Logins zu <a href="https://zenodo.org/records/19470557" class="external-link" target="_blank">Zenodo</a> vom 14.09.2026.*

3. **Dateien hochladen:** Legen Sie über **„New upload“** einen neuen Eintrag an und laden Sie die vorbereiteten Dateien hoch. Soll eine hierarchische Ordnerstruktur erhalten bleiben, können die Dateien als ZIP-Archiv hochgeladen werden.

```{figure} /assets/zenodo_newupload.png
---
align: center
width: 100%
---
Screenshot des Anlegens eines neuen Uploads.
```
*Quellenangabe: Screenshot des Anlegens eines neuen Uploads bei <a href="https://zenodo.org/records/19470557" class="external-link" target="_blank">Zenodo</a> vom 14.09.2026.*

Wenn Sie mehrere Uploads tätigen wollen, beachten Sie die Upload-Reihenfolge (bei Zenodo z. B. nach Datum, d.h. der erste Upload steht später unten). Innerhalb eines Uploads wird nach Namen sortiert, d. h. hier agieren Sie am besten mit Nummern oder stellen, wie vorgeschlagen, das ganze Datenpaket als ZIP zur Verfügung. Die Daten(pakete) können einfach per Drag-and-Drop hinzugefügt werden.

```{figure} /assets/zenodo_data.png
---
align: center
width: 75%
---
Screenshot des Drag-and-Drop-Feldes.
```
*Quellenangabe: Screenshot des Drag-and-Drop-Feldes eines neuen Uploads bei <a href="https://zenodo.org/records/19470557" class="external-link" target="_blank">Zenodo</a> vom 14.09.2026.*

4. **Datensatz beschreiben und Zugriffsrechte festlegen:** Beschreiben Sie den Datensatz mithilfe der Metadatenfelder. Füllen Sie so viele Felder wie möglich aus. Für den Eintrag kann ein neuer DOI generiert oder ein bereits zugewiesener DOI angegeben werden. Ergänzend können beispielsweise Schlagwörter, Förderinformationen oder Verknüpfungen zu verwandten Publikationen angegeben werden. Legen Sie außerdem unter **„Visibility“** fest, wie der Datensatz zugänglich sein soll. Hier sollte "öffentlich" der Standard sein.

```{figure} /assets/zenodo_metadata.png
---
align: center
width: 75%
---
Screenshot einiger Metadatenfelder.
```
*Quellenangabe: Screenshot des Anfangs der Metadatenfelder bei <a href="https://zenodo.org/records/19470557" class="external-link" target="_blank">Zenodo</a> vom 14.09.2026.*

Vergessen Sie nicht eine TOC (Table of Contents = Inhaltsverzeichnis) in der Beschreibung hinzuzufügen. Diese ermöglicht einen schnellen Überblick über die Dateien und ist nicht nur bei großen Datenpaketen hilfreich.

5. **Eintrag prüfen und veröffentlichen:** Solange der Eintrag noch nicht veröffentlicht werden soll, kann er als Entwurf gespeichert werden. Prüfen Sie vor der Veröffentlichung, ob die Dateien korrekt hochgeladen und die Angaben vollständig sind. Anschließend kann der Eintrag veröffentlicht werden.

```{figure} /assets/zenodo_publish.png
---
align: center
width: 100%
---
Screenshot des Feldes zum Speichern des Entwurfs ("Save draft") und zum Veröffentlichen ("Publish").
```
*Quellenangabe: Screenshot des des Feldes zum Speichern des Entwurfs ("Save draft") und zum Veröffentlichen ("Publish") bei <a href="https://zenodo.org/records/19470557" class="external-link" target="_blank">Zenodo</a> vom 14.09.2026.*

Eine ausführliche Schritt-für-Schritt-Anleitung auf Englisch zum Upload von Forschungsdaten auf Zenodo finden Sie bei den <a href="https://onderzoektips.ugent.be/en/tips/00002267/" class="external-link" target="_blank">(Re)Search Tips</a> auf der Webseite der Universität Gent.

## Beispielszenario 

Im Beispielszenario der Publikation der Forschungsdaten aus dem Projekt Q-LCA fiel die Entscheidung auf das Repositorium <a href="https://zenodo.org/" class="external-link" target="_blank">Zenodo</a> - u. a. weil es kein fachspezifisches Repositorium gab (s. Unterkapitel 4.1 [Aufbewahrung](publikation:aufbewahrung)). Entsprechend der Leitlinie 17 der Guten wissenschaftlichen Praxis sollen Forschungsdaten an der Einrichtung, an der sie entstanden sind oder in "standortübergreifenden Repositorien" öffentlich zugänglich gemacht werden {cite}`deutsche_forschungsgemeinschaft_2025`.

Die veröffentlichten Daten finden Sie hier: https://zenodo.org/records/17866716 

- aus Cloud runterladen, alles durchgehen, ob alles richtig ist (Qualiprüfung); kontrollieren, ob alles geht (in diesem FAll gab es eine interaktive Tabelle und das Hin- und Herreichen der Tabelle führte zu Anzeigeproblemen (auch Mac/Windows-Problem) -> Prüfen, dass hochgeladene Version dem Original in seiner Interaktivität entspricht)
- auch alles andere prüfen: FD-Bericht, Struktur und Ordnung des Uploads etc.
- zudem: bei allen Dateien administrative Metadaten mitnehmen
- Publikation aus Sicherheitsgründen zudem in RADAR (Zweitveröffentlichung; institutionelles Repo)
- Paket benennen/beschreiben (Community Nachhaltige Quartiers- und Stadtentwicklung) -> mehrere Veröffentlichung, die zum Projekt gehören, mussten geordnet werden.

## Learnings

**Zenodo-Upload**
- Dummies angelegt, weil eine Datei im Entwurfsmodus eingestellt werden muss -> dann in Ruhe Metadaten ausgefüllt
- Achten Sie auf die Reihenfolge des Uploads und die Benennung der Dateien, da dies Auswirkungen auf die Anzeigereihenfolge hat.

---


In dem hier skizzierten Fall der nachträglichen Publikation von Forschungsdaten sind also folgende Aspekte zu beachten:
- Wenn man Daten publiziert, muss man vielleicht alles andere nochmal publizieren, weil man für alles eine DOI braucht (Problem der Gleichzeitigkeit, s. auch Abschnitt ? DMP in Kapitel 4 Datenmanagment [Link]).

*Die vom Projekt ausgemachten Qualitätskriterien zur Veröffentlichung sollten hier selbstverständlich Erwähnung finden:*

```{admonition} Zusätzliche Materialien
:class: seealso

- Sehr umfangreiche Zusammenstellung zum Thema Forschungsdaten publizieren auf der Informationsseite <a href="https://forschungsdaten.info/fdm-allgemein/veroeffentlichen-und-archivieren/daten-publizieren" class="external-link" target="_blank">forschungsdaten.info</a>
```

---

**Literatur**

```{bibliography}
:filter: docname in docnames
```
