# Lernjournal M164 – Asani AP24b

## Inhaltsverzeichnis

- [Einführung: SQL](#einführung-sql)
- [Tag 1 – Modellierung](#tag-1--modellierung)
- [Tag 2 – Generalisierung und DBMS](#tag-2--generalisierung-und-dbms)
- [Tag 3 – Datentypen & Hierarchien](#tag-3--datentypen--hierarchien)
- [Tag 4 – Beziehungen & Constraints](#tag-4--beziehungen--constraints)
- [Tag 5 – Datenintegrität & Aggregatsfunktionen](#tag-5--datenintegrität--aggregatsfunktionen)
- [Tag 6 – Subqueries & CSV-Import](#tag-6--subqueries--csv-import)
- [Tag 7 – Backup & Daten einbinden](#tag-7--backup--daten-einbinden)
- [Tag 8 – Datenbereinigung & Opendata](#tag-8--datenbereinigung--opendata)

---

## Einführung: SQL

**SQL (Structured Query Language)** ist eine Sprache, mit der man Daten in relationalen Datenbanken abfragen, ändern und verwalten kann. Sie besteht aus verschiedenen Teilen wie DDL (Strukturen), DML (Daten), DQL (Abfragen) und DCL (Rechte).

SQL wurde 1974 bei IBM entwickelt. 1986 wurde es offizieller ANSI-Standard. Es wird bis heute in fast allen Datenbanksystemen eingesetzt.

---

## Tag 1 – Modellierung

### Thema
Ein Busunternehmen modellieren mit ERD.

### Umsetzung
- Entitäten: Fahrt, Station, Ort, Fahrer, Disponent, Fahrzeug
- Beziehungen und Regeln erkannt

### Erkenntnisse
- Ich kann Anforderungen in ein Datenmodell überführen  
- Ich kenne die Schritte bis zur 3. Normalform

---

## Tag 2 – Generalisierung und DBMS

### Thema
Vererbung im Datenmodell, Identifying-Beziehungen, DBMS-Funktionen, DDL-Befehle.

### Umsetzung
- Oberklasse `Person`, Unterklassen `Fahrer`, `Disponent`
- Identifying vs. Non-Identifying erklärt
- DBMS-Aufgaben kennengelernt
- Tabellen mit SQL erstellt und angepasst
- Forward Engineering geübt

### Erkenntnisse
- Generalisierung spart Wiederholungen  
- Ich kann Modelle logisch aufbauen und als SQL generieren

---

## Tag 3 – Datentypen und Hierarchien

### Thema
Datentypen, rekursive Beziehungen, mc:mc-Beziehungen, Daten einfügen und abfragen.

### Umsetzung
- Datentypen und Formate zugeordnet
- Hierarchie mit rekursiver Tabelle modelliert
- Komplexe Tourenbeziehungen abgebildet
- `INSERT`, `UPDATE`, `SELECT` mit `JOIN` geübt

### Erkenntnisse
- Ich kann Hierarchien per SQL abfragen  
- Ich kenne sinnvolle Einsatzbereiche für Transformationstabellen

---

## Tag 4 – Beziehungen und Constraints

### Thema
Beziehungen in SQL mit Einschränkungen, Forward Engineering mit verschiedenen Typen, Mengenlehre.

### Umsetzung
- Beziehungstypen (1:1, 1:mc, mc:mc) technisch umgesetzt
- `NOT NULL`, `UNIQUE`, `FOREIGN KEY` gesetzt
- `ALTER TABLE` mit `ADD CONSTRAINT` geübt

### Erkenntnisse
- Ich kann Tabellenbeziehungen mit Regeln absichern  
- Ich kenne den praktischen Einsatz von Constraints

---

## Tag 5 – Datenintegrität und Aggregatsfunktionen

### Thema
Daten schützen, korrekt löschen, FK-Regeln, Aliase, Gruppenabfragen mit `GROUP BY` und `HAVING`.

### Umsetzung
- Löschen durch "deaktivieren" statt `DELETE`
- Integritätsregeln: Entität, Referenz, Bereich, Benutzerdefiniert
- FK-Regeln: `RESTRICT`, `CASCADE`, `SET NULL`
- `COUNT`, `SUM`, `AVG` kombiniert mit Gruppierung

### Erkenntnisse
- Ich kenne Alternativen zum Löschen  
- Ich kann Gruppen gezielt abfragen und filtern

---

## Tag 6 – Subqueries und CSV-Import

### Thema
Unterabfragen, Datenimport mit `LOAD DATA INFILE`, Daten in 3NF aufteilen.

### Umsetzung
- Subqueries mit `IN`, `EXISTS`, Skalare und Nicht-Skalare
- CSV-Dateien importiert und bereinigt
- Tabellen zerlegt in `Person`, `Ort`, `Strasse`
- Daten mit `INSERT SELECT` verteilt

### Erkenntnisse
- Ich kann Daten aus einer Tabelle auf mehrere normalisierte aufteilen  
- Ich kann gezielt externe Daten importieren

---

## Tag 7 – Backup und Daten einbinden

### Thema
Backup-Arten und -Tools, Freifächer-DB importieren und prüfen.

### Umsetzung
- Backup-Strategien: Voll, Differenziell, Inkrementell
- Tools: mysqldump, phpMyAdmin, HeidiSQL usw.
- Backup-User mit `GRANT` erstellt
- Freifächer-Excel bereinigt, importiert, geprüft
- Abfragen erstellt, Ergebnisse exportiert (`OUTFILE`)

### Erkenntnisse
- Ich kenne Tools und Arten von Backups  
- Ich kann eine strukturierte DB mit echten Daten füllen

---

## Tag 8 – Datenbereinigung und Opendata

### Thema
Weitere Arbeit an Freifächer-DB, Opendata-Daten importieren und analysieren.

### Umsetzung
- 290 Schüler generiert und importiert
- Freifächer-Abfragen mit `JOIN`, `IN`, `GROUP BY`
- Opendata von Stadt Zürich analysiert (Quartierdaten)
- Daten bereinigt, importiert, gruppiert und ausgewertet

### Erkenntnisse
- Ich kann Opendata-Daten in einer eigenen DB verarbeiten  
- Ich kann komplexe Analysen mit SQL ausführen
