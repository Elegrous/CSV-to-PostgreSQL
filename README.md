# Azure-PostgreSQL
Create PostgreSQL database from CSV file and open it in DBeaver

1. Open [Microsoft Azure portal](https://portal.azure.com/)

2. Create Virtual Machine in Azure:
<img width="500" alt="image" src="https://user-images.githubusercontent.com/44158648/154346439-5969001e-e76d-4809-baaf-bfa979de167d.png">

3. Install [PostgreSQL](https://www.postgresql.org/download/)
<img width="600" alt="image" src="https://user-images.githubusercontent.com/44158648/154361329-95e55257-b2a0-46e2-bb10-368f7cf55875.png">

4. Create Database
<img width="350" alt="image" src="https://user-images.githubusercontent.com/44158648/154361594-af4ee363-4613-46cf-8b5e-efbee678b8da.png">

5. Create Table
<img width="300" alt="image" src="https://user-images.githubusercontent.com/44158648/154361820-89946cf3-7f43-459d-9aa1-58dc375a43eb.png">

Add Columns to the Table: <br/>
<img width="600" alt="image" src="https://user-images.githubusercontent.com/44158648/154362633-9ba01fcc-d984-4ddb-b6ab-dc55ad75abf6.png">

Import/Export Data: <br/>
<img width="250" alt="image" src="https://user-images.githubusercontent.com/44158648/154363350-d612375d-a503-4fc1-aac5-6a4dbda9d5d2.png"><br/>
<img width="450" alt="image" src="https://user-images.githubusercontent.com/44158648/154363678-2eaefdd1-0b35-4034-88be-9683fc2c61db.png"><br/>
<img width="350" alt="image" src="https://user-images.githubusercontent.com/44158648/154363222-f89cc790-d814-4897-a3b4-8845aa6787f9.png"><br/>

6. Connect PostreSQL Server to DBeaver

7. If you see the following error: "connect to PostgreSQL server: FATAL: no pg_hba.conf entry for host"
- Add or edit the following line in your postgresql.conf :
```diff
listen_addresses = '*'
```
- Add the following line as the first line of pg_hba.conf. It allows access to all databases for all users with an encrypted password:
```diff
# TYPE DATABASE USER CIDR-ADDRESS  METHOD
host  all  all 0.0.0.0/0 md5
```

8. 
