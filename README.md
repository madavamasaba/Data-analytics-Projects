# Data-analytics-Projects
/*Creating Companyy Database or schema*/
CREATE DATABASE COMPANYY;
USE COMPANYY;
/*Creating Employee table*/
CREATE TABLE Employee (emp_id int primary key , first_name varchar(20) , last_name varchar (20), sex varchar(20), Salary float ,super_id integer, branch_id integer);
describe Employee;
/*Creating Branch table*/
create table Branch (branch_id int primary key, branch_name varchar (20), mgr_id int);
describe Branch;
/*Creating Client table*/
create table Client(client_id int primary key, client_name varchar (20), branch_id int);
describe Client;
/*Creating Works_with table*/
Create table Works_with (emp_id int,Client_id int, Total_Sales int);
describe works_with;
/*Creating Branch_supplier table*/
Create table Branch_supplier (branch_id int,Supplier_name varchar (20),Supply_type varchar (20));
Describe works_with;

/*INSERTING DATA INTO THE TABLES */
/*INSERTING DATA INTO BRANCH*/


Insert into branch (branch_id, branch_name,mgr_id) values (1,"kakamega",254),(2,"Mumias",255),(3,"Nairobi",256),(4,"Kisumu",257),(5,"Bungoma",258),(6,"Kitale",259),(7,"Eldoret","260"),(8,"Nakuru",261),(9,"Naivasha",262),(10,"Mombasa",263)
/*Viewing elements in Branch table*/

select * from branch;

/*INSERTING DATA INTO BRANCH_SUPPLIER*/
Insert into branch_Supplier (branch_id, Supplier_name,Supply_type) values (1,"kenblest","Bread"),(2,"Brookside","Milk"),(3,"Tropikal","Cooking oil"),(4,"Safaricom","Scratch_cards"),(5,"Toyota","Cars"),(6,"Cocacola","Drinks"),(7,"Keringet","Drinking_water"),(8,"Gucci","Clothes"),(9,"Hilton","Hospitality"),(10,"Easy_coach","Transport")
Select*from branch_supplier;

/*INSERTING DATA INTO CLIENT*/
Insert into Client (Client_id, Client_name,branch_id) values (400,"John",1),(401,"Virginia",2),(403,"Michael",3),(404,"Simon",4),(405,"Joseph",5),(406,"Dunnet",6),(407,"Ruth",7),(408,"Sam",8),(409,"Hillary",9),(410,"Elsie",10);
select *from client;
/*INSERTING DATA INTO Employee*/

select*from employee;

/*INSERTING DATA INTO WORKS_WITH*/
Insert into Works_with (emp_id, Client_id,total_sales) values (34,400,150000),(34,403,300000),(36,404,400000),(35,405,250000),(34,408,600000),(36,410,650000),(35,407,700000),(34,410,800000),(35,403,450000),(36,402,1000000);
select*from works_with;

SELECT emp_id,first_name,last_name from employee ;

Select*from branch;
Select*from branch_supplier;
select*from client;
select*from employee;
Select*from works_with;
