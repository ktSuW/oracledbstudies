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

<details>
  <summary> Day 4 </summary>
</details>

<details>
  <summary> Day 5 </summary>
</details>

<details>
  <summary> Day 6 </summary>
</details>

<details>
  <summary> Day 7 </summary>
</details>

<details>
  <summary> Day 8 </summary>
</details>

<details>
  <summary> Day 9 </summary>
</details>

<details>
  <summary> Day 10 </summary>
</details>
