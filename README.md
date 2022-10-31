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