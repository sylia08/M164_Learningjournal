# Tag 5: Löschen in professionellen Datenbanken  

## Datenintegrität (4 Integritätsregeln)

* **Entitätsintegrität:** Jeder Datensatz eindeutig identifizierbar und dauerhaft, keine Duplikate oder ungewollte Änderungen.
* **Referenzielle Integrität:** Beziehungen zwischen Tabellen bleiben konsistent (z. B. Fremdschlüssel beziehen sich nur auf existierende Primärschlüssel).
* **Bereichswertintegrität (Datentypen):** Daten müssen im korrekten Datentyp gespeichert werden (z.B. Telefonnummer als String, nicht Integer).
* **Benutzerdefinierte Integrität (Datenbeschränkungen):** Daten müssen gültig sein, z.B. nur positive Zahlen oder korrekt formatierte E-Mail-Adressen.



## Löschen in professionellen Datenbanken

* **Löschen (DELETE) ist in professionellen Systemen oft tabu, weil dadurch wichtige Informationen verloren gehen.**
* Beispiel: Mitarbeiterdatensätze sollten nicht gelöscht werden, da sonst alle Aktivitäten dieses Mitarbeiters verloren sind (z.B. aus juristischen Gründen). Stattdessen wird der Mitarbeiter als inaktiv markiert oder mit Austrittsdatum versehen.
* Zeitliche Abläufe werden nicht durch Überschreiben abgebildet, sondern durch zusätzliche Tabellen zur Historisierung.
* Beispiel Kassensystem: Löschen von Einkaufsdaten ist problematisch; stattdessen Stornierungen verwenden.
* Referentielle Integrität verhindert Löschvorgänge, wenn abhängige Datensätze existieren (Fremdschlüssel-Constraints).
* Beispiel Wikipedia: Benutzernamen werden nicht gelöscht, sondern nur gesperrt, um Historie zu erhalten.



## Fremdschlüssel-Regeln beim Löschen (ON DELETE Optionen)

| Regel                    | Bedeutung                                                                                                                                       |
| ------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **NO ACTION** (Standard) | Löschen in Primärtabelle nur möglich, wenn kein Fremdschlüssel in Detailtabelle existiert. Überprüfung am Ende der Transaktion.                 |
| **RESTRICT**             | Wie NO ACTION, aber Prüfung direkt nach jedem Befehl.                                                                                           |
| **CASCADE**              | Löschen in Primärtabelle löscht auch alle abhängigen Datensätze in der Fremdschlüsseltabelle. Achtung: kann zu ungewolltem Datenverlust führen! |
| **SET NULL**             | Beim Löschen werden Fremdschlüssel in abhängigen Tabellen auf NULL gesetzt (nur möglich, wenn FK NULL erlaubt ist).                             |

* ON UPDATE-Regeln relevant, wenn Primärschlüssel geändert werden, sind hier meist irrelevant (Auto Increment IDs ändern sich nicht).



## SQL Basics: SELECT ALIAS

* Aliase sind temporäre Namen für Spalten oder Tabellen in einer Abfrage.
* Spaltenalias existiert nur während der Abfrage.
* Tabellenalias wird in der ganzen Abfrage verwendet (z.B. `p` statt `person`).



## Aggregatsfunktionen

* **COUNT:** Anzahl der Zeilen (oder nicht-NULL Werte einer Spalte)
* **SUM:** Summe von Zahlenwerten
* **AVG:** Durchschnitt von Zahlenwerten
* **MIN:** Kleinster Wert
* **MAX:** Größter Wert

Beispiel:

```sql
SELECT COUNT(*) FROM customers;
SELECT SUM(salary) FROM employees;
```



## GROUP BY

* Gruppiert Zeilen mit gleichen Werten in einer oder mehreren Spalten.
* Wird oft mit Aggregatsfunktionen kombiniert, um Gruppenergebnisse zu berechnen.
* Beispiel: Gesamtbestellwert pro Kunde

```sql
SELECT customer_id, SUM(order_total)
FROM orders
GROUP BY customer_id;
```



## HAVING Condition

* Filtert Ergebnisse nach einer Gruppierung, basierend auf Aggregatfunktionen.
* Im Gegensatz zu WHERE wird HAVING auf Gruppenergebnisse angewandt.
* Beispiel: Nur Kunden mit Bestellsumme > 500

```sql
SELECT customer_id, SUM(order_total)
FROM orders
GROUP BY customer_id
HAVING SUM(order_total) > 500;
```


## Checkpoint Fragen (ohne Lösungen)

* Nenne die vier Aspekte der Datenintegrität in einer Datenbank.
* Was ist der Unterschied zwischen Datenintegrität und Datenkonsistenz?
* Was ist die Gefahr bei der FK-Constraint-Option ON DELETE CASCADE?
* Was ist der Unterschied zwischen COUNT(\*) und COUNT(attr)?
* Formuliere einen SELECT-Befehl mit der WHERE BETWEEN Klausel.
* Worauf müssen Sie bei der HAVING Klausel achten?


