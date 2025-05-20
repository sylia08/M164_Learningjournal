# Tag 2

## Generalisierung / Spezialisierung
Die Datenbankmodellierung basiert auf Attributen, die Entitätstypen zugeordnet werden. 
Problematisch wird es, wenn mehrere Entitätstypen gemeinsame Attribute haben, was zu Redundanz führen kann (z. B. Mitarbeiter, die auch Kunden sind).
Um das zu vermeiden, fasst man gemeinsame Attribute in einem allgemeinen Entitätstyp zusammen (Generalisierung), während spezielle Attribute in den jeweiligen Entitätstypen bleiben (Spezialisierung).
Die spezialisierten Tabellen verweisen per Fremdschlüssel auf die generalisierte Tabelle („is_a“-Beziehung). Dieses Prinzip ist Vererbung in der objektorientierten Modellierung.

<img width="592" alt="image" src="https://github.com/user-attachments/assets/a57d5128-3b6e-4316-b252-26e98f35ab6a" />
<img width="592" alt="image" src="https://github.com/user-attachments/assets/26a22c0c-5ee5-4808-a419-7c5f334149d1" />

