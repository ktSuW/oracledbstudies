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