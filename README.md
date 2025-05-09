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
- ** EJERCICIO 2622 Legal Person **
```
Solucion:
SELECT c.name
FROM customers c
INNER JOIN
legal_person lp
ON
c.id = lp.id_customers;
```
- ** EJERCICIO 2744 Passwords **
```
Solucion:
SELECT id, password, MD5(password)
FROM account;
```
- ** EJERCICIO 2746 Viruses **
```
Solucion:
SELECT REPLACE(name, 'H1', 'X') AS name
FROM virus;
```
- ** EJERCICIO 2604 Under 10 or Greater Than 100 **
```
Solucion:
SELECT id, name
FROM products
WHERE price < 10 OR price > 100;
```
- ** EJERCICIO 2613 Cheap Movies **
```
Solucion:
SELECT m.id, m.name
FROM movies m
INNER JOIN
prices p
ON
m.id_prices = p.id
WHERE
p.value < 2;
```
- ** EJERCICIO 2619 Super Luxury **
```
Solucion:
SELECT p.name, pr.name, p.price
FROM products p
INNER JOIN
providers pr
ON
p.id_providers = pr.id
INNER JOIN 
categories c
ON
p.id_categories = c.id
WHERE
p.price > 1000 AND c.name='Super Luxury';
```
- ** EJERCICIO 2994 How much does a Doctor earn? **
```
Solucion:
SELECT d.name, ROUND( SUM(a.hours*150+a.hours*150*(w.bonus/100)),1) AS salary
FROM 
doctors d
INNER JOIN 
attendances a
ON 
d.id = a.id_doctor
INNER JOIN 
work_shifts w
ON
a.id_work_shift = w.id
GROUP BY d.id
ORDER BY salary DESC;
```
![image](https://github.com/user-attachments/assets/b872d607-e81c-4ef4-b473-8744eb9e6284)
- ** EJERCICIO 2618 Imported Products **
```
Solucion:
SELECT p.name, pr.name, c.name
FROM
products p
INNER JOIN
providers pr
ON
p.id_providers = pr.id
INNER JOIN
categories c
ON
p.id_categories = c.id
WHERE 
pr.name = 'Sansul SA' AND c.name = 'Imported';
```
![image](https://github.com/user-attachments/assets/4b62bf0c-861e-46b9-9e44-a2c5348b7736)
- ** EJERCICIO 2620 Orders in First Half **
```
Solucion:
SELECT
c.name, o.id
FROM
customers c
INNER JOIN
orders o
ON
c.id=o.id_customers 
WHERE 
EXTRACT(MONTH FROM o.orders_date)<=6;
```
![image](https://github.com/user-attachments/assets/8c631907-09dd-481f-a4fc-e8108d3176bd)
- ** EJERCICIO 2621 Amounts Between 10 and 20 **
```
Solucion:
SELECT 
pr.name
FROM
providers p
INNER JOIN
products pr
ON 
p.id = pr.id_providers
WHERE
(pr.amount>=10 AND pr.amount<=20) AND
p.name LIKE 'P%';
```
![image](https://github.com/user-attachments/assets/6bc5be02-9632-4b1c-9e8a-a1ab56054a8f)
- ** EJERCICIO 2624 Number of Cities per Customers **
```
Solucion:
SELECT COUNT(DISTINCT(city))
FROM customers;
```
![image](https://github.com/user-attachments/assets/acd83124-e8e5-4cfa-a4df-b0d75386d053)
- ** EJERCICIO 2743 Number of Characters **
```
Solucion:
SELECT name, LENGTH(name)
FROM
people
ORDER BY LENGTH(name) DESC;
```
![image](https://github.com/user-attachments/assets/2937315b-7b35-4869-8f0d-b2ede2b0025b)
- ** EJERCICIO 2745 Taxes **
```
Solucion:
SELECT 
name, ROUND(salary*0.10, 2) as tax
FROM
people
WHERE
salary > 3000;
```
![image](https://github.com/user-attachments/assets/8c9329fb-2e3d-46b1-a6a1-f191e372dc17)





