# SQL-PRACTICE-4-1-by-MUSKAN

create database project4
use project4

create table Employee_Detail(ID int primary key not null,First_Name varchar(20),
Last_NAme varchar(20),Salary money,Joining_Date date,Department varchar(20),Gender varchar(20))

select * from Employee_Detail
sp_help Employee_detail


insert into Employee_Detail values
(2,'vikash','ahalabat',60000,'2013-02-15','IT','Male'),
(3,'nikite','jain',53000,'2014-01-09','HR','Female'),
(4,'shweta','sharma',50000,'2013-02-15','IT','Female'),
(5,'moham','rana',60000,'2013-02-15','HR','Male'),
(6,'Raju','ram',45000,'2013-02-20','IT','Male'),
(7,'sanjeev','kumar',60000,'2013-02-15','IT','Male')


select * from Employee_Detail where First_Name like '(^a-p)%'

select * from Employee_Detail where Gender like '__le'

select * from Employee_Detail where First_Name like 'n_____'

select * from Employee_Detail where First_Name like '%'

select distinct Department from Employee_Detail

select max(salary) from Employee_Detail
select min(salary) from Employee_Detail
SELECT First_Name, GETDATE() [Current Date], Joining_Date,
DATEDIFF(DD,Joining_Date,GETDATE()) 
AS
[Total Months]
FROM
Employee_detail
select*from Employee_Detail
where datepart(yyyy,Joining_Date)='2013';
select*from  Employee_Detail
where datepart(mm,Joining_Date)='1';
select*from Employee_Detail
where Joining_Date between '2014-01-09'and '2015-03-05';
select First_Name case 
when
gender='male'then 'm'
when gender='female'then 'f' find
as
gender from  Employee_Detais
