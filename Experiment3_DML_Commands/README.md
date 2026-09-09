# Experiment 3: DML Commands
NAME: MOHANA K.V.S.L
REG NO: 212224240093
## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
<img width="613" height="417" alt="image" src="https://github.com/user-attachments/assets/8bfeb8b2-3b45-4c80-94a9-b78dca1b0e2b" />


```sql
delete from Doctors
where specialization is null;

```

**Output:**

<img width="597" height="673" alt="image" src="https://github.com/user-attachments/assets/4ef38891-dea9-4dc7-b559-cb25bf56805e" />


**Question 2**
---
<img width="610" height="395" alt="image" src="https://github.com/user-attachments/assets/a6af22b1-73e6-490a-8347-666a80dd7487" />


```sql
delete from Customer
where (GRADE > 2 AND PAYMENT_AMT < (SELECT AVG(PAYMENT_AMT) FROM Customer)) OR OUTSTANDING_AMT>8000;

```

**Output:**

<img width="606" height="476" alt="image" src="https://github.com/user-attachments/assets/4a5b8299-55d0-4f6a-9511-2ebbb7ca4e99" />


**Question 3**
---
<img width="611" height="489" alt="image" src="https://github.com/user-attachments/assets/85b720c7-25b0-4492-9ac6-3fbaca1f8306" />



```sql
SELECT * FROM orders
where not  ((ord_date='2012-08-17' or customer_id > 3005) and purch_amt < 1000);
```

**Output:**
<img width="608" height="574" alt="image" src="https://github.com/user-attachments/assets/20d3a2b2-15bb-451b-b90e-0fc8bf39693f" />



**Question 4**
---
<img width="612" height="364" alt="image" src="https://github.com/user-attachments/assets/a58617d2-b8fb-4804-972c-61f897de6016" />


```sql
select customer_id, cust_name, city, grade,salesman_id from customer
where city='New York' or grade>200;

```

**Output:**
<img width="618" height="382" alt="image" src="https://github.com/user-attachments/assets/0b7f02d8-0553-40c3-874f-63c94dd14ea4" />



**Question 5**
---
<img width="600" height="423" alt="image" src="https://github.com/user-attachments/assets/24a68295-e9dc-41ae-9763-cd3e6236a294" />


```sql
select id , value1,
case 
when value1 > 0 then 'Positive'
when value1 < 0 then 'Negative'
else 'Zero'
end as value_status
from Calculations;
```

**Output:**

<img width="850" height="551" alt="image" src="https://github.com/user-attachments/assets/46bd8f3f-74e6-4f7b-b5e0-c1e176d67266" />


**Question 6**
---
<img width="850" height="512" alt="image" src="https://github.com/user-attachments/assets/6ec9a296-d664-4e3d-8406-b06ef5539032" />


```sql
select * from EmployeeInfo
limit 5 offset 4;

```

**Output:**

<img width="867" height="320" alt="image" src="https://github.com/user-attachments/assets/b2bf37dc-90d7-4f70-9e9e-0061717198f3" />

**Question 7**
---
<img width="842" height="606" alt="image" src="https://github.com/user-attachments/assets/187f3c44-d251-4070-a9ec-8879317bf1a6" />


```sql
update Products 
set category = 'Household'
where product_name like '%Detergent%';

```

**Output:**

<img width="852" height="583" alt="image" src="https://github.com/user-attachments/assets/56df5790-8b22-4db2-bc45-e31e63da6ea3" />


**Question 8**
---
<img width="877" height="655" alt="image" src="https://github.com/user-attachments/assets/fdf075df-0f79-4a1b-86a7-4388ecda8fac" />


```sql
update Products 
set category = 'Household'
where product_name like '%Detergent%';
```

**Output:**

![Output8](output.png)

**Question 9**
---
<img width="877" height="655" alt="image" src="https://github.com/user-attachments/assets/b418ebed-2030-41bd-9ab0-3099870f0851" />

```sql
update Products 
set category = 'Household'
where product_name like '%Detergent%';

```

**Output:**
<img width="836" height="582" alt="image" src="https://github.com/user-attachments/assets/de252b8f-e4e8-47f7-b385-e4982dc468e5" />



**Question 10**
---
<img width="892" height="520" alt="image" src="https://github.com/user-attachments/assets/c7d77949-a14f-4b7f-9bb8-ac7b6f3d89fa" />


```sql
update Products
set reorder_lvl = 20 
where (quantity<10 and category='Snacks');

```

**Output:**

<img width="615" height="456" alt="image" src="https://github.com/user-attachments/assets/89f89d1f-63c5-41fc-83d0-c3147c8fa623" />

## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
