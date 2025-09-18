# IntelligentPDF - Der intelligente Posteingang
Das Tool um lästigen Papierkram zu beseitigen und der Digitlisierung und einem Workflow endlich näher zu kommen.


## Beschreibung
Dieses Projekt ist ein „intelligenter Posteingang“ für Dokumente. Eingehende Dateien (z. B. aus einem Scanner-Ordner oder manuell hochgeladen) werden vom Backend an einen Klassifizierungs-Mock übergeben, der Metadaten und einen Confidence-Wert liefert. Abhängig vom Schwellenwert werden Dokumente automatisch verarbeitet oder landen in einer Review-Maske, in der Metadaten korrigiert, Confidence-Overrides gesetzt und die Verarbeitung manuell angestoßen werden können. Statuswechsel und Aktionen werden nachvollziehbar protokolliert; Re-Klassifizieren und Aufräumregeln (Löschen/Archivieren) sind integriert. Ziel ist ein schlanker, nachvollziehbarer End-to-End-Flow vom Eingang bis zur Verarbeitung.



## Ausführen des Programms
### Linux / Windows
**Diese Beschreibung ist anzuwenden in einem Bash-Terminal**

Laden sie sich das Git-Repo herunter
```
$ git clone https://github.com/aliosman6161/intelligentPDF.git
```

Navigieren sie zu den Ordner und öffnen sie den die login.html in einem Browser ihrer Wahl.
```
$ cd intelligentPDF/src/client
$ firefox login.html
```

Starte nun den Docker und den den indes.js über node in seperaten Terminal

```
$ node intelligentPDF/src/server/index.js
$ cd intelligentPDF/pdfclassifier-api-mock-1_1_0
$ docker-compose up --build
```

