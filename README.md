# Oracle Database Studies Notes

This repo contains oracle db studies notes.
- [Apex Oracle can be used](https://apex.oracle.com/pls/apex/f?p=4550:1:109036778534060:::::)
  
## Notes 


<details>
  <summary> Day 1 : Basic Intro </summary>

- Basic Terminology of DB
  - What is data?
    - Could be number, characters, special characters, etc.
  - What is information?
    - Processing, meaningful information
  ```
      Employee    ID
      ========    ===
      Sam         1
      Lee         2
      Kelly       3
  ```
  - What is Database?
    - Storage memory where we can store the information, memory space where we can store the **collection of inter-related data/information**
    - e.g. Banking application
  ```
        DB_YourBank (database ID)
          > branches group-----------> customers 
              > department group
                  > Employee group 
        
        no employees == no departments
        no departments == no employees
  ```
  - Types of Databases
    - OLTP (online transaction processing)
      - store day to day transactional information
      - OLTP data source is from applications. Every transactional data  will be saved.
      - When OLTP data are full, they will be transferred to OLAP.
    - OLAP (Online analytical processing) (data warehouse)
      - Store historical big data/information
      - e.g. data warehouse 
      - OLTP to OLAP is by ETL tools (PowerBI Integration Services, SSIS, Informatica)
        - Extract 
        - Transfer
        - Loading 
        - How they transfer is by Job Schedules
    - <img src="https://tutorialshut.com/wp-content/uploads/2020/11/OLTVVsOLAP-768x499.jpg" width=500>
    - <img src="https://www.researchgate.net/publication/327656028/figure/tbl1/AS:673012806336514@1537470165105/DIFFERENCES-BETWEEN-OLTP-AND-OLAP.png" width=500>
    - <img src="https://rkicdn.rkimball.com/1663579722423.png" width=500>
    - <img src="https://databasetown.com/wp-content/uploads/2019/10/types-of-databases-1.jpg" width=500>
    - <img src="https://galaktika-soft.com/wp-content/uploads/2018/01/oltp.jpg" width=500>


</details>

<details>
  <summary> Day 2 : Basic definitions => Datastorage, Data redundancy, inconsistency, retrieval, integrity, secuirty, indexing , DBMS, Models of DBMS</summary>

- What is Datastorage
  - It is a location where we can store data/information in early days
- Types of Datastorages
    - Papers and books (before computers) - security, data manipulation, transfer - very challenging 
    - Flatfile (textfile) - (early day of computer) - 
    - DBMS (softwares)
- Flatfile / File management system
  - Challenges
    - Data redundancy : Duplicates data , store the same information in a number of files. Memory wastage.
  ```
      File1
        Employee Details
        EID   EName       DateOfCommenced   Role    Salary    Gender
        1001  Sally       05-11-2022        SE      150,000     F
        1002  Smith       03-11-2020        JSE     89,000      M


      File2
        Employee Details
        EID   EName       DateOfCommenced   Role    Salary    Gender
        1001  Sally       05-11-2022        SE      150,000     F
        1002  Smith       03-11-2020        JSE     89,000      M
  ```
      - Thre is no error message from the computer saying the data is duplicated.
    - Data inconsistency :
      - Shows different data for the same object. 
      - After someone manipulates the data in File2, File1 and File2 data are not the same any more.... 
      - This can be resolved with PK, FK, Normalisation.
      - When we have data redundancy then there is a chance to get data inconsistency problem.
      - No duplicate == no consistency
    - Data retrieval : 
      - Very hard to retrieve data from a file.
      - High level programming languages C, C++, Java - Applications I/O File handling 
    - Data integrity mechanism
      - Data validation 
      - Mobile number entry e.g. It should be 10 digits. But users can add any length in File1 or File2. Invlaid data gets accepted.
      - There is no accuracy in the data.
    - Data security 
      - Very poor security 
    - Data indexing 
      - To access the required data in efficient manner 
      - e.g. every textbook has index page. Book has 400 pages. Topic has page number.
      - Retrieval of required topic is fast.
      - 
- What is dBMS?
  - By using DBMS, we can perform the following operations:
      - create database memory
      - create table
      - insert
      - update
      - select
      - delete 
    - DBMS will act as an "interface" between user and database memory .
      - User <-----------> DBMS (interface) <---------> Database
- Models of DBMS
  - Hierarchical database management system (HDBMS) - first DBMS e.g. IMS information management system
    - Root, parent, child - time consuming, data duplication
    - Security, retrieval 
  - This HDBMS was enhanced with Network database management system (NDBMS) e.g. IDBMS s/w integrated dbms with network
  - **NOTE: HDBMS and NDBMS are no longer in use.**
  - Relational DBMS
    - Object relational database management system (ORDBMS)
    - Object Oriented database management system (OODBMS)
    - <img src="https://www.assignmenthelp.net/images/database-models.png" width=550>
    - <img src="https://webimages.mongodb.com/_com_assets/cms/kod60sm2c5px0q7do-Object-Oriented-DBs-Example.png?auto=format%2Ccompress" width=550>
    - <img src="https://anydifferencebetween.com/wp-content/uploads/2016/09/Difference-Between-Relational-Database-and-Object-Oriented-Database.jpg" width=550> 
    - <img src="https://d3i71xaburhd42.cloudfront.net/35c0ff1b084ba700f4bb8125f7a34d66da44cc22/4-Table1-1.png" width=550>

- Advantages of DBMS

</details>
  
---
  
<details>
  <summary> Day 3 </summary>

- Object Relational DBMS
  - Data can be stored in table format
  - Tabular format 
  - Depends on SQL Language. Therefore they are called SQL d
  - e.g. Oracle, SQL server, mysql, postgresql, db2, etc.
  - 
- Object Oriented DBMS
  - data can be stored in "object" format
  - Not depend on "SQL", NoSQL DB
  - e.g. MongoDB, Cassandra, etc.

- Oracle, DBMS, 1979 - store data/information permanently (e.g. hardisk) and along with security
- Oracle can be deployed in any OS
- Types of edition
  - Oracle express 
- Working with Oracle
  - When working with oracle DB, follow the following two steps:
    - Connect to Oracle server : use client tools
        - SQL developer, **SQL plus** - CUI (Character User Interface)
    - Communicate with Oracle DB : After successfully connecting to the server,
      - needs to send request (SQL)
      - get response back
  - SQL plus
    - db tool from oracle
    - Used to connec to oracle server
    - Can be used as an editor
  - SQL
    - DB language from IBM
- Standard
  - DDL
  - DML
  - DQL
  - TCL
  - DCL
- How to connect to Oracle DB server
- Download Oracle 19c, [sql plus](https://www.youtube.com/watch?v=Fh-1eO8SA9o)
 - Go to All Programs -> Oracle 19db Home
    - sql plus 
    - Enter user-name:system
    - Password : enterYourPassword - for security reason, the password will not be visible
    - Login successful! Connected to:
    - Another way - username is not case sensitive, but password is
      - system/password
      - SYSTEM/password 
 - Common connection error fixing tips
    - Go to services -> oracleServiceORCL -> select startup type: automatic -> click start button -> Apply -> OK
    - GO to SQL plus -> enter username : system/password 
    - TNS protocol adapter error 

</details>
---
<details>
  <summary> Day 4 </summary>
</details>  

---

<details>
  <summary> Day 5 </summary>
- [some tips](https://stackoverflow.com/questions/35199084/forgot-oracle-username-and-password-how-to-retrieve#:~:text=Once%20connected%2Cyou%20can%20enter,the%20password%20for%20that%20user.)
- Structured Query English Language (SEQUEL), later SQL
- SQL Plus : SQL*Plus is a client terminal software allowing users to interact with Oracle server to manipulate data and data structures. Users type in SQL statements in SQL*Plus that send statements to Oracle server. Oracle server then validates and executes the statements on its databases.
- Sub languages of SQL
  - DDL - Data definition language 
    - create : a new db object in oracle db e.g.table, views, synonyms, procedure, function, triggers, etc.
      - table is a core object of db. 
      ```
        CREATE TABLE <TABLE NAME>
        ( 
          <COLUMN NAME1> <DATATYPE>[SIZE], 
          <COLUMN NAME1> <DATATYPE>[SIZE], 
          <COLUMN NAME1> <DATATYPE>[SIZE]
         );
      ```
    - alter
      - alter modify
      - alter -add 
      - alter - rename
      - alter - drop
    - rename
    - truncate
    - drop
  - new commands 
    - recyclebin
    - flashback
    - purge
- Data Manipulation Language (DML)
  - insert
  - update
  - delete 
  - new commands 
    - insert all
    - merge
- Data query/ retrieval (DQL/DRL)
  - select 
- Transaction control langauge (TCL)
  - commit 
  - rollback
  - savepoint 
- Data control langauge (DCL)
  - grant
  - revoke 
- <img src="http://2.bp.blogspot.com/-zYkYjhaqEps/VgS24O6hdqI/AAAAAAAAAVI/X_K858Bph7U/s1600/DDL_DML.jpg">
- <img src="https://csharpcorner-mindcrackerinc.netdna-ssl.com/article/sql-commands-ddl-dql-dml-dcl-tcl-with-examples/Images/SQL_Diagram.drawio.png">

- Oracle data types
  - numeric 
    - int = number(38) - 38 digits 
    - serial number column int - sno number(38), sno number(1)
      - sno number(4) => you can save 1, 23, 554, 1234.
    - number(p,s) => precision, counting all digits including left and right sides digits of a decimal point
      - storing both integer and float values 
      - number(p) - only integer
      - number(p,s) - float values 
      - e.g. 65.34 => precision = 4
      - e.g. 1223589.34 => precision = 9
      - e.g. S-SCALE 
    - counting the right side digits only
      - 89.22 => scale = 2, precision = 4
      - 12345.67 => scale = 2, precision = 7 
      - e.g. Product_Price(6,2) 
  - string
    - EMPLOYEE_NAME CHAR(10) -  'Sally', without '' is char
    - [Data types](https://docs.oracle.com/database/121/SQLRF/sql_elements001.htm#SQLRF0021)
  - long
  - date
  - raw and long 
  - lob 
 - <img src="https://cf.ppt-online.org/files1/slide/w/WahumSXpt1zDy46bOenj38g5wZEdJiPR0LCUYf/slide-10.jpg">
</details>
            
---
            
<details>
  <summary> Day 6 </summary>
</details>

 ---
            
<details>
  <summary> Day 7 </summary>
</details>
            
 ---
            
<details>
  <summary> Day 8 </summary>
</details>

 ---
            
<details>
  <summary> Day 9 </summary>
</details>

<details>
  <summary> Day 10 </summary>
</details>
