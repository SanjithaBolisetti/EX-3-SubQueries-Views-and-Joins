# EX 3 SubQueries, Views and Joins 


## Create employee Table
```sql
CREATE TABLE EMP (EMPNO NUMBER(4) PRIMARY KEY,ENAME VARCHAR2(10),JOB VARCHAR2(9),MGR NUMBER(4),HIREDATE DATE,SAL NUMBER(7,2),COMM NUMBER(7,2),DEPTNO NUMBER(2));
```
## Insert the values
```sql

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7369, 'SMITH', 'CLERK', 7902, '17-DEC-80', 800, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7499, 'ALLEN', 'SALESMAN', 7698, '20-FEB-81', 1600, 300, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7521, 'WARD', 'SALESMAN', 7698, '22-FEB-81', 1250, 500, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7566, 'JONES', 'MANAGER', 7839, '02-APR-81', 2975, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7654, 'MARTIN', 'SALESMAN', 7698, '28-SEP-81', 1250, 1400, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7698, 'BLAKE', 'MANAGER', 7839, '01-MAY-81', 2850, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7782, 'CLARK', 'MANAGER', 7839, '09-JUN-81', 2450, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7788, 'SCOTT', 'ANALYST', 7566, '19-APR-87', 3000, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7839, 'KING', 'PRESIDENT', NULL, '17-NOV-81', 5000, NULL, 10);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7844, 'TURNER', 'SALESMAN', 7698, '08-SEP-81', 1500, 0, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7876, 'ADAMS', 'CLERK', 7788, '23-MAY-87', 1100, NULL, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7900, 'JAMES', 'CLERK', 7698, '03-DEC-81', 950, NULL, 30);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7902, 'FORD', 'ANALYST', 7566, TO_DATE('03-DEC-81', 'DD-MON-RR'), 3000, 20, 20);

INSERT INTO EMP (EMPNO, ENAME, JOB, MGR, HIREDATE, SAL, COMM, DEPTNO)
VALUES (7934, 'MILLER', 'CLERK', 7782, TO_DATE('23-JAN-82', 'DD-MON-RR'), 1300, 10, 10);
```

## Create department table
```sql
CREATE TABLE DEPT (DEPTNO NUMBER(2) PRIMARY KEY,DNAME VARCHAR2(14),LOC VARCHAR2(13));
```
## Insert the values in the department table
```sql
INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (10, 'ACCOUNTING', 'NEW YORK');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (20, 'RESEARCH', 'DALLAS');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (30, 'SALES', 'CHICAGO');

INSERT INTO DEPT (DEPTNO, DNAME, LOC) VALUES (40, 'OPERATIONS', 'BOSTON');
```

### Q1) List the name of the employees whose salary is greater than that of employee with empno 7566.


### QUERY:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/e4e16512-5589-47b5-b840-65030cead687)


### OUTPUT:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/3295da85-11b2-4e5f-81bd-6558670504c5)


### Q2) List the ename,job,sal of the employee who get minimum salary in the company.

### QUERY:
 
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/2668d2d4-e9e1-4eb8-a664-e552c2f44d52)

### OUTPUT:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/88cd752a-6f09-4904-955e-12b764b55555)


### Q3) List ename, job of the employees who work in deptno 10 and his/her job is any one of the job in the department ‘SALES’.

### QUERY:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/945f7753-bb0c-4d13-9d1e-192f33c9c4bb)

### OUTPUT:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/8aab52cc-39cf-4615-9998-ab95658abc0d)



### Q4) Create a view empv5 (for the table emp) that contains empno, ename, job of the employees who work in dept 10.

### QUERY:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/640c35ff-3f87-4a47-afcc-f7e108be6a00)



### OUTPUT:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/089f1ffd-69a9-4d88-9eff-56809bb64554)


### Q5) Create a view with column aliases empv30 that contains empno, ename, sal of the employees who work in dept 30. Also display the contents of the view.

### QUERY:

![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/7bbb9835-c2fc-4b58-8c0e-2bc548594fd6)


### OUTPUT:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/9af52641-5377-4b88-9ca7-ee71984945a7)



### Q6) Update the view empv5 by increasing 10% salary of the employees who work as ‘CLERK’. Also confirm the modifications in emp table

### QUERY:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/f7d0aa2b-5634-479a-b59c-a53b20b9c83f)
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/85279ec0-ce78-42a4-838a-67b5f9b20b86)


### OUTPUT:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/b625a27d-998f-4be9-858e-55af8c3377fb)

## Create a Customer1 Table
```sql
CREATE TABLE Customer1 (customer_id INT,cust_name VARCHAR(20),city VARCHAR(20),grade INT,salesman_id INT);
```
## Inserting Values to the Table
```sql
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3002, 'Nick Rimando', 'New York', 100, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3007, 'Brad Davis', 'New York', 200, 5001);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3005, 'Graham Zusi', 'California', 200, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3008, 'Julian Green', 'London', 300, 5002);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3004, 'Fabian Johnson', 'Paris', 300, 5006);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3009, 'Geoff Cameron', 'Berlin', 100, 5003);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3003, 'Jozy Altidor', 'Moscow', 200, 5007);
INSERT INTO Customer1 (customer_id, cust_name, city, grade, salesman_id) VALUES(3001, 'Brad Guzan', 'London', NULL, 5005);
```
## Create a Salesperson1 table
```sql
CREATE TABLE Salesman1 (salesman_id INT,name VARCHAR(20),city VARCHAR(20),commission DECIMAL(4,2));
```
## Inserting Values to the Table
```sql
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5001, 'James Hoog', 'New York', 0.15);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5002, 'Nail Knite', 'Paris', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5005, 'Pit Alex', 'London', 0.11);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5006, 'Mc Lyon', 'Paris', 0.14);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5007, 'Paul Adam', 'Rome', 0.13);
INSERT INTO Salesman1 (salesman_id, name, city, commission) VALUES(5003, 'Lauson Hen', 'San Jose', 0.12);
```
### Q7) Write a SQL query to find the salesperson and customer who reside in the same city. Return Salesman, cust_name and city.

### QUERY:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/68805255-9c11-4714-b14d-a3b1f8f6d615)

### OUTPUT:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/c2542522-5171-4fdd-8a48-b28dfffb4803)


### Q8) Write a SQL query to find salespeople who received commissions of more than 13 percent from the company. Return Customer Name, customer city, Salesman, commission.


### QUERY:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/f5d1c611-3691-4786-b3ae-b4f5942bd3a2)

### OUTPUT:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/68c7db4d-3e2f-4418-ad90-618f10be4510)



### Q9) Perform Natural join on both tables

### QUERY:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/7fcfbd4c-bd3c-4c7e-9b2b-720718622795)



### OUTPUT:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/82740a45-c451-4ffc-b409-6a2a9ffbf29d)


### Q10) Perform Left and right join on both tables

### QUERY FOR LEFT JOIN:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/3aeaa116-596c-4c69-a704-b3e99a6a0643)


### OUTPUT FOR LEFT JOIN:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/4355d463-42b2-4039-bd0c-30caa91376d0)



### QUERY FOR RIGHT JOIN:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/94a258f3-7c70-4bb5-afea-de18d4b98010)

### OUTPUT FOR RIGHT JOIN:
![image](https://github.com/SanjithaBolisetti/EX-3-SubQueries-Views-and-Joins/assets/119393633/2edaa8be-a8a3-4c11-b9ac-df615b9f8a09)

### Result:
SQL queries executed successfully.
