# Bank-Management
Database Project 

## Installation process
> Download the ([Oracle Database 11g Express Edition](https://www.oracle.com/database/technologies/xe-prior-release-downloads.html)) and install the software.
> Remember the password during the installation because this password is used for connecting the database account.

![alt text](https://github.com/shahidul034/BookList_database-project/blob/master/DIAGRAM%20PIC/installation.png)

> Open the SQL Plus. Write 'connect system' and use the password that you set in the installation process. Follow the below figure.

![alt text](https://github.com/shahidul034/Database-Lab-Tutorial/blob/main/DIAGRAM%20PIC/sqlplus.png)

> You can create a new user because we use the system(administrator) as a user. Then, we will give the new user all privileges to perform all SQL tasks. Follow the figure.
> Change the password of the admin(system)
```
connect / as sysdba
alter user system identified by [password]
```

## Creating user and giving system privileges
```
create user tamim identified by 123;
```
>  Granting system privileges
> Here, we give all the privileges to the user.
```
grant all privileges to tamim;
```
> Reboke all the privileges from the user
```
revoke all privileges from user_name
```
![alt text](https://github.com/shahidul034/Database-Lab-Tutorial/blob/main/DIAGRAM%20PIC/sqlplus2.png)
> We can give specific privileges to the user.
```
grant create session to shakib034;
```
> Creating a role(Assigned system privileges)
```
create role cse2k15;
grant create table, create session to cse2k15;
grant cse2k15 to shakib034;
```
> Revoking System Privileges
```
revoke create table from shakib034;
```

![alt text](https://github.com/shahidul034/Database-Lab-Tutorial/blob/main/DIAGRAM%20PIC/system%20privileges.png)
## Set line size and page size
```
show pagesize
show linesize
```
```
set pagesize 100
set linesize 500
```
