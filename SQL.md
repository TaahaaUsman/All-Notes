<h1 style='color: red; text-align: center; font-size: 45px'>What is database</h1> 
Database ak asi jaga ha jahn par data within a format save kiya howa hota ha
<h2 style='color: Pink; font-size: 30px'>What is database management system?</h2>
Asa software or set of softwares wo ka database ka ander delete, update & insert operations perform karna ka liya use hota ha

<h2 style='color: aquamarine'>Types of databases</h2>

Databases ki two types hoti hain:

**Relational database**
<br>
Relational database ka ander data tables 
ki form ma store hota ha
SQL, Oracle, SQL Server, PostgreSQL

**Non Relation database**
<br>
Non relation database ka ander data tables ki form ma store nahi hota, MongoDB

<h2 style='color: aquamarine'>What is SQL</h2>
SQL stand for structured query language, and this language is used to intract with relational database. 
<br>
There are four major CRUD operations in SQL:

- Create
- Read
- Update
- Delete

<h2 style='color: aquamarine'>Installation of SQL?</h2>
Sab sa pala sql ki website par jana ha

[Dev_mySQL](https://dev.mysql.com/downloads/ 'dev.mySQL')
is link par jana ha
mySql of installer for windows par click karna ha ya download ho jaya ga
Baki installation simple ha, bass ak password set karna ha nahi to next aor execute par hi click karta jana ha

<h2 style='color: aquamarine'>Creating our first program of SQL</H2>

<h2 style='color: aqua'>Creating a Database</h2>

```
CREATE DATABASE db_name;
or
create database db_name;

<-- SQL is not case sensitive we can write commands in capital words or smaller letter words>
```
<h2 style='color: aquamarine'>Drop a database</h2> 
Means delete a database

```
DROP DATABASE db_name;
```

> yad raha ka ak bar database ban jana ka bad ham ager sara program execute karin ga to already bana howa database phir bana ga jis sa error a sakta ha, jo link bhi hama execute karni ha ham osa select kar ka siraf osa execute kar sakta hain

<h2 style='color: aquamarine'>USE command</h2>

```
USE db_name
```
_Ham use command os wakt use karta hain jab hama kisi database ka ander kam karna hota ha_

<h2 style='color: aquamarine'>CREATE TABLE command</h2>

```
create table student(
    id INT primary key,
    name varchar(50),
    age int not NULL
);
```
_Is ka ander ak table create kiya gaya ha aor os ka kuch attributes set kiya gaya hain_

<h2 style='color: aquamarine'>Insert data into table</h2>

```
insert into student values(1,"Taahaa Usman",21);
```

<h2 style='color: aquamarine'>Print all table command</h2>

```
select * from student;
```

<h2 style='color: aquamarine'>Database Data Types</h2>
![Data Types]()

- Signed dataTypes:<br>
asi datatypes jin ka ander numeric data store kiya jata ha, ager os ka ander hama koi asi value store karwani ha jis ka sath - or + ka sign hota ha to ham signed keyword use kar sakta hain
- Unsigned dataType:<br>
Is ka ander koi sign nahi hota datatype ka sath, ager ager koi signed datatype ka sath ham Unsigned lik data hain to os ki range zayada ho jati ha, jasa ka TINYINT

<h2 style='color: aquamarine'>Types of SQL Commands</h2>

- DDL: Data Defination language,
```
create, alter , rename, truncate & drop
```
- DQL: Data query language
```
select
```
- DML: Data manipulation language
```
insert , update , delete
```
- DCL: Data control language
```
grant and revoke permission to users
```
- TCL: Transaction control Language
```
start transaction, commit , rollback etc
```

<h2 style='color: aquamarine'>Database related queries</h2>
 IF NOT EXISTS & IF EXISTS:

```
CREATE DATABASE IF NOT EXISTS collage;
DROP DATABASE IF EXISTS school;
```
> Ya commands achi practice ka liya use ki jati hain.

```
SHOW DATABASES:
SHOW TABLES:
```
> In dono commands ki madat sa ham database yan tables dak sakta hian.
Show tables: command ka liya zarori ha ka ham kisi database ko use kar raha hon

<h2 style='color: aquamarine'>Table related queries</h2>

```
create table student(
    id INT primary key,
    name varchar(50),
    age int not NULL
);
```
Selecting an table:

```
select * from student;
```
> means all in student, Ham jab bhi table ka ander data insert karta hain to zarori nahi ka ham na jis tartib ka ander banaya tha os ka ander hi data inter karna ha, ham kud define bhi kar sakta hain ka kis tara ham data inter karin ga

```
insert into students 
(name, age, fathername, id, courseName) 
values ('Hazi masood', 42, 'Ali asgar', 5, 'Database Engineer');
```
> Hama har bar insert likna ki zarorat nahi ager hama kafi rows ka data save karna ha to ham ak insert li kar brackets laga kar bhi data lik sakta hain.

```
insert into students values
(1, 'Taahaa Usman', 21, 'Muhammad Anwar', 'Software Engineering'),
(2, 'Saad Ranjha', 21, 'Muhammad Anwar', 'MSC Chemistry'),
(3, 'Haider Ali', 21, 'Abu bakar Gondal', 'Matric'),
(4, 'Subhan', 21, 'Usmana', 'Software Engineering');
```

<h1 style='color: red; text-align: center; font-size: 45px'>KEYS</h1>

<h2 style='color: aquamarine'>Primary key</h2>
This is an column or set of columns that uniquely identifies each row in a table. The primary key of a table must be unique and not Null. There is only 1 primary key in an table.
<br>
Foreign key:
<br>
A foreign key is an column or set of colums that refers to primary key of another table to link the tables. There is multiple FK in an table. FKs can have multiple duplicate & null values.

<h2 style='color: aquamarine'>Constraints</h2>
SQL constraints are used to specify rules for data in a table
<br>
NOT NULL:
<br>
ager ya constraint ham ksis column ka sath use karta hain to ham osa phir NULL nahi rak sakta matlab empty nahi rak sakta 

UNIQUE:
<br>
Is constraint ka use sa ham apna column ka ander duplication nahi kar sakta
PRIMARY KEY: Ager ham kisi column ko primary key banata hain to os ma NOT NULL and UNIQUE dono rules follow hon ga,
<br>
Syntax for making primary key:
There are two types of primary keys
<br>

**code 1:**
```
create table students(
    id int primary key,
    name varchar(50),
    age int,
    fathername varchar(50),
    courseName varchar(50)
);
```
**code 2:**
```
create table students(
    id int,
    name varchar(50),
    age int,
    fathername varchar(50),
    courseName varchar(50),
    primary key (id, name)
);
```
_is oper wali code 2 ka ander two columns ka combination primary key banaya ga ha_

<h2 style='color: aquamarine'>Foreign key constraints</h2>

**code:**
```
create table teachers(
	teacher_id int,
    salary int default 30000,
    name varchar(50),
    foreign key (teacher_id) references students (id)
);
```

**Default**
is constraint ki madat sa ham kuch values by default set kar sakta hain
Check constraint:
is constraint ki madat sa ham apna attribute par condition laga sakta hain
code:
```
 age int check (age >= 18) or
 age int check (age >= 18 and age <= 30)
 ```

<h2 style='color: aquamarine'>Lecture_Sample_Database exercise</h2>

<h2 style='color: aquamarine'>Select in detail</h2>
select ham use karta hain table ka ander data ko select kar ka search karna ka liya aor view karna ka liya

```
select * from table_name:
```
> is used to select all columns in table.
code:

```
select * from students;
select city, name from students;
select distinct grade from students;
```
>distinct: ka matlab hota ha ka jo values repeat ho rahi hain on ko ak bar show karwaya jaya.
<h1 style='color: red; text-align: center; font-size: 45px'>Where clause</h1>

```
select * from students where name = "Usman";
select * from students where grade = "C" and name = "Usman";
```
_is ka ander ham condition set karta hain ka hama is type ka data chya_

<h2 style='color: aquamarine'>Operator in SQL</h2>
mana ak picture ka screenshot is folder ma banaya ha 'Operators in SQL' ka ander sara operators lika howa hain
<br>
Between operator:
<br>
ager hama limit set karni ha ka kisi khas value ka ander data chya to between use karta hain
code:

```
select * from students where Roll_no between 103 and 110;
```
In operator:
<br>
In operator ka ander ham ak list data hain aor ager data os list ka data sa math kara to sara row print kar di jati ha
code:

```
select * from students where Roll_no in (112, 115,117);
```
Not operator:
<br>
not in operator check karta ha ka jo value isa di jati ha condition ka ander di jati ha ager value wo database ka ander mili to wo data print nahi ho ga baki sara data print ho jaya ga
code:

```
select * from students where Roll_no not in (112, 115,117);
```
limit operator:
<br>
ham limit set kar sakta hain ka siraf itna rows of data hi chya
code:

```
select * from students where Roll_no = 101 limit 3;
```
order by operator:
<br>
kabi kabi hama data kisi khas order ma chya hota ha for example kabi hama high id sa low id ki taraf jana ha to os ka liya ya operator use hota ha
<br>
ASC: Assending order
<br>
DESC: Dessending order
<br>
code:

```
select * from students order by Roll_no desc;
```

<h2 style='color: aquamarine'>Aggregation functions</h2>

Aggregartion functions perform a calculation on multiple values, and return a single value. There are multiple ways to use aggregation functions but simple way is we use aggregation function with select.

```
count() function:
max() function:
sum() function:
min() function:
avg() function:
```

<h2 style='color: aquamarine'>Group by Clause</h2>

Groups rows that have the same values into summary rows.
It collect data from multiple records and groups the result by one or more column.
Code:

```
select courseName, count(id) from students group by courseName;
```

<h2 style='color: aquamarine'>Having Clause</h2>

Having clause bhi same ha where clause ki tara bass difference ki samj nahi ai lakin ma abi isa chor kar aga bar raha hon revision ma dakain ga isa
Code:

```
select marks, count(Roll_no) from students
group by marks
having max(marks) > 85;
```

<h2 style='color: aquamarine'>General order of all Clauses</h2>


```
select columns // hama kon sa colums select karna hain
from table_name // kis table sa select karna hain
where condition // On columns par kuch condition lagana ka liya
group by columns // Hama kis columns ka group banana ha
having condition // wo group ka ander koi condition matlab wo kon si conditions ko mind ma rak kar chlain ga
order by columns ASC; // hama kon sa columns ki bass par order ma lana ha data ko
```


<h1 style='color: red; text-align: center; font-size: 45px'>Table Related Queries</h1>

<h2 style='color: aquamarine'>How to off safe mode</h2>

```
set sql_safe_updates = 0; 
```
> if we again change 0 to 1 so safe mode is on again

<h2 style='color: aquamarine'>Update</h2>

```
update students set grade = "A" where grade = "C";
```

hama table ka name likana ha set ka ander wo data ho ga jo hama set karna ha aor where ka ander wo data ho ga jisa hama change karna ha

<h2 style='color: aquamarine'>DELETE</h2>

delete from tableName where condition;

is line ki madat sa ham table ka ander kisi bhi  row ko delete kar sakta hain

```
delete from tablename;
```

likna sa simple sara table bhi delete ho sakta ha.

<h2 style='color: aquamarine'>Revisiting Foriegn key</h2>


```
create table department(
	course_id int primary key,
    name varchar(50)
);
```
```
create table teachers (
	teacher_id int primary key,
    name varchar(50),
    CNIC bigint,
    departmental_id int,
    foreign key (departmental_id) references department(course_id) 
);
```

>is tara sa ham Foriegn key bana saka hain abi is ka ander ham na itna hi para ha.

<h2 style='color: aquamarine'>How to view ER Diagram in sql benchmark</h2>

setps: 
1. go to database
2. select reverse Engineer
3. Simple next next everything

<h2 style='color: aquamarine'>Cascading in foreign key</h2>

Cascadeing ka simple matlab hota ha ka ak jaga par change hona sa dosri jaga par bhi change ho jaya
is ka liya two operations hota hain:
1. on delete Cascade 
2. on update Cascade
code :

```
create table teachers (
	teacher_id int primary key,
    name varchar(50),
    CNIC bigint,
    departmental_id int,
    foreign key (departmental_id) references department(course_id)
    ON UPDATE CASCADE
    ON DELETE CASCADE
);
```
> ager hama update reflect karni ha to ham ak operation laga sakta hain ager delete karna ha to wo operation

<h2 style='color: aqua'>Alter: table related queries</h2>

is lecture ma ham 5 queries parain ga table ka related:
1. ADD column:
Alter table student
ADD column age int default 21;
<h2 style='color: aqua'>Is command sa ham new column add kar sakta hain</h2>
2. Modify column:
Alter table student
modify column age varchar(3);
<h2 style='color: aqua'>is command sa ham colum ka name aor constraints ko modify kar sakta hain</h2>
3. Change column:
Alter table student
change age students_age int;
<h2 style='color: aqua'>is command sa ham column ka name change aor datatype change kar sakta hain, rename</h2>
4. DROP column:
Alter table students
DROP column students_age;
<hr style='color: aqua'>is command ki madat sa ham column delete kar satka hain kisi table ka ander</h2>
5. Rename column:
Alter table students
rename student;
<h2 style='color: aqua'>is command sa ham kisi bhi table ko rename kar sakta hain</h2>
6. TRUNCATE TABLE:
TRUNCATE TABLE student;
truncate aor drop ma ya farak ha ka drop table ko delete kar data ha lakin truncate table ka ander data ko delete karta ha

# PRACTICE QUESTION

# join in sql

join:
    Join two or more tables ko apass ma combine karna ka liya use hota ha based on related column between them.
There are four types of joins: (ven diagram)
1-inner join
    ak database banao
    2 tables banao
    1st table courses
    2nd table teacher
    set inner join in course_id and teaching info
    # code 
    ```
    select * from teachers inner join courses on teachers.teaching_course = courses.course_id;
    ```
    folder ka ander prac_innerjoin ki detail liki hoi ha
    as:
    
2- left join
    inner aor left join ma siraf itna farak ha ka left table ka sara data ata ha aor jin data ki keys same nahi hotin wo right table ka data nahi ata
    code aor practical ka liya dakain 'prac_leftjoin.sql'
    # code 
    select * from teachers as t left join courses on t.teaching_course = courses.course_id;
3- right Join
    left aor right bilkul same hain itna farak ha ka left join ma left table ka data aor common data show hota ha right join ma right table ka data aor common data show hota ha
    # code 
    select * from teachers as t right join courses on t.teaching_course = courses.course_id;
4- full join
    Name sa hi zahir ha dono tables ka pora ka pora data a jaya ga
    lakin hama full join perform karna ka liya left join aor right join ka union lana parta ha os ka ilawa aor koi statement exist nahi karti
    # code
    select * from teachers as t right join courses on t.teaching_course = courses.course_id
    union
    select * from teachers as t left join courses on t.teaching_course = courses.course_id;

    # Some more joins 
    1- Right exclusive join
        Is ka matlab ha ka right table ka wo data jo left ma nahi ha siraf wo hama show ho jaya, ya operation ham simple right exclusive join par ak condition ki madat sa karta hain 
        # code 
        select * from courses as c left join teachers as t on c.course_id = t.teaching_course 
        where t.teaching_course is null; 

    2- Left exclusive join
        Same as Right Exclusive , for more data please visit 'Right_Exclusive_Join'
        # code 
        select * from courses as c right join teachers as t on c.course_id = t.teaching_course 
        where c.course_id is null; 

        # Note 
        left aor right exclusive join ma ak bat dayan rakna wali ha ka condition oposite table par laga gi

    3- Full Exclusive Join
        select * from courses as c right join teachers as t on c.course_id = t.teaching_course 
        where c.course_id is null
        union 
        select * from courses as c left join teachers as t on c.course_id = t.teaching_course 
        where t.teaching_course is null;

        just like full join we use 'union' 

# Self Join

This is ever simple innerjoin which is join table with itself.
    Simply when we want to join same table, means that we have a table in which name of employees is writen and also in these employees some employees are manager of other employees. In this situation if we want to check the manager of one employee. And there is no name is written in the manager_id field. so by using self join we can get the name of employees managers.

                                # UNIONS

We use unions when we need full-join. it combine the result-set of two or more tables.

how to use union:
1- every select must have same number of columns.
2- Columns must have similar data types.
3- Columns in every SELECT should be in same order.

    Syntax:

select * from a
union all
select * from b;

difference between union * union all
union all will present all duplicate values.
&
union will hide duplicate values.

for more information plz visit UNION&UNION_ALL.sql

            # SQL sub queries

We use SQL sub queries for dynamic approach fro CRUD operations. Some times a situation comes where we have to add a querie inside to another querie. So, this is the concept of sub queries.

    Syntax:

select * from a where marks > (select avg(marks) from a);

For more details kindly visit SQL_SUB_QUIERIES.sql

            # mySql views

Ham mysql views use karta hain taka ham kuch columns ko data ka ander hide kar sakain , aor os table ka ander kisi user ko siraf os ka related data dikaya jaya.

mysql is a virtual table it cannot effect the real table or column

    Syntax:

create view view1 as
select name,marks from a;

select * from view1;

# How to delete sql view

drop view1;


# what is PL-SQL?
pl_sql is procedural sql. it means we need to use programming in the sql.

# what is transaction?

It is a set of operations used to perform a logical unit of work.

# ACID Properties

# Trasaction states

There are total five states of transaction. In the first state the transaction comes in the active state. After the read/write operation it comes in second state which is partially commited state. it means that transaction is commpleted and now it is ready to commit. In third state the transaction has been commited. And in forth the resources for transaction will be free, and this state called termination. in fifth state Trasaction will be failed or successed. If failed so transaction will be killed and go to the start position.

# what is schedule

Schedule is a sequence of multiple executions.

There are two types of schedules.
1- Serial schedule 
    In serial schedule there is only one transaction will be occur. other transactions gone to the waiting state. Benifts of serial schedule is that there is consistancy in the database.
2- Parallel schedule
    In Parallel schedule there are numbers of transaction can be executed in the same time. It is less time consuming then serial schedule. Modren databases are working on the parallel schedule.
Disadvantages of parallel schedule:
1- Dirty read uncommited problem or write after read problem 
2- Incorrect summary
3- Lost update
4- Unrepeatable Read
5- Phantom Read
For more details kindly visit a very little video of gate smasher:
https://www.youtube.com/watch?v=oP8yLMjmszE&list=PLxCzCOWd7aiFAN6I8CuViBuCdJgiOkT2Y&index=78

There are many ways to adjust the Disadvantages of the parallel schedule:
1- cascading schedule
2- cascadless schedule
    There is an problem in the cascadless schedule we cannot read the Trasaction but we can write the trasaction and this ma cause concurrency.
3- strict recoverable

# what is serializability?

Converting parallel schedule into serial schedule is called serializability. The method is that:
We have a parallel schedule, so we have to find a clone of it. And the clone will be serial schedule. In the simple words Converting parallel schedule into serial schedule is called serializability.

# What are equivalent schedule?

If two schedule produce same result after their execution are called equivalent schedule.

# What is indexing?

Indexing is used to index the data into hard disk , if we not index the data so data retrival time will be increased.

# Indexing types?

1- Primary 
2- Clustered
3- Secondary


# What is PL-SQL?










    


