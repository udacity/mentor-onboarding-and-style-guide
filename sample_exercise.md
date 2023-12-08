## Exercise Instructions

### Task 1: Create your Azure resources
Create an Azure Database for PostgreSQL single server. Choose the Basic SQL database compute+storage, i.e., *Standard_B1ms* (1vCore) compute and 32GiB storage. Here are the configuration you must choose while creating a Database for PostgreSQL:

<p align=center>

|**Field**|**Value**|
|---|----|
|Resource group|ODL-DataEng-xxxxx|
|Workload type|Development|
|Compute + storage|Burstable, B1ms<br>1 vCores, 1 GiB RAM, 32 GiB storage<br>Geo-redundancy : Disabled|
| Admin username | `sqladminuser` |
| Password | `password@123` |

Also, note that the TLS/SSL is enforced on the server by default. You must disable the **require_secure_transport**. 
</p>
<br /><br />

### Task 2: Design a star schema

You are being provided a relational schema that describes the data as it exists in PostgreSQL. In addition, you have been given a set of business requirements related to the data warehouse. You are being asked to design a star schema using fact and dimension tables. 
<br /><br />

### Task 3: Create the data in PostgreSQL
Open a terminal session, and copy over the files from local to the PostgreSQL server

```bash
git clone https://github.com/udacity/Azure-Data-Warehouse-Project.git
cd Azure-Data-Warehouse-Project/starter
mkdir data
# Download the CSV files from the classroom resrouces section.
cp -r ~/Downloads/Out/ data/
# Update the host, username, and passsword in the ProjectDataToPostgres.py file.
pip install psycopg2
python ProjectDataToPostgres.py
# psql -h "mypostgresserver230963.postgres.database.azure.com" -U "sqladminuser" -d "mydatabase" -c "\copy friends FROM 'friends.csv' with (format csv,header true, delimiter ',');"
```


Open another terminal session and connect to the database using a command similar to:
<br />

```bash
# Replace the host, username and password as applicable to you.
psql "host=mypostgresserver230963.postgres.database.azure.com port=5432 dbname=udacityproject user=sqladminuser password=password@123 sslmode=require"
# Run these commands in the psql 
\list
\connect udacityproject
\dt
```
It should display the output similar to:

```bash
udacityproject-> \dt
            List of relations
 Schema |  Name   | Type  |    Owner
--------+---------+-------+--------------
 public | payment | table | sqladminuser
 public | rider   | table | sqladminuser
 public | station | table | sqladminuser
 public | trip    | table | sqladminuser
(4 rows)
```

You can verify the data as:

```bash
select count (*) from payment;      # 1946607
select count (*) from rider;        # 75000
select count (*) from station;      # 838
select count (*) from trip;         # 4584921
```


<br /><br />


### Task 4: EXTRACT the data from PostgreSQL
Create Azure Synapse workspace with the default serverless SQL pool. Use the ingest wizard to create a one-time pipeline that ingests the data from PostgreSQL into Azure Blob Storage. This will result in all four tables being represented as text files in Blob Storage, ready for loading into the data warehouse.  

1. Create a Linked service for Azure Database for PostgreSQL. To establish a connection, ensure that **require_secure_transport** is disabled in the Postgres server. 


2. Create a Linked service for Azure Storage Account. 


3. Ingest data (four tables) from PostgreSQL to Blob storage in the .csv format. 


4. Verify the data ingestion by navigating to **Data > Linked > Azure Blob Storage > [storage_account] > [storage_contaienr]**. It must show all imported .csv files. 



<br /><br />


### Task 5: LOAD the data into external tables in the data warehouse

Once in Blob storage, the files will be shown in the data lake node in the Synapse Workspace.  From here, use the script-generating function to load the data from blob storage into **external staging tables** in the data warehouse you created using the serverless SQL Pool. 

- Navigate to the Linked data tab. 
- View the files in the ADLS. It should show all those files you may have imported to the Azure blob storage in the previous EXTRACT step. 
- Selct a file, and write a new SQL script to create an external staging table (say `staging_payment`). 
- If a SQL database is not present already, it will prompt you to create a new database in the wizard. 
- Review the SQL script, and run it to create the external staging table. 

<br /><br />


### Task 6: TRANSFORM the data to the star schema

Write SQL scripts to transform the data from the staging tables to the final star schema you designed.  




### Helpful Hints

* When you use the ingest wizard, it uses the copy tool to EXTRACT into Blob storage. During this process, Azure Synapse automatically creates links for the data lake. When you start the  SQL script wizard to LOAD data into external tables, start the wizard from the data lake node, not the blob storage node. 

* When using the external table wizard, you may need to modify the script to put dates into a varchar field in staging rather than using the datetime data type.  You can convert them during the transform step.

* When using the external table wizard, if you rename the columns in your script, it will help you when writing transform scripts. By default, they are named [C1], [C2], etc. which are not useful column names in staging.
