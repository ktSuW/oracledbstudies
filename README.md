# Oracle Database Studies Notes

This repo contains oracle db studies notes.
- [Apex Oracle can be used](https://apex.oracle.com/pls/apex/f?p=4550:1:109036778534060:::::)
## Notes 

<details>
  <summary> Week : 1 Intro </summary>

    ```
        SELECT  ENAME AS Employee_Name , JOB AS Employee_Job FROM EMP;
        select  DNAME AS Department_Name , LOC AS Department_Location from dept;

        SELECT JOB FROM EMP;
        SELECT distinct JOB FROM EMP;

    ```
- where filter 

```
    SELECT * 
    from emp 
    where job = 'MANAGER';

    SELECT *  from emp  where SAL <= 1500;
    SELECT *  from emp  where SAL <= 1500 and JOB = 'CLERK';
    SELECT *  FROM emp  WHERE SAL <= 1500 AND JOB != 'CLERK';
```
- **31 October 22 - Theory** 
  - [Connecting with SQL*Plus 18c](https://www.oracle.com/au/database/technologies/instant-client/winx64-64-downloads.html)
  - Oracle -> Database , store data permanently in secondary storage devices, Matrix formation
    - SQL language 
    - PL/SQL : Procedural language 
    - Dynamic SQL
  - ANSI standard SQL
    - Oracle : oracel sql -> nvl()
    - SQL server : sqlserver sql -> isnull()
    - MYSQL : mysql sql -> ifnull()

- **1 October 22 - Theory **
```
  - Account No. Name    Balance
    1001        Aalla     3000
    1002        Bella

    You cannot withdraw more than 3000.

    create or replace procedure p1(p_account_number, p_amount_number)
    is
    v_balance number(10);
    begin
    select balance into v_balance from bank
    where accountNo == p_account_number;
    if p_amount < v_balance then
    update bank set balance = balance - p_amount where accountNo = p_account_number;
    dbms.output.put_line('Transaction successful');
    commit;
    else 
    dbms_output.put_line('Insufficient funds');
    end if;
    exception
    when others then
    rollback;

    set serveroutput on;
    exec p1(1001, 8000); // Insufficient funds code part will be executed.

    exec p1(1001, 2000); // Transaction successful code part will be executed.

    select * from bank; // balance will be 1000;


```
  - www.amazon.com -> web server -> db server -> db database
    - order-main table
      - orderID (Primary Key), orderDate, orderItem, orderPrice, 
    - Purchase

<details>

<details>
  <summary> Session:  </summary>
<details>

<details>
  <summary> Session:  </summary>
<details>

<details>
  <summary> Session:  </summary>
<details>