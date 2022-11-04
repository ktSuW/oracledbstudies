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
  - What is Datastorage?
  - Types of Datastorages

</details>

<details>
  <summary> Day 2 </summary>
</details>

<details>
  <summary> Day 3 </summary>
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