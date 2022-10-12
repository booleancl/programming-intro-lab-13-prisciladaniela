## Repaso SQL

SQL, es un lenguaje de programación para bases de datos.Su traducción literal sería Lenguaje Estructurado De Consultas(Structured Query Language)

SQL, es un lenguaje insensible a mayúsculas y minúsculas. "select" == SELECT.

En sql las tablas tienen columnas que tendrán información de cierto **tipo**

Como buena práctica los nommbres de las tablas deben ser en **plural**

Llave primaria: con valor único y no nulo.

CSV: Es un formato de archivo muy popular en los negocios. A partir de Excel se pueden exportar datos en CSV y también importar. "Valores separados por coma"

```SQL
SELECT <column>
FROM<table>;
```

La sentencia **WHERE** es para filtrar información 

```SQL
SELECT <column>
FROM<table>
WHERE <column><condition>;
```
```sql
 SELECT * 
 FROM cities
 WHERE area < 1100
 AND country = 'Japan';
```
 
### Ejemplo usando **OR**

```sql
 SELECT name,country,area
 FROM cities
 WHERE area < 1100
 OR country = 'Japan';
```


### Ejemplo ordenando los resultados de forma ascendente


```sql 
SELECT name,country,area
FROM cities
ORDER BY area;
```
### Ejemplo con WHERE, OR y ORDER

```sql
 SELECT name,country,area
 FROM cities
 WHERE area < 1100
 OR country = 'Japan';
 ORDER BY area
```


### Ejemplo descendente
```sql
 SELECT name,country,area
 FROM cities
 WHERE area < 1100
 OR country = 'Japan'
 ORDER BY area DESC;
 ```


>Nota: Distinto puede ser <> ! 

### Campos calculados con AS (como)

```sql
SELECT name,population/area AS density
FROM cities 
ORDER BY density DESC;
```


### Contando elementos con COUNT

```sql
SELECT COUNT(name)
FROM cities
WHERE country = 'India';
```


###  Limitar los resultados con **Limit**

```sql
SELECT name,population/area AS density
FROM cities
ORDER BY density DESC
LIMIT 2;
```