# Tag 1 – Einführung & Recap M162

## Inhalt
- [Grundlagen der Datenmodellierung](#grundlagen-der-datenmodellierung)
  - [Konzeptionelles Datenmodell (ERM)](#1-konzeptionelles-datenmodell-erm)
  - [Logisches Datenmodell (ERD)](#2-logisches-datenmodell-erd)
  - [Physisches Datenmodell](#3-physisches-datenmodell)
  - [Modellierung in der 3. Normalform (3NF)](#modellierung-in-der-3-normalform-3nf)


## Grundlagen der Datenmodellierung

- Ziel: Struktur von zu speichernden/verarbeitenden Daten definieren  
- Datenmodellierung ist eine Phase der Datenbankentwicklung  
- Drei aufeinander aufbauende Datenmodelle:

### 1. Konzeptionelles Datenmodell (ERM)
- Fachlich, unabhängig von Technik  
- Entwickelt aus Anforderungen  
- Entitäten und Beziehungen (1:c, c:mc, m:mc)

### 2. Logisches Datenmodell (ERD)
- Abbildung des ERM auf relationales Modell  
- Enthält Primär-/Fremdschlüssel und zusätzliche Attribute  
- Netzwerkbeziehungen über Transformationstabellen

### 3. Physisches Datenmodell
- Erweiterung des logischen Modells um technische Details  
- SQL-DDL-Befehle wie `CREATE TABLE`  
- Weitere Aspekte: Indizes, Partitionierung  
- Meist als SQL-Skript oder durch Tools generiert

### Modellierung in der 3. Normalform (3NF)
- Anwendung in operativen Systemen (z. B. ERP) und DWH  
- Daten werden anwendungsunabhängig und ohne Redundanz gespeichert  
- 3NF verhindert Anomalien und sichert Datenqualität durch Constraints
