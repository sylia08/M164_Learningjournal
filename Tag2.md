# Tag 2
## Inhalt
- [ Generalisierung Spezialisierung](#generalisierung-spezialisierung)
- [ Beziehungsarten in Datenbanken](#beziehungsarten-in-datenbanken)
- [DBMS](#dbms)
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

## DBS
Ein DBS dient der elektronischen Verwaltung grosser Datenmengen. Es speichert Daten effizient, widerspruchsfrei und dauerhaft und stellt benötigte Informationen in nutzergerechter Form dar.
Bestandteile eines DBS:
- DBMS (Datenbankmanagementsystem): Software zur Organisation, Zugriffskontrolle und Abfrage.
- DB (Datenbank): Die zu verwaltenden Daten.
  
Datenbanksysteme gibt es in verschiedenen Formen. Die Art und Weise, wie ein solches System Daten speichert und verwaltet, wird durch das Datenbankmodell festgelegt. Die bekannteste Form eines Datenbanksystems ist das Relationale Datenbanksystem.
<img width="592" alt="image" src="https://github.com/user-attachments/assets/e4e70afc-6822-48b2-ac9e-9ae81337cc3a"/>

## DBMS
