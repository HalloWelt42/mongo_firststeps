# Erste Gehversuche mit Mongo

Eingabe
```bash
test> show dbs
```
Ergebnis
```bash
admin      102 kB
config    73.7 kB
local     73.7 kB
```
## Temporär zu einer DB wechseln
Temporär, weil die Datenbank noch nicht wirklich exsistiert.

Eingabe
```bash
test> use tutorial
```
Ergebnis
```bash
switched to db tutorial
```
## Datenbank löschen
Eingabe
```bash
tutorial> db.dropDatabase('tutorial')
```
Ergebnis
```bash
{ ok: 1, dropped: 'tutorial' }
```

## Collection anlegen
**Collection** kann man hier kategorisch vergleichen wie bei relationalen Datenbanken **Tabellen**.
Eine Datenbank enthält ein oder mehrere Collections.

Eingabe
```bash
tutorial> db.createCollection('products')
```
Ergebnis
```bash
{ ok: 1 }
```
jetzt wurde die Collection mit dem Namen 'products' angelegt