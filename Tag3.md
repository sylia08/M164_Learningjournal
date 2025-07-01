# Tag 3
## Inhalt
- [Mehrfachbeziehungen](#mehrfachbeziehungen)  
- [Rekursion (strenge Hierarchie)](#rekursion-strenge-hierarchie)  
- [Einfache Hierarchie (mit Zwischentabelle)](#einfache-hierarchie-mit-zwischentabelle)  
- [Stücklistenproblem](#stücklistenproblem)  
---

## Mehrfachbeziehungen  
Erklärung, Rollenbezeichnungen, Kardinalitäten, Transformationstabellen bei m:n-Beziehungen  

## Rekursion (strenge Hierarchie)  
Beziehung eines Entitätstyps zu sich selbst, Fremdschlüssel auf eigene Tabelle, c:mc-Beziehung  

## Einfache Hierarchie (mit Zwischentabelle)  
Netzwerkstrukturen mit mehreren Vorgesetzten, m:n-Beziehung, Transformationstabelle mit Rollen  

## Stücklistenproblem  
Rekursive Produkt-Zusammensetzungen, Aggregat-Komponenten-Beziehungen, Lösung mit Zusatztabellen  

---

## Praktische Umsetzung im Tourenplaner  
- Aufbau des Schemas mit Mehrfachbeziehungen und Hierarchien  
- Erstellung der Datenbank mit Forward Engineering  
- Daten einfügen (Mitarbeiter, Touren)  
- Hierarchische Beziehungen pflegen (SQL UPDATE mit Fremdschlüsseln)  
- Tourendaten und Mehrfachbeziehungen mit JOIN abfragen  

---

## Datenbearbeitung (DML)  
- INSERT, UPDATE, DELETE, ALTER, DROP Befehle  
- Beispiele und Übungen  

## Datenabfrage mit SELECT (DQL)  
- Syntax und Beispiele  
- Funktionen (ROUND, IF, mathematische Funktionen)  
- JOINs zum Verbinden mehrerer Tabellen  

---

## Hierarchien und Mehrfachbeziehungen einpflegen  
- Beispiel Hierarchie-Tabelle mit Chef-Mitarbeiter Beziehungen  
- Beispiel Mehrfachbeziehungen zwischen Fahrten und Orten  
- Testen der Datenintegrität mit SELECT-Queries  

