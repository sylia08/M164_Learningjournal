# Tag 2
## Inhalt
- [Generalisierung & Spezialisierung](#generalisierung-spezialisierung)
- [Beziehungsarten in Datenbanken](#beziehungsarten-in-datenbanken)
  - [Identifying Relationships](#identifying-relationships)
  - [Non-Identifying Relationships](#non-identifying-relationships)
- [DBMS (Datenbankmanagementsysteme)](#dbms)
  - [Aufgaben und Merkmale eines DBMS](#aufgaben-und-merkmale-eines-dbms)
  - [Vorteile eines DBS](#vorteile-eines-dbs)
  - [Nachteile eines DBS](#nachteile-eines-dbs)
  - [Produkte](#produkte)
## Generalisierung Spezialisierung 
Die Datenbankmodellierung basiert auf Attributen, die Entitätstypen zugeordnet werden. 
Problematisch wird es, wenn mehrere Entitätstypen gemeinsame Attribute haben, was zu Redundanz führen kann (z. B. Mitarbeiter, die auch Kunden sind).
Um das zu vermeiden, fasst man gemeinsame Attribute in einem allgemeinen Entitätstyp zusammen (Generalisierung), während spezielle Attribute in den jeweiligen Entitätstypen bleiben (Spezialisierung).
Die spezialisierten Tabellen verweisen per Fremdschlüssel auf die generalisierte Tabelle („is_a“-Beziehung). Dieses Prinzip ist Vererbung in der objektorientierten Modellierung.

<img width="592" alt="image" src="https://github.com/user-attachments/assets/a57d5128-3b6e-4316-b252-26e98f35ab6a" />
<img width="592" alt="image" src="https://github.com/user-attachments/assets/26a22c0c-5ee5-4808-a419-7c5f334149d1" />

## Beziehungsarten in Datenbanken:
In Datenbanken gibt es verschiedene Arten von Beziehungen zwischen Tabellen, insbesondere zwischen einer Parent-Tabelle (Eltern/Master) und einer Child-Tabelle (Kind/Detail). Die Art der Beziehung wird vor allem durch die Rolle des Fremdschlüssels (Foreign Key) im Primärschlüssel (Primary Key) der Child-Tabelle bestimmt.
### Identifying Relationships
Der Foreign Key ein Teil des Primary Keys der Child-Tabelle und identifiziert somit eine eindeuitige verbindung.
Eigenschaften:
- Die ID besteht aus mehreren Attributen (min.2 Attribute).
- Die Zugehörigkeit kann nicht einfach geändert werden, da sie Teil der Identität ist.
- Die Beziehung ist eindeutig und spezifisch: nur eine verbindung zur  Parent-Tabelle.
-  Wird im Diagramm mit _______ verbindungen erkannt
 <img width="592" alt="image" src="https://github.com/user-attachments/assets/dd29b2bb-2a27-499a-af7a-bbde31cea73c" />
 
### Non-Identifying Relationships
Der Fremdschlüssel ist kein Teil des Primärschlüssels der Child-Tabelle.
Bedeutung:
Die Foreign Key der Child-Tabelle ist unabhängig von der Parent-Tabelle. Die Beziehung ist flexibler und weniger strikt.
Eigenschaften:
- Die Beziehung ist allgemeiner und vager.
- Der Fremdschlüssel kann beliebig geändert werden, ohne dass die Foreign Key der Child-Tabelle verloren geht.
- Wird im Diagramm mit ----- verbindungen erkannt
<img width="592" alt="image" src="https://github.com/user-attachments/assets/6376a314-def1-4fb4-90d8-1db41876c92b" />

## DBMS
Ein Datenbanksystem (DBS) dient der elektronischen Verwaltung grosser Datenmengen. Es besteht aus:
- dem Datenbankmanagementsystem (DBMS): Software zur Organisation, Speicherung, Abfrage und Kontrolle von Datenzugriffen.
- der Datenbank (DB): Sammlung der zu verwaltenden Daten.

### Aufgaben und Merkmale eines DBMS:
Integrierte Datenhaltung: Einheitliche, redundanzarme Speicherung mit effizienter Verknüpfung komplexer Datenbeziehungen.

Datenbanksprache:
- DQL/DRL: Datenabfragen (z. B. SELECT)
- DDL: Definition von Datenstrukturen (z. B. CREATE)
- DML: Datenmanipulation (z. B. INSERT)
- DCL: Rechtevergabe (z. B. GRANT)
- TCL: Transaktionssteuerung (z. B. COMMIT)

**Benutzeroberflächen:** Unterschiedliche Interfaces (z. B. GUI, Webzugriff, API) für verschiedene Nutzergruppen.

**Katalog (Data Dictionary):** Enthält Metadaten zur Beschreibung der Datenstruktur.

**Benutzersichten (Views):** Angepasste Ausschnitte des Datenbestands für unterschiedliche Nutzer.

**Konsistenzkontrolle:** Wahrung der Datenintegrität durch Regeln (Constraints) und Sicherstellung der Speicherintegrität.

**Zugriffskontrolle:** Schutz vor unautorisierten Zugriffen.

**Transaktionen:** Änderungen werden atomar und dauerhaft ausgeführt.

**Mehrbenutzerfähigkeit:** Gleichzeitiger Zugriff durch mehrere Nutzer ohne Konflikte (Isolation).

**Datensicherung (Recovery):** Wiederherstellung der Daten nach Fehlern.

### Vorteile eines DBS:
- Standardisierung der Datenorganisation.
- Effizienter Datenzugriff durch spezialisierte Speichertechniken.
- Schnellere Anwendungsentwicklung dank integrierter Funktionen.
- Flexibilität durch Datenunabhängigkeit.
- Hohe Verfügbarkeit durch gleichzeitigen Zugriff und Transaktionskontrolle.
- Wirtschaftlichkeit durch zentrale Datenhaltung und Ressourcennutzung.

### Nachteile eines DBS:
- Hohe Anfangskosten (Software, Hardware, Personal).
- Geringere Effizienz bei spezialisierten Anwendungen.
- Komplexe Anforderungen an Sicherheit, Synchronisation, Personal.
- Zentralisierung als Risiko (Ausfallgefahr, Lösung: Verteilung).
- Einsatz traditioneller Dateisysteme sinnvoll bei:
- Kein Mehrbenutzerzugriff.
- Feste Echtzeitanforderungen.
- Statische, einfache Daten ohne Änderungsbedarf.
  
### Produkte
| **Hersteller** | **Produkt**                       | **Modell/Charakteristik**          |
| -------------- | --------------------------------- | ---------------------------------- |
| Software AG    | Adabas                            | NF²-Modell (nicht normalisiert)    |
| InterSystems   | Cache                             | hierarchisch, postrelational       |
| IBM            | DB2, IMS, Informix                | objektrelational bzw. hierarchisch |
| Microsoft      | Access, SQL Server, Visual FoxPro | relational/objektrelational        |
| Oracle         | Oracle                            | objektrelational                   |
| MySQL AB       | MySQL                             | relational                         |
| PostgreSQL     | PostgreSQL                        | objektrelational                   |
| Sybase         | Sybase ASE                        | relational                         |
| Versant        | Versant                           | objektorientiert                   |
| NCR Teradata   | Teradata                          | relationales Hochleistungs-DBMS    |

