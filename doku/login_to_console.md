# In den Dockercontainer einloggen
```bash
docker exec -it db bash
```

Nach erfolgreichen Login, in die Konsole des Container:
Mongo-Shell im Container starten:

```bash
mongosh
```
Wenn alles geklappt hat könnte es so ähnlich wie hier aussehen:

```bash
root@929edc205fc6:/# mongosh
Current Mongosh Log ID: 61f9bc9025c23e78a0241c3a
Connecting to:          mongodb://127.0.0.1:27017/?directConnection=true&serverSelectionTimeoutMS=2000&appName=mongosh+1.1.9
Using MongoDB:          5.0.6
Using Mongosh:          1.1.9

For mongosh info see: https://docs.mongodb.com/mongodb-shell/


To help improve our products, anonymous usage data is collected and sent to MongoDB periodically (https://www.mongodb.com/legal/privacy-policy).
You can opt-out by running the disableTelemetry() command.

test>
```

Mongo-Shell verlassen mit:
```bash
exit
```

Um mit der MongoDB richtig arbeiten zu können, muss man sich wie folgt Authentifizieren ...
```bash
mongosh "mongodb://localhost:27017" --username root --authenticationDatabase admin
```
... und im Anschluss das passwort eingaben (im Projektbeispiel immernoch: example)
```bash
root@929edc205fc6:/# mongosh "mongodb://localhost:27017" --username root --authenticationDatabase admin
Enter password: *******
Current Mongosh Log ID: 61f9c5d1ae07d35aa700c055
Connecting to:          mongodb://localhost:27017/?directConnection=true&serverSelectionTimeoutMS=2000&appName=mongosh+1.1.9
Using MongoDB:          5.0.6
Using Mongosh:          1.1.9

For mongosh info see: https://docs.mongodb.com/mongodb-shell/

```



