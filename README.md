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

---

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
  <summary> Day 3 : Intro Continued </summary>

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
  <summary> Day 5 : SQL sublanguages overiew </summary>
  
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
  <summary> Session 7 : SQL connection issues </summary>

- **Problem-1**
 - \sys as sysdba (default username)
 - password is sys (default password)
 - alter user system account unlock;
 - alter user system account lock;
 - conn => connect
 - **Problem-2**
  - Services => OracleServiceORCL => Stop
  - TNS: protocol adapter error
  - Go To Services and check whether it is running or stop mode.
    - Status Type -> Automatic 
    - Start 

  - **Problem -3**
    - Enter username: username/ password
    - Error : unreacheable host
    - Solution: 
      - Enter Username: \sys as sysdba
      - Enter password: sys
      - connected
    - SQL> ALTER USER SYSTEM ACCOUNT UNLOCK;
    - SQL> ALTER USER SYSTEM IDENTIFIED BY yournewpassword;
    - SQL > CONN
    - Enter username: system / yournewpassword
    - connected
  - **Problem -4**
      - Enter Username: \sys as sysdba
      - Enter password: sys
      - error : Unable to connect to Oracle db server
      - reinstall Oracle software 

- How the client tool SQL Plus connect to SQL server
  - When we install Oracle software, there are two components installed by the system automatically:
    - Client component can perform the following three operations:
      - User can connect
      - User can send request to the server
      - User get the response back from the server
      - e.g. sql plus, sql developer, toad
    - Server component
      - Instance component
        - It is a temporary memory (allocated from RAM location)
        - This instance sub component can store data temporarily 
      - Database component
        - Permanent storage memory which will allocated from hard disk
        - Storing data permanently
    - Client Server architecture 
      - Every newly inserted data first will go to the Instance memory
      - If user wants to move data from instance memory into database, you need to commit.
        - instance db(allocate from RAM) to the permanent storage database (allocate from HD) => commit
      - data retrival is from permanent db
        - select * from tab;
  - create own user account (username and password) in Oracle db
    - create user onisan identified by Ramen123
    - If you come across with this error, [How to Resolve ORA-65096: invalid common user or role name](https://logic.edchen.org/how-to-resolve-ora-65096-invalid-common-user-or-role-name/) & [How to Resolve ORA-01109: database not open](https://logic.edchen.org/how-to-resolve-ora-01109-database-not-open/)
      - show con_name
      - alter session set container=orclpdb;
      - create user Eden identified by house (credentials are assigned to the employees)
        - First level security - you cannot use the credentials to connect to db.
        - every new user is a dummy user. DBA needs to give permissions/priviledges
      - HOw DBA grant permissions to user
        - grant priviledgeName to username
        - e.g. grant connect to Eden
        - If the grant succeeded, user will be able to login
        - Eden/house
        - **unable to grant. debug**
    - How to change password by user 
      - select * from ALL_USERS;
      - SQL> PASSWORD 
      - Enter old password and enter new password
      - SQL > CONN
      - Enter user-name: username/password
    - How to recreate a new password for a user
      - alter user username identified by new_password
      - alter user mydb2pm identified by mydb2pm
      - alter session set "_ORACLE_SCRIPT"=true;  
      - grant sysdba to user_name;
    - How to view usernames if we forget
      - select username from All_USERS;
    - How to drop a user from DB
      - drop user username cascade;

</details>

 ---
            
<details>
  <summary> Session 9:  Datatypes </summary>

- String data type
  - characters only string - A-Z, a-z
    - non-unicode datatypes - supports to store localised data e.g. english language ONlY
      - char(size) - fixed length datatype 
        - static
        - non unicode char -> 1 char = 1 byte
        - Emp_Name char(10) => 'HELLO' - 5 bytes used -> 5 bytes remaining.
        - Therefore, waste 5 bytes. If you know the size and it won't change, then use it. Otherwise, there is memory wastage.
        - maximum size is 2000 bytes 
      - varchar2(size)
        - ANSII datatype , variable length datatype, dynamic
        - maximum size is 4000 bytes
        - Due to its dynamic nature, it will not waste memory like char. 
        - 'Hello' -, Allocates 5 bytes, there is 0 memory bytes waste.
          - 5 - 5 = 0
    - unicode datatypes - supports multilingual langauges , n stands for national
      - nChar(size)
        - fixed length datatype , static,
        - store unicode char (all national langauges)
        - memory wastage is same was char.
        - 2000 bytes
      - nvarchar2(size)
        - 4000 bytes
        - n stands for national 
  - alpanumeric characters
- long data type
  - dynamic datatype, store non unicode character & unicode character 
  - 1 char == 1 byte
  - maximum size is 2GB.
  - customer_Address long - out of 2GB - 30bytes = 1024 x .....
    - Name: Ellen Smith
    - 123/45 Heaven Street, Earth 67890 
  - **every table should have only one long data type column**
- Date
  - store date and time information 
  - Date : store date & time information of particular day
    - time is optional. If user does not enter time information by default, oracle server will take '00:00:00am' or '12:00:00am'
    - date range must be from '01-jan-4712 bc' to '31-dec-9999ad'
    - DateOfJoining => 11-Nov-2022 15:19 - system time and insertion time is different
      - sysdate
      - Oracle default date formate - 'DD-MON-YY/YYYY HH:MM:SS'
      - '11-NOV-22 15:21:XX'
      - 1    1   2  1  1  1   ---> 7 BYTES (fixed memory)
  - Timestamp
    - store date and time information along with milliseconds 
    - Oracle default timestamp datatype is, 
      - 'dd-mon-yy/yyyy hh:mm:ss.ms' 
      - '11-Nov-2022 15:24:56.0000'
      -  1  1   2    1  1  1  4  => 11 bytes - fixed memory 
- [Raw and long raw ](https://docs.oracle.com/database/121/SQLRF/sql_elements001.htm#SQLRF0021)
  - image file, multimedia files, audio files - in the form of binary format.
  - database will convert pictures into binary format
  - These datatypes are also called as "Binary data types"
  - raw 
    - maximum size : 2000 bytes
  - long raw : 2GB
- Lob datatypes
  - lob - large objects
  - clob - character large objects 
    - store non-unicode char
    - dynamic datatype
    - maximum size is 4GB
  - **Non-unicode char**
    - char(size) - 2000 bytes
    - varchar(size) - 4000 bytes
    - long - 2GB
    - clob - 4GB
  - nclob
    - national characters large object
    - dynamic datatype
    - maximum size - 4GB
  - Unicode char
    - nchar(size) - 2000 bytes
    - nvarchar(size) - 4000
    - long -2GB
    - nclob - 4GB
  - blob
    - binary large object
    - store image/audio/video file
    - dynamic dataype
    - maximum size = 4GB
  - Binary data
    - raw - 2000 bytes
    - long raw - 2GB
    - blob - 4GB



</details>
            
 ---
            
<details>
  <summary> Session 10 : alter, grant, truncate, drop, recyclebin </summary>

1. Connect to system/Yourpassword
2. create user yourusername identified by youruserpassword
3. grant connect

- connect su/su
4. create table Student(SId int, SName char(10), SFees number(6,2));

```
  dBA is system/YourPassword
  create user su identified by su;
  alter session set "_ORACLE_SCRIPT"=true;
  alter session set container=ORCLPDB;
  ORA-65024: Pluggable database ORCLPDB is not open.
  ORA-01031: Insufficient privileges 

  connect/ as sysdba;
  grant all privileges to system;
  grant connect to su;
  ORA-01017: invalid username/password; logon denied
  select * from ttab;


  create table student 
  (
    SId int,
    SName char(10),
    SFees number(6,2)
  );

  If you have infufficient priviledges, you need to ask ssystem admin for permission
  conn
  grant create table to su;

```
- **View list of tables in oracle db**
  - select * from tab;
  - TName - table name
  - TabType - which type of object you have created
    - Tabtype - table object for Student
    - ClusterId - 
- **View the structure of table**
  - desc means describe 
  - desc Student;
  - SId int, SId number(38) means int == number(38)
- **Alter**
  - To change/ modify the structure of a table
  - Sub commands under alter
    - alter - modify
    - alter - add
    - alter - rename
    - alter - drop
  - Alter modify 
    - Change data type and size  e.g. char(10)
    - alter table <Table Name> modify <Column Name> <New Datatype>[New size];
    - alter table Student modify SName varchar2(20);
  - Alter add
    - add new column to an existing table
    - alter table <table name> add <new column name> <datatype>[size];
    - alter table Student add SAddress varchar2(20);
    - You can only add column to the end of the table structure
  - Alter rename
    - Change the column's name
    - alter table <table name> rename <column> <old column name> to <new column name>
  - Rename - for renaming the table 
    - Change a table name
    - rename <old table name> <new table name>
  - Alter drop (delete)
    - alter table <table name> drop <column> <column name>;
    - alter table Student drop column SFees;
  
  - Truncate 
    - You have created a table with some columns. Structure of table, no data
    - After that, users insert data. Then rows will be added.
    - When you use truncate, only rows are deleted. Structure of the table remains.
    - truncate table <table name>;
    - you cannot delete specific row. In the query statement, you need to use where condition. where condition is not supported under the truncate command.
    - insert into StudentInfo values(1, 'Kim', 'Busan', 'kim@moon.com');
    - ORA-01959: no privileges on tablespace 'Users';
    - conn
    - system/yourpassword
    - grant unlimited tablespace to su;
    - After this, you have unlimited access to hardisk memory.
    - You cannot delete it using where clause
      - truncate table StudentInfo where SName='Son';
    - commit;
  - Drop
    - To delele the entire table 
    - drop table <table name>
    - drop table StudentInfo;
    - select * from tab;
      - you will see tabtype - some address location
      - After dropping your table, you will see the address.
      - It means you have deleted temporarily 
      - BIN$AboOgAhsTB+MAgBKRal/dA==$0
        - BIN means recycle bin
        - Before Oracle10g enterprise edition, once you drop the table from a database, that is permanent whereras from orcle10g enterprise edition, once you drop a table from a database, it is temporary.
      - New Features in Oracle10g Enterprise Edition
        - recyclebin
        - flashback
        - purge
    - Recyclebin
      - It is a system defined table.
      - it is one of the table name, inbuilt table 
      - desc recyclebin;
      - select OBJECT_NAME, ORIGINAL_NAME from recyclebin;

</details>

 ---
            
<details>
  <summary> Session 11 </summary>

- set pagesize 100;
- set lines 160;
- desc recyclebin;
- select * from tab;
- **flashback** - restore what is in the recyclebin
  - Use to restore deleted table from recyclebin to database memory 
  - flashback table <table name> to before drop;
  - e.g. flashback table StudentInfo to before drop;
- **purge**
  - delete your table permanently from database memory including recyclebin
  - To delete a specific table from recyclebin
  - purge table <table name>
  - purge table Apartment;
  - select * from tab;
  - flashback table Apartment to before drop; // object not in Recycle bin
- Delete all tables from recyclebin
  - purge recyclebin;
- Delete table from database permanently 
  - drop table <table name> purge;
- show user;  
  - If you add as admin user;
  - If the table is not showing in recyclebin, it means you have connected as system admin;
  - Finished at 31:00min

</details>

---

<details>
  <summary> Session 12 </summary>
</details>

---

<details>
  <summary> Session 13 </summary>
</details>

---

<details>
  <summary> Session 14 </summary>
</details>

---

<details>
  <summary> Session 15 </summary>
</details>


---

<details>
  <summary> Session 16 </summary>
</details>

---

<details>
  <summary> Session 17 </summary>
</details>


---

<details>
  <summary> Session 18 </summary>
</details>

---

<details>
  <summary> Session 19 </summary>
</details>

---

<details>
  <summary> Session 20 </summary>
</details>

---