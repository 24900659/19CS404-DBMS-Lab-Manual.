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
<img width="806" height="553" alt="image" src="https://github.com/user-attachments/assets/4eb0edde-f951-46ad-81fb-829b3edfaf73" />


```sql
delete from Doctors
where specialization is null;
```

**Output:**
<img width="867" height="958" alt="image" src="https://github.com/user-attachments/assets/211d2213-271b-4b4c-ad89-c700b594393b" />



**Question 2**
---
<img width="870" height="582" alt="image" src="https://github.com/user-attachments/assets/79fc9aee-0c60-4a36-8810-50a86bbd0f5e" />

```sql
delete from Customer
where (GRADE > 2 AND PAYMENT_AMT < (SELECT AVG(PAYMENT_AMT) FROM Customer)) OR OUTSTANDING_AMT>8000;
```

**Output:**
<img width="862" height="717" alt="image" src="https://github.com/user-attachments/assets/46281146-8608-402a-93eb-bb593ca9a232" />



**Question 3**
---
<img width="892" height="722" alt="image" src="https://github.com/user-attachments/assets/d3943093-cfc4-4f41-99b3-45d4dbaa74ff" />


```sql
SELECT * FROM orders
where not  ((ord_date='2012-08-17' or customer_id > 3005) and purch_amt < 1000);
```

**Output:**
<img width="851" height="811" alt="image" src="https://github.com/user-attachments/assets/14689161-4569-4e95-a2ba-19d15e49c7ac" />



**Question 4**
---
<img width="862" height="520" alt="image" src="https://github.com/user-attachments/assets/c874db06-ea7b-4e33-bfb6-81caae2b72d0" />


```sql
select customer_id, cust_name, city, grade,salesman_id from customer
where city='New York' or grade>200;
```

**Output:**

<img width="862" height="557" alt="image" src="https://github.com/user-attachments/assets/a44f1499-a71d-4970-8bf3-c21703ec31a7" />


**Question 5**
---

<img width="887" height="642" alt="image" src="https://github.com/user-attachments/assets/99ab717e-a30c-4896-a652-c833a8803d4a" />

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
<img width="850" height="551" alt="image" src="https://github.com/user-attachments/assets/b49c2601-e04c-48a6-a671-92e90d14ddb0" />



**Question 6**
---

<img width="850" height="512" alt="image" src="https://github.com/user-attachments/assets/d3b822cb-8456-4b68-9c3d-77c7a354947e" />

```sql
select * from EmployeeInfo
limit 5 offset 4;
```

**Output:**
<img width="867" height="320" alt="image" src="https://github.com/user-attachments/assets/34b377e1-5c34-4b99-9ed7-1caaa2bddfe0" />


**Question 7**
---
<img width="842" height="606" alt="image" src="https://github.com/user-attachments/assets/aacf200d-8ffd-4b2f-a71b-d6e5bf1e4bb1" />



```sql
update Products 
set category = 'Household'
where product_name like '%Detergent%';
```

**Output:**

<img width="852" height="583" alt="image" src="https://github.com/user-attachments/assets/96599c44-e3ed-4645-8874-7cae6a345216" />


**Question 8**
---

<img width="877" height="655" alt="image" src="https://github.com/user-attachments/assets/b5d809e0-8b3e-46fd-82d7-528bf14b6e22" />

```sql
update Products 
set category = 'Household'
where product_name like '%Detergent%';
```

**Output:**
<img width="861" height="327" alt="image" src="https://github.com/user-attachments/assets/72783be4-aee5-445f-93f9-c99bd3b2fc64" />



**Question 9**
```
<img width="857" height="693" alt="image" src="https://github.com/user-attachments/assets/d55ec671-4e4c-41ef-b66c-fa610c8be6cc" />


```sql
delete from customer
where GRADE <> 3;
```

**Output:**
<img width="836" height="582" alt="image" src="https://github.com/user-attachments/assets/a69b658e-3e5a-4756-9257-642d3988e702" />


**Question 10**
---
<img width="892" height="520" alt="image" src="https://github.com/user-attachments/assets/d36e980d-22a0-4dac-ba88-bdc8491fd8f2" />


```sql
update Products
set reorder_lvl = 20 
where (quantity<10 and category='Snacks');
```

**Output:**
<img width="850" height="627" alt="image" src="https://github.com/user-attachments/assets/9673bcda-3301-4579-b31b-54cc0428b1cc" />


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
