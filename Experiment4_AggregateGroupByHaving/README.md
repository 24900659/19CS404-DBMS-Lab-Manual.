# Experiment 4: Aggregate Functions, Group By and Having Clause
NAME: MOHANA K.V.S.L

REG NO: 212224240093
## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
How many patients are covered by each insurance company?

Sample table:Insurance Table

name type

InsuranceID INTEGER

PatientID INTEGER

InsuranceCompany TEXT

PolicyNumber TEXT

PolicyHolder TEXT

ValidityPeriod TEXT

```sql
SELECT InsuranceCompany, count(PatientID) as TotalPatients from Insurance group by InsuranceCompany;
```

**Output:**

<img width="972" height="741" alt="image" src="https://github.com/user-attachments/assets/3b3ff11e-a667-48ec-87b6-0bd7f6176272" />


**Question 2**
---
<img width="1224" height="757" alt="image" src="https://github.com/user-attachments/assets/4732f728-5671-4519-906d-8c6d537a372c" />


```sql
select DoctorID, count(PrescriptionID) as TotalPrescriptions from Prescriptions group by DoctorID;
```

**Output:**
<img width="954" height="761" alt="image" src="https://github.com/user-attachments/assets/67d67c82-2084-4d0a-bdd9-50c4184e7af4" />


**Question 3**
---
How many patients have insurance coverage valid in each year?

Sample table:Insurance Table

name type

InsuranceID INTEGER PatientID INTEGER InsuranceCompany TEXT PolicyNumber TEXT PolicyHolder TEXT ValidityPeriod TEXT

```sql
select SUBSTR(ValidityPeriod,1,4) as ValidityYear,count(PatientID) as TotalPatients from Insurance group by SUBSTR(ValidityPeriod,1,4) order by ValidityYear;
```

**Output:**

<img width="855" height="568" alt="image" src="https://github.com/user-attachments/assets/b38582b4-5e15-46cf-ba73-143829eeb7ef" />


**Question 4**
---
Write a SQL query to find the total amount of fruits with a unit type of 'LB'.

Note: Inventory attribute contains amount of fruits

Table: fruits

name type

id INTEGER name TEXT unit TEXT inventory INTEGER price REAL

```sql
select SUM(inventory) as total from fruits where unit='LB';
```

**Output:**

<img width="621" height="476" alt="image" src="https://github.com/user-attachments/assets/f9b471a3-880c-4ff8-902d-09a58c73b80d" />


**Question 5**
```
Write a SQL query to find the total income of employees aged 40 or above.

Table: employee

name type

id INTEGER name TEXT age INTEGER city TEXT income INTEGER

```sql
select SUM(income) as total_income from employee where age>=40;
```

**Output:**

<img width="584" height="476" alt="image" src="https://github.com/user-attachments/assets/b0407493-9d3d-4304-b9f1-f50d4884db6a" />


**Question 6**
---
Write a SQL query to Calculate the average email length (in characters) for people who lives in Mumbai city

Table: customer

name type

id INTEGER name TEXT
city TEXT email TEXT phone INTEGER
```sql
select AVG(LENGTH(email)) as avg_email_length_below_30 from customer where city='Mumbai';
```

**Output:**
<img width="820" height="521" alt="image" src="https://github.com/user-attachments/assets/7d92785e-1c80-4cbf-bd12-90fa81571ff6" />



**Question 7**
---

<img width="1210" height="600" alt="image" src="https://github.com/user-attachments/assets/ced7becd-847c-4137-a804-68f027e9eee4" />

```sql
select count(*) as COUNT from customer where city<> 'Noida';
```

**Output:**

<img width="575" height="477" alt="image" src="https://github.com/user-attachments/assets/40ca9d04-5f76-4fce-a86a-de3a944a62c3" />


**Question 8**
---
<img width="1205" height="622" alt="image" src="https://github.com/user-attachments/assets/7ab36c57-ee78-463d-b612-4ff0b0f1c4ba" />

```sql
select age,MAX(income) from employee group by age having max(income)>2000000;
```

**Output:**

<img width="778" height="536" alt="image" src="https://github.com/user-attachments/assets/5dc619d8-43a1-4b0d-81fd-8778799d7938" />


**Question 9**
---
<img width="1167" height="677" alt="image" src="https://github.com/user-attachments/assets/1fc02947-18ed-4e46-97c5-35110e11332f" />

```sql
select city,SUM(income) as Income from employee group by city having SUM(income)>200000;
```

**Output:**
<img width="801" height="723" alt="image" src="https://github.com/user-attachments/assets/494ce106-b8a6-4be5-bbb1-529b7ef7cd54" />


**Question 10**
---
<img width="1203" height="635" alt="image" src="https://github.com/user-attachments/assets/ab3d8693-9c09-4341-adf7-e50b75985661" />


```sql
select occupation,AVG(workhour) from employee1 group by occupation having AVG(workhour) between 10 and 12;
```

**Output:**
<img width="875" height="578" alt="image" src="https://github.com/user-attachments/assets/c6f4dc71-7abf-4397-b405-55f7fb6a8424" />



## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
