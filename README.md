# SQL-BEECROWD
- ** EJERCICIO 2603 Customer Address **
```
solucion:
SELECT name, street
FROM customers
WHERE city = 'Porto Alegre';
```
- ** EJERCICIO 2607 Providers' City in Alphabetical Order **
```
Solucion:
SELECT DISTINCT (city)
FROM providers
ORDER BY city ASC;
```
- ** EJERCICIO 2608 Higher and Lower Price **
```
Solucion:
SELECT MAX(price), MIN(price)
FROM products;
```
- ** EJERCICIO 2615 Expanding the Business **
```
Solucion:
SELECT DISTINCT(city)
FROM customers;
```
- ** EJERCICIO 2617 Provider Ajax SA **
```
Solucion:
SELECT products.name, providers.name
FROM products
INNER JOIN providers ON
products.id_providers=providers.id
WHERE 
providers.name = 'Ajax SA';
```
