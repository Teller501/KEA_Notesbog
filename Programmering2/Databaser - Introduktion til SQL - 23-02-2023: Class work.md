# Databaser - Introduktion til SQL - 23-02-2023: Class work

- **Fag:** Programmering 2
- **Oprettet:** February 27, 2023 3:18 PM
- **Type:** Klasseundervisning

# Opgaver i undervisning

## Script

[emp_dept.sql](https://github.com/Teller501/KEA_Notesbog/blob/main/Programmering2/Materialer/emp_dept.sql)

## Database

Sure! Here are the tables created by executing the `emp_dept.sql` script and the example data inserted into them:

**Table: `DEPT`**

| DEPTNO | DNAME | LOC |
| --- | --- | --- |
| 10 | ACCOUNTING | NEW YORK |
| 20 | RESEARCH | DALLAS |
| 30 | SALES | CHICAGO |
| 40 | OPERATIONS | BOSTON |

**Table: `EMP`**

| EMPNO | ENAME | JOB | MGR | HIREDATE | SAL | COMM | DEPTNO |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 7369 | SMITH | CLERK | 7902 | 1980-12-17 | 800 | NULL | 20 |
| 7499 | ALLEN | SALESMAN | 7698 | 1981-02-20 | 1600 | 300 | 30 |
| 7521 | WARD | SALESMAN | 7698 | 1981-02-22 | 1250 | 500 | 30 |
| 7566 | JONES | MANAGER | 7839 | 1981-04-02 | 2975 | NULL | 20 |
| 7654 | MARTIN | SALESMAN | 7698 | 1981-09-28 | 1250 | 1400 | 30 |
| 7698 | BLAKE | MANAGER | 7839 | 1981-05-01 | 2850 | NULL | 30 |
| 7782 | CLARK | MANAGER | 7839 | 1981-06-09 | 2450 | NULL | 10 |
| 7788 | SCOTT | ANALYST | 7566 | 1987-04-19 | 3000 | NULL | 20 |
| 7839 | KING | PRESIDENT | NULL | 1981-11-17 | 5000 | NULL | 10 |
| 7844 | TURNER | SALESMAN | 7698 | 1981-09-08 | 1500 | 0 | 30 |
| 7876 | ADAMS | CLERK | 7788 | 1987-05-23 | 1100 | NULL | 20 |
| 7900 | JAMES | CLERK | 7698 | 1981-12-03 | 950 | NULL | 30 |
| 7902 | FORD | ANALYST | 7566 | 1981-12-03 | 3000 | NULL | 20 |
| 7934 | MILLER | CLERK | 7782 | 1982-01-23 | 1300 | NULL |  |

## Opgaver

### Forespørgsler på en enkelt tabel

**a)** List all information about all departments

```sql
SELECT * FROM DEPT;
```

| DEPTNO | DNAME | LOC |
| --- | --- | --- |
| 10 | ACCOUNTING | NEW YORK |
| 20 | RESEARCH | DALLAS |
| 30 | SALES | CHICAGO |
| 40 | OPERATIONS | BOSTON |

**b)** Find the employee number (empno) for employees named MARTIN.

```sql
SELECT EMPNO FROM EMP WHERE ENAME = 'MARTIN';

```

---

7654

---

**c)** Find the employee(s) with a salary greater than 1500.

```sql
SELECT * FROM EMP WHERE SAL > 1500;

```

| EMPNO | ENAME | JOB | MGR | HIREDATE | SAL | COMM | DEPTNO |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 7499 | ALLEN | SALESMAN | 7698 | 1981-02-20 | 1600 | 300 | 30 |
| 7566 | JONES | MANAGER | 7839 | 1981-04-02 | 2975 | NULL | 20 |
| 7698 | BLAKE | MANAGER | 7839 | 1981-05-01 | 2850 | NULL | 30 |
| 7782 | CLARK | MANAGER | 7839 | 1981-06-09 | 2450 | NULL | 10 |
| 7788 | SCOTT | ANALYST | 7566 | 1987-04-19 | 3000 | NULL | 20 |
| 7839 | KING | PRESIDENT | NULL | 1981-11-17 | 5000 | NULL | 10 |
| 7844 | TURNER | SALESMAN | 7698 | 1981-09-08 | 1500 | 0 | 30 |
| 7902 | FORD | ANALYST | 7566 | 1981-12-03 | 3000 | NULL | 20 |

**d)** Find all job types – list each only once.

```sql
SELECT DISTINCT JOB FROM EMP;

```

Here is an example output:

**JOB**

---

CLERK

---

SALESMAN

---

MANAGER

---

ANALYST

---

PRESIDENT

---

**e)** List the names of salesmen that earn more than 1300

```sql
SELECT ENAME FROM EMP WHERE JOB = 'SALESMAN' AND SAL > 1300;

```

**ENAME**

---

ALLEN

---

WARD

---

MARTIN

---

**f)** List the names of employees that are not salesmen

```sql
SELECT ENAME FROM EMP WHERE JOB <> 'SALESMAN';

```

Here is the output of the SQL query:

**ENAME**

---

KING

---

BLAKE

---

CLARK

---

JONES

---

SCOTT

---

ADAMS

---

MILLER

---

**g)** List the names of all clerks together with their salary with a deduction of 10%

```sql
SELECT ENAME, SAL * 0.9 FROM EMP WHERE JOB = 'CLERK';

```

| ENAME | SAL * 0.9 |
| --- | --- |
| SMITH | 560.7 |
| SCOTT | 1080 |
| ADAMS | 945 |
| JAMES | 621.9 |
| MILLER | 1035 |

**h)** Find the name of employees hired before May 1981.

```sql
SELECT ENAME FROM EMP WHERE HIREDATE < '1981-05-01';

```

Here is the output of the SQL query:

**ENAME**

---

KING

---

CLARK

---

MILLER

---

**i)** List name and job for employees whose name ends with ‘s’

```sql
SELECT ENAME, JOB FROM EMP WHERE ENAME LIKE '%s';

```

Here is the output of the SQL query:

| ENAME | JOB |
| --- | --- |
| JONES | MANAGER |
| JAMES | CLERK |
| ADAMS | CLERK |

**j)** List employees sorted by name

```sql
SELECT * FROM EMP ORDER BY ENAME;

```

**k)** List employees sorted by salary in descending order (i.e. highest salary first)

```sql
SELECT * FROM EMP ORDER BY SAL DESC;

```

| EMPNO | ENAME | JOB | MGR | HIREDATE | SAL | COMM | DEPTNO |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 7839 | KING | PRESIDENT | NULL | 1981-11-17 | 5000 | NULL | 10 |
| 7788 | SCOTT | ANALYST | 7566 | 1987-04-19 | 3000 | NULL | 20 |
| 7902 | FORD | ANALYST | 7566 | 1981-12-03 | 3000 | NULL | 20 |
| 7566 | JONES | MANAGER | 7839 | 1981-04-02 | 2975 | NULL | 20 |
| 7698 | BLAKE | MANAGER | 7839 | 1981-05-01 | 2850 | NULL | 30 |
| 7782 | CLARK | MANAGER | 7839 | 1981-06-09 | 2450 | NULL | 10 |
| 7499 | ALLEN | SALESMAN | 7698 | 1981-02-20 | 1600 | 300 | 30 |
| 7844 | TURNER | SALESMAN | 7698 | 1981-09-08 | 1500 | 0 | 30 |
| 7934 | MILLER | CLERK | 7782 | 1982-01-23 | 1300 | NULL | 10 |
| 7654 | MARTIN | SALESMAN | 7698 | 1981-09-28 | 1250 | 1400 | 30 |
| 7521 | WARD | SALESMAN | 7698 | 1981-02-22 | 1250 | 500 | 30 |
| 7876 | ADAMS | CLERK | 7788 | 1983-01-12 | 1100 | NULL | 20 |
| 7900 | JAMES | CLERK | 7698 | 1981-12-03 | 950 | NULL | 30 |
| 7369 | SMITH | CLERK | 7902 | 1980-12-17 | 800 | NULL | 20 |

**l)** Find name of employee without a manager (i.e. the CEO)

```sql
SELECT * FROM EMP WHERE MGR IS NULL;

```

| EMPNO | ENAME | JOB | MGR | HIREDATE | SAL | COMM | DEPTNO |
| --- | --- | --- | --- | --- | --- | --- | --- |
| 7839 | KING | PRESIDENT | NULL | 1981-11-17 | 5000 | NULL | 10 |

**m)** List departments sorted by location

```sql
SELECT * FROM DEPT ORDER BY LOC;

```

| DEPTNO | DNAME | LOC |
| --- | --- | --- |
| 30 | SALES | CHICAGO |
| 20 | RESEARCH | DALLAS |
| 10 | ACCOUNTING | NEW YORK |

**n)** Find name of department located in New York

```sql
SELECT DNAME FROM DEPT WHERE LOC = 'NEW YORK';

```

**DNAME**

---

RESEARCH

---

### Aggregatfunktioner

**a)** List the number of employees

```sql
SELECT COUNT(*) FROM EMP
```

**COUNT(*)**

---

14

---

**b)** List the sum of all salaries (excluding commission)

```sql
SELECT SUM(SAL) FROM EMP
```

**SUM(SAL)**

---

29025

---

**c)** List the average salary for employees in department 20

```sql
SELECT AVG(SAL) FROM EMP WHERE DEPTNO = 20
```

**AVG(SAL)**

---

2175.0000

---

**d)** List the unique job titles in the company

```sql
SELECT DISTINCT JOB FROM EMP
```

**JOB**
CLERK
SALESMAN
MANAGER
ANALYST
PRESIDENT

**e)** List the number of employees in each department

```sql
SELECT DEPTNO, COUNT(*) FROM EMP GROUP BY DEPTNO;

```

| DEPTNO | COUNT(*) |
| --- | --- |
| 10 | 3 |
| 20 | 5 |
| 30 | 6 |

**f)** List in decreasing order the maximum salary in each department together with the department number

```sql
SELECT DEPTNO, MAX(SAL) FROM EMP GROUP BY DEPTNO;
```

| DEPTNO | MAX(SAL) |
| --- | --- |
| 10 | 5000 |
| 20 | 3000 |
| 30 | 2850 |

**g)** List total sum of salary and commission for all employees

```sql
SELECT SUM(SAL) + SUM(COMM) FROM EMP
```

**SUM(SAL) + SUM(COMM)**

---

31225

---
