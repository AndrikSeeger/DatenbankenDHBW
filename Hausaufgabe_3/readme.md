# 3. Hausaufgabe

## A)

```MySQL
USE uebungSchule;

SELECT * FROM schueler sch, smartphones phones WHERE sch.idSmartphones = phones.id
AND phones.marke = 'Apple'
```

## B1)

```MySQL
USE uebungSchule;

SELECT sch.name AS Schuelername, lr.name AS Lehrername
FROM lehrer_hat_schueler lhs, schueler sch, lehrer lr
WHERE lr.id = lhs.idLehrer
  AND lhs.idSchueler = sch.id
```

## B2)

```MySQL
USE uebungSchule;

SELECT sch.name AS Schuelername, o.name AS Schuelerwohnort
FROM lehrer_hat_schueler lhs, schueler sch, lehrer lr, orte o
WHERE lr.name = 'Maier'
  AND lr.id = lhs.idLehrer
  AND lhs.idSchueler = sch.id
  AND o.id = sch.idOrte;
 ```

## C)

```MySQL
USE uebungSchule;

SELECT sch.name AS Schuelername, o.name AS Wohnort, sm.marke AS Smartphonemarke
FROM schueler sch, orte o, smartphones sm
WHERE o.name = 'Emmendingen'
  AND o.id = sch.idOrte
  AND sm.id = sch.idSmartphones;
```
 
## D)

```MySQL
USE uebungSchule;

SELECT sch.name AS Schuelername, o.name AS Wohnort, lr.name AS Lehrername
FROM schueler sch, orte o, smartphones sm, lehrer lr, lehrer_hat_schueler lhs
WHERE o.name = 'Emmendingen'
  AND lr.name = 'Huber'
  AND sch.id = lhs.idSchueler
  AND lr.id = lhs.idLehrer
  AND o.id = sch.idOrte;
```
## Contributing
[Andrik Seeger](https://github.com/AndrikSeeger) 
