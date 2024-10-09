# BayWa Coding Task Backend

## Aufgabe

Entwickle einen REST-API-Endpoint für eine "Task"-Entität mit den folgenden Eigenschaften: id, title, description, status, und createdAt. Der Endpoint soll die vollständigen CRUD-Operationen (Create, Read, Update, Delete) unterstützen. Alternativ kannst du eine eigene Entität mit fünf Eigenschaften wählen.

## Ziel

Der Endpoint soll alle CRUD-Operationen für die gewählte Entität erfolgreich ausführen. Eine funktionierende Datenvalidierung ist erforderlich, und einfache Unit-Tests müssen implementiert werden. Die Aufgabe ist erfolgreich abgeschlossen, wenn die CRUD-Funktionalität vollständig ist, die Validierung korrekt funktioniert, und die Unit-Tests bestehen.

### Prüfkriterien

- Die CRUD-Operationen sind korrekt implementiert und funktionieren wie erwartet.
- Eingabedaten werden mithilfe von class-validator überprüft.
- Der Code enthält mindestens einen Unit-Test pro CRUD-Operation, die erfolgreich durchlaufen.


## Implementierungsschritte

1. Ressourcenwahl:    

- Wähle eine einfache Ressource, wie z.B. Task, Note oder User.
- Definiere, welche Felder die Ressource haben soll (z.B. id, title, description, createdAt für eine Task-Ressource).

2. Modulerstellung:
  
- Erstelle ein neues Modul für die Ressource (nest g module tasks).

3. Service und Controller anlegen:

- Erstelle einen Service und Controller für die Ressource (nest g service tasks und nest g controller tasks).
- Im Controller implementiere die grundlegenden CRUD-Endpunkte:
  -  GET /tasks: Gibt alle Aufgaben zurück.
  -  GET /tasks/:id: Gibt eine Aufgabe anhand der ID zurück.
  -  POST /tasks: Fügt eine neue Aufgabe hinzu.
  -  PUT /tasks/:id: Aktualisiert eine bestehende Aufgabe.
  -  DELETE /tasks/:id: Löscht eine Aufgabe.
 
4. Datenmodell und Validierung:

- Definiere ein DTO (Data Transfer Object) für die Ressource, z.B. CreateTaskDto und UpdateTaskDto.
- Verwende class-validator, um sicherzustellen, dass die Eingabedaten korrekt sind (z.B. @IsString(), @IsNotEmpty()).

5. Implementierung der Logik im Service:

- Implementiere die Logik für die CRUD-Operationen im TasksService.
- Nutze eine einfache In-Memory-Datenstruktur (z.B. ein Array), um die Daten temporär zu speichern.

6. Testing und Auswertung:

- Teste die Endpoints mit einem Tool wie Postman oder Swagger
- Besprecht anschließend:
  - Wie die Module und Abhängigkeiten aufgebaut sind.
  - Welche zusätzlichen Features möglich wären (z.B. Authentifizierung).
  - Optimierungsmöglichkeiten für größere Datenmengen oder Datenbanken.
