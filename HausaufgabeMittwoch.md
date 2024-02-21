# REACT_EXPRESS_REPOS

**_Hausaufgaben Mittwoch, 21.02.2024_**

1. **Repository erstellt** (hier wurden jeweils die React-App sowie die Express-App eingefügt)

2. **Familiarisierung mit der React-App** ("/todo"-Seite) -> Funktionen wie "erledigt" & "löschen" betrachtet

3. **Erklärung der onClickDelete-Funktion:**
   Die onClickDelete Funktion wird aktiviert, wenn der Benutzer auf die Schaltfläche zum Löschen eines Todos klickt. Diese Funktion kommuniziert mit der Express-App, um das entsprechende Todo zu entfernen.
   In der React-App wird eine DELETE HTTP-Anfrage an die Route /api/todos/:id geschickt, wobei :id die einzigartige ID des zu löschenden Todos ist. Diese ID wird aus dem Todo-Objekt extrahiert, das der onClickDelete Funktion übergeben wird.

Im Backend, genauer gesagt in der Express-App, ist eine Route definiert, die auf DELETE /api/todos/:id reagiert. Der :id Parameter wird genutzt, um das richtige Todo in der Datenbank zu finden und zu löschen. Üblicherweise wird hierfür eine Datenbankabfrage (z. B. mit Mongoose in MongoDB) verwendet, um das Todo anhand seiner ID zu identifizieren und zu entfernen.

4. **Erklärung der onClickDone-Funktion:**
   Die onClickDone Funktion wird ausgelöst, wenn der Benutzer auf die Schaltfläche klickt, um ein Todo als "erledigt" zu markieren. Ähnlich wie bei onClickDelete kommuniziert diese Funktion mit der Express-App, um das Todo entsprechend zu aktualisieren.
   In der React-App wird eine PUT HTTP-Anfrage an die Route /api/todos/:id gesendet, wobei :id erneut die eindeutige ID des betreffenden Todos ist. Neben der ID wird ein Datenobjekt übergeben, das angibt, dass das Todo als "erledigt" markiert wurde.

Im Backend wird eine Route PUT /api/todos/:id definiert, um solche Anfragen zu verarbeiten. Die Express-App sucht das Todo mit der übergebenen ID und aktualisiert seinen Status entsprechend, üblicherweise in der Datenbank. Dies erfolgt durch eine Aktualisierungsanfrage (z. B. mit Mongoose in MongoDB), die das Todo anhand seiner ID identifiziert und den Status ändert.

=> **Beide Funktionen, onClickDelete und onClickDone, ermöglichen die Kommunikation zwischen der React- und der Express-App, um CRUD-Operationen (Create, Read, Update, Delete) auf der Todo-Liste durchzuführen.**
