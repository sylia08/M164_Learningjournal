# Tag4

## Inhalt
- [Beziehung mit Einschränkung (Constraint) erstellen](#beziehung-mit-einschränkung-constraint-erstellen)
- [Forward Engineering](#forward-engineering)

## Beziehung mit Einschränkung (Constraint) erstellen  
- Beziehungen in relationalen DBs sind durch Constraints an Fremdschlüsseln eingeschränkt  
- Mögliche Beziehungstypen und ihre Realisierbarkeit im physischen Modell:

| Beziehung MasterTab.links | DetailTab.rechts | möglich? | Erläuterung |
|---------------------------|------------------|----------|-------------|
| 1:1 (eins zu eins)         | 1:c, c:c         | 1:1 ➔ 1:c möglich; c:c nicht möglich | NN + UQ als Constraints |
| 1:mc (eins zu viele)       | c:mc             | 1:m ➔ 1:mc, c:m ➔ c:mc möglich       | NN als Constraint          |
| m:m (viele zu viele)       | -                | nur über Transformationstabelle      | 1:mc-[TT]-mc:1             |

- Gewisse Kundenwünsche können nicht direkt im RDBMS abgebildet werden, müssen in der Applikation umgesetzt werden  


## Forward Engineering  
- Erstellen der vier Beziehungstypen in MySQL Workbench  
- Setzen von NN (NOT NULL) und UQ (UNIQUE) Constraints am Fremdschlüssel  
- Erzeugen des DDL-SQL-Skripts zum Aufbau der Tabellen und Beziehungen  
- Rollenbezeichnungen können über Relationship Caption eingestellt werden  


