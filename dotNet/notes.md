# .Net waali cheezein   

**C#**
- C sharp is a modern object origented programming language build by microsoft and it is used to build web apps, mobile applications, games(2d,3d), cloud applications etc.

- Provides workign with classes, interfaces and inheritance.

- Asynchronous nature uses async await.

- Linq (language integrated querying) for querying data from databases or collections.

**ASP.NET web api**
- A framework for building RESTful api web services using .net. It enables communication between client and server.

- It provides basic of http methods ['get', 'post', 'update' ,'delete']

- It provides routing such as ["Route", "HttpGet", etc].

- JSON serialization and deserialization.

- Provides Middleware support and filters for exception handeling.

- Securing APIs with jwt.


**Entity framework**

- An object-relation mapper (ORM) which simplifies queirying with databse operations by allowing developers to work with database data as .net objects.

- Code first and Database first approach.

- Wring Linq queries for CRUD operations.

- Migration to update the database schema.

- Lazy loading and eager loading for handling realted data.


**SQL server**
- A realtional database managment system (RDBMS) by microsoft used to sore and retrive dcata. 

- Writing sql queries: SELECT, INSERT,UPDATE, DELETE.

- Joins(inner, left, right, full).

- Indexing and performance optimization. 

- Stored procedures and Triggers. 

- Database design and normalization.



# SQL queries


Basic SQL Queries
Select all data from a table:

  sql
  Copy code
  SELECT * FROM table_name;
Select specific columns from a table:

  sql
  Copy code
  SELECT column1, column2 FROM table_name;
Count the number of rows in a table:

  sql
  Copy code
  SELECT COUNT(*) FROM table_name;
Filter data with a WHERE clause:

  sql
  Copy code
  SELECT * FROM table_name WHERE column_name = 'value';
Use logical operators (AND, OR):

  sql
  Copy code
  SELECT * FROM table_name WHERE column1 = 'value1' AND column2 = 'value2';
Order results by a specific column:

  sql
  Copy code
  SELECT * FROM table_name ORDER BY column_name DESC;
Limit the number of rows returned:

  sql
  Copy code
  SELECT * FROM table_name LIMIT 5;

Aggregate Functions
Find the sum of a column:

  sql
  Copy code
  SELECT SUM(column_name) FROM table_name;
Find the average of a column:

  sql
  Copy code
  SELECT AVG(column_name) FROM table_name;
Find the maximum and minimum values of a column:

  sql
  Copy code
  SELECT MAX(column_name), MIN(column_name) FROM table_name;
Group results by a column:

  sql
  Copy code
  SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name;
Having clause with GROUP BY:

  sql
  Copy code
  SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name HAVING COUNT(*) > 10;

JOIN Operations
INNER JOIN (Returns only matched rows):

  sql
  Copy code
  SELECT * FROM table1 t1
INNER JOIN table2 t2 ON t1.column_name = t2.column_name;
LEFT JOIN (Returns all rows from the left table and matched rows from the right table):

  sql
  Copy code
  SELECT * FROM table1 t1
LEFT JOIN table2 t2 ON t1.column_name = t2.column_name;
RIGHT JOIN (Returns all rows from the right table and matched rows from the left table):

  sql
  Copy code
  SELECT * FROM table1 t1
RIGHT JOIN table2 t2 ON t1.column_name = t2.column_name;
FULL OUTER JOIN (Returns rows when there is a match in either left or right table):

  sql
  Copy code
  SELECT * FROM table1 t1
FULL OUTER JOIN table2 t2 ON t1.column_name = t2.column_name;
Self Join (Join the table with itself):

  sql
  Copy code
  SELECT t1.column_name, t2.column_name
FROM table_name t1, table_name t2
WHERE t1.column_name = t2.column_name;

# 4. Subqueries
Subquery in SELECT:

  sql
  Copy code
  SELECT column_name,
       (SELECT COUNT(*) FROM table2 WHERE table2.column_name = table1.column_name) AS count_value
FROM table1;
Subquery in WHERE:

  sql
  Copy code
  SELECT * FROM table_name
WHERE column_name = (SELECT MAX(column_name) FROM table_name);
Correlated Subquery (Subquery depends on the outer query):

  sql
  Copy code
  SELECT * FROM table1 t1
WHERE EXISTS (SELECT 1 FROM table2 t2 WHERE t1.column_name = t2.column_name);

# 5. Data Modification Queries
INSERT data into a table:

  sql
  Copy code
  INSERT INTO table_name (column1, column2) 
VALUES ('value1', 'value2');
UPDATE existing data in a table:

  sql
  Copy code
  UPDATE table_name 
SET column1 = 'new_value'
WHERE column2 = 'value';
DELETE data from a table:

  sql
  Copy code
  DELETE FROM table_name WHERE column_name = 'value';
TRUNCATE table (Removes all rows, but does not log individual row deletions):

  sql
  Copy code
  TRUNCATE TABLE table_name;
# 6. Indexes and Constraints
Create an index on a column:

  sql
  Copy code
  CREATE INDEX idx_column_name ON table_name (column_name);
  Add a primary key constraint:

  sql
  Copy code
  ALTER TABLE table_name ADD CONSTRAINT pk_constraint PRIMARY KEY (column_name);
  Add a foreign key constraint:

  sql
  Copy code
  ALTER TABLE table_name
  ADD CONSTRAINT fk_constraint FOREIGN KEY (column_name)
  REFERENCES another_table(column_name);
 
# 7. Normalization and Denormalization
Normalize a table:
First Normal Form (1NF), Second Normal Form (2NF), and Third Normal Form (3NF) focus on ensuring that the database schema is optimized to avoid redundancy and dependency issues.
8. Advanced Queries
Window Functions (e.g., ROW_NUMBER, RANK):

  sql
  Copy code
  SELECT column1, column2, ROW_NUMBER() OVER (PARTITION BY column1 ORDER BY column2 DESC) AS row_num
  FROM table_name;
  Case Statements (Conditional logic inside queries):

  sql
  Copy code
  SELECT column1, 
        CASE 
            WHEN column2 > 10 THEN 'High'
           ELSE 'Low'
       END AS status
FROM table_name;

# 9. Transactions
Start a transaction:

  sql
  Copy code
  BEGIN TRANSACTION;
  Commit a transaction:

  sql
  Copy code
  COMMIT;
  Rollback a transaction:

  sql
  Copy code
  ROLLBACK;

# 10. Backup and Restore
  Backup a database:

  sql
  Copy code
  BACKUP DATABASE database_name TO DISK = 'path_to_backup_file';
  Restore a database:

  sql
  Copy code
  RESTORE DATABASE database_name FROM DISK = 'path_to_backup_file';



# Question that might be asked 

C# Programming Questions
What are the key features of C#?

Object-oriented programming (OOP)
Strongly-typed language
Automatic garbage collection
Type safety
Exception handling
Delegates and events
LINQ (Language Integrated Query)
Explain OOP concepts: Inheritance, Polymorphism, Encapsulation.

Inheritance: One class (child) inherits the properties and behavior of another class (parent).
Example:
csharp
Copy code
class Parent { public void Show() => Console.WriteLine("Parent"); }
class Child : Parent { }  
Polymorphism: Ability to take multiple forms. It is achieved through method overriding or interfaces.
Example:
csharp
Copy code
public virtual void Display() { Console.WriteLine("Base"); }
public override void Display() { Console.WriteLine("Derived"); }
Encapsulation: Wrapping data (fields) and methods into a single unit (class) and restricting access using access modifiers (private, public, etc.).
Difference between const, readonly, and static:

const: Compile-time constant; value cannot change.
readonly: Value can be assigned at runtime but only once (e.g., in a constructor).
static: Belongs to the class, not an instance.
What is garbage collection in C#?

Automatic memory management that reclaims unused objects to free memory.
GC Methods: GC.Collect() forces garbage collection.
What are delegates and events?

Delegate: A reference type that holds a reference to a method.
Example:
csharp
Copy code
delegate void MyDelegate(string message);
MyDelegate del = Console.WriteLine;
del("Hello");
Events: Special delegates used for notification.
Example:
csharp
Copy code
public event MyDelegate MyEvent;
ASP.NET Questions
What is ASP.NET?

A web development framework by Microsoft for building dynamic web applications and APIs.
What is the Page Life Cycle in ASP.NET?

Stages: Initialization → Load → Postback Events → Rendering → Unload.
Explain MVC architecture.

Model: Represents data and business logic.
View: Represents the user interface (HTML).
Controller: Handles user requests, updates the model, and renders the view.
Difference between GET and POST methods:

GET: Retrieves data; data is visible in the URL.
POST: Sends data securely; data is not visible in the URL.
What is routing in ASP.NET MVC?

Maps incoming URLs to controller actions.
Example:
csharp
Copy code
routes.MapRoute("Default", "{controller}/{action}/{id}");
Entity Framework Questions
What is Entity Framework?

An ORM (Object Relational Mapping) tool that allows developers to interact with a database using C# objects.
Difference between Code First and Database First:

Code First: Write classes first; database is generated automatically.
Database First: Start with an existing database; generate classes from the database schema.
What is DbContext?

It is the bridge between your entity classes and the database.
Example:
csharp
Copy code
public class MyDbContext : DbContext  
{  
    public DbSet<Student> Students { get; set; }  
}  
Difference between Lazy Loading and Eager Loading:

Lazy Loading: Loads related data on demand.
Eager Loading: Loads related data immediately with the query.
Example:
csharp
Copy code
var students = context.Students.Include(s => s.Courses).ToList();
What is LINQ?

LINQ (Language Integrated Query) allows querying collections and databases using C#.
Example:
csharp
Copy code
var result = dbContext.Students.Where(s => s.Age > 20).ToList();
SQL Server Questions
What is a primary key and a foreign key?

Primary Key: Uniquely identifies each row in a table.
Foreign Key: A reference to a primary key in another table to establish a relationship.
Explain joins and their types:

INNER JOIN: Returns matching rows from both tables.
sql
Copy code
SELECT * FROM TableA INNER JOIN TableB ON TableA.ID = TableB.ID;
LEFT JOIN: Returns all rows from the left table and matching rows from the right table.
RIGHT JOIN: Returns all rows from the right table.
FULL JOIN: Returns rows when there is a match in either table.
What is a stored procedure?

A precompiled SQL query stored in the database for reuse.
Example:
sql
Copy code
CREATE PROCEDURE GetStudents AS SELECT * FROM Students;
How to find duplicate records in a table?

sql
Copy code
SELECT Name, COUNT(*)  
FROM TableName  
GROUP BY Name  
HAVING COUNT(*) > 1;
Query to find the second highest salary:

sql
Copy code
SELECT MAX(Salary) AS SecondHighest  
FROM Employees  
WHERE Salary < (SELECT MAX(Salary) FROM Employees);
Final Tips:
Practice coding small programs and SQL queries.
Be clear and confident in your explanations.
When asked group questions, listen to others, provide precise answers, and engage respectfully.
Let me know if you want detailed code examples for any specific area! 🚀










Here are the answers to the common questions you might face in the interview for C#, ASP.NET, Entity Framework, and SQL Server:

C# Programming Questions
What are the key features of C#?

Object-oriented programming (OOP)
Strongly-typed language
Automatic garbage collection
Type safety
Exception handling
Delegates and events
LINQ (Language Integrated Query)
Explain OOP concepts: Inheritance, Polymorphism, Encapsulation.

Inheritance: One class (child) inherits the properties and behavior of another class (parent).
Example:
csharp
Copy code
class Parent { public void Show() => Console.WriteLine("Parent"); }
class Child : Parent { }  
Polymorphism: Ability to take multiple forms. It is achieved through method overriding or interfaces.
Example:
csharp
Copy code
public virtual void Display() { Console.WriteLine("Base"); }
public override void Display() { Console.WriteLine("Derived"); }
Encapsulation: Wrapping data (fields) and methods into a single unit (class) and restricting access using access modifiers (private, public, etc.).
Difference between const, readonly, and static:

const: Compile-time constant; value cannot change.
readonly: Value can be assigned at runtime but only once (e.g., in a constructor).
static: Belongs to the class, not an instance.
What is garbage collection in C#?

Automatic memory management that reclaims unused objects to free memory.
GC Methods: GC.Collect() forces garbage collection.
What are delegates and events?

Delegate: A reference type that holds a reference to a method.
Example:
csharp
Copy code
delegate void MyDelegate(string message);
MyDelegate del = Console.WriteLine;
del("Hello");
Events: Special delegates used for notification.
Example:
csharp
Copy code
public event MyDelegate MyEvent;
ASP.NET Questions
What is ASP.NET?

A web development framework by Microsoft for building dynamic web applications and APIs.
What is the Page Life Cycle in ASP.NET?

Stages: Initialization → Load → Postback Events → Rendering → Unload.
Explain MVC architecture.

Model: Represents data and business logic.
View: Represents the user interface (HTML).
Controller: Handles user requests, updates the model, and renders the view.
Difference between GET and POST methods:

GET: Retrieves data; data is visible in the URL.
POST: Sends data securely; data is not visible in the URL.
What is routing in ASP.NET MVC?

Maps incoming URLs to controller actions.
Example:
csharp
Copy code
routes.MapRoute("Default", "{controller}/{action}/{id}");
Entity Framework Questions
What is Entity Framework?

An ORM (Object Relational Mapping) tool that allows developers to interact with a database using C# objects.
Difference between Code First and Database First:

Code First: Write classes first; database is generated automatically.
Database First: Start with an existing database; generate classes from the database schema.
What is DbContext?

It is the bridge between your entity classes and the database.
Example:
csharp
Copy code
public class MyDbContext : DbContext  
{  
    public DbSet<Student> Students { get; set; }  
}  
Difference between Lazy Loading and Eager Loading:

Lazy Loading: Loads related data on demand.
Eager Loading: Loads related data immediately with the query.
Example:
csharp
Copy code
var students = context.Students.Include(s => s.Courses).ToList();
What is LINQ?

LINQ (Language Integrated Query) allows querying collections and databases using C#.
Example:
csharp
Copy code
var result = dbContext.Students.Where(s => s.Age > 20).ToList();
SQL Server Questions
What is a primary key and a foreign key?

Primary Key: Uniquely identifies each row in a table.
Foreign Key: A reference to a primary key in another table to establish a relationship.
Explain joins and their types:

INNER JOIN: Returns matching rows from both tables.
sql
Copy code
SELECT * FROM TableA INNER JOIN TableB ON TableA.ID = TableB.ID;
LEFT JOIN: Returns all rows from the left table and matching rows from the right table.
RIGHT JOIN: Returns all rows from the right table.
FULL JOIN: Returns rows when there is a match in either table.
What is a stored procedure?

A precompiled SQL query stored in the database for reuse.
Example:
sql
Copy code
CREATE PROCEDURE GetStudents AS SELECT * FROM Students;
How to find duplicate records in a table?

sql
Copy code
SELECT Name, COUNT(*)  
FROM TableName  
GROUP BY Name  
HAVING COUNT(*) > 1;
Query to find the second highest salary:

sql
Copy code
SELECT MAX(Salary) AS SecondHighest  
FROM Employees  
WHERE Salary < (SELECT MAX(Salary) FROM Employees);
Final Tips:
Practice coding small programs and SQL queries.
Be clear and confident in your explanations.
When asked group questions, listen to others, provide precise answers, and engage respectfully.
Let me know if you want detailed code examples for any specific area! 🚀






Here are the answers to the common questions you might face in the interview for C#, ASP.NET, Entity Framework, and SQL Server:

C# Programming Questions
What are the key features of C#?

Object-oriented programming (OOP)
Strongly-typed language
Automatic garbage collection
Type safety
Exception handling
Delegates and events
LINQ (Language Integrated Query)
Explain OOP concepts: Inheritance, Polymorphism, Encapsulation.

Inheritance: One class (child) inherits the properties and behavior of another class (parent).
Example:
csharp
Copy code
class Parent { public void Show() => Console.WriteLine("Parent"); }
class Child : Parent { }  
Polymorphism: Ability to take multiple forms. It is achieved through method overriding or interfaces.
Example:
csharp
Copy code
public virtual void Display() { Console.WriteLine("Base"); }
public override void Display() { Console.WriteLine("Derived"); }
Encapsulation: Wrapping data (fields) and methods into a single unit (class) and restricting access using access modifiers (private, public, etc.).
Difference between const, readonly, and static:

const: Compile-time constant; value cannot change.
readonly: Value can be assigned at runtime but only once (e.g., in a constructor).
static: Belongs to the class, not an instance.
What is garbage collection in C#?

Automatic memory management that reclaims unused objects to free memory.
GC Methods: GC.Collect() forces garbage collection.
What are delegates and events?

Delegate: A reference type that holds a reference to a method.
Example:
csharp
Copy code
delegate void MyDelegate(string message);
MyDelegate del = Console.WriteLine;
del("Hello");
Events: Special delegates used for notification.
Example:
csharp
Copy code
public event MyDelegate MyEvent;
ASP.NET Questions
What is ASP.NET?

A web development framework by Microsoft for building dynamic web applications and APIs.
What is the Page Life Cycle in ASP.NET?

Stages: Initialization → Load → Postback Events → Rendering → Unload.
Explain MVC architecture.

Model: Represents data and business logic.
View: Represents the user interface (HTML).
Controller: Handles user requests, updates the model, and renders the view.
Difference between GET and POST methods:

GET: Retrieves data; data is visible in the URL.
POST: Sends data securely; data is not visible in the URL.
What is routing in ASP.NET MVC?

Maps incoming URLs to controller actions.
Example:
csharp
Copy code
routes.MapRoute("Default", "{controller}/{action}/{id}");
Entity Framework Questions
What is Entity Framework?

An ORM (Object Relational Mapping) tool that allows developers to interact with a database using C# objects.
Difference between Code First and Database First:

Code First: Write classes first; database is generated automatically.
Database First: Start with an existing database; generate classes from the database schema.
What is DbContext?

It is the bridge between your entity classes and the database.
Example:
csharp
Copy code
public class MyDbContext : DbContext  
{  
    public DbSet<Student> Students { get; set; }  
}  
Difference between Lazy Loading and Eager Loading:

Lazy Loading: Loads related data on demand.
Eager Loading: Loads related data immediately with the query.
Example:
csharp
Copy code
var students = context.Students.Include(s => s.Courses).ToList();
What is LINQ?

LINQ (Language Integrated Query) allows querying collections and databases using C#.
Example:
csharp
Copy code
var result = dbContext.Students.Where(s => s.Age > 20).ToList();
SQL Server Questions
What is a primary key and a foreign key?

Primary Key: Uniquely identifies each row in a table.
Foreign Key: A reference to a primary key in another table to establish a relationship.
Explain joins and their types:

INNER JOIN: Returns matching rows from both tables.
sql
Copy code
SELECT * FROM TableA INNER JOIN TableB ON TableA.ID = TableB.ID;
LEFT JOIN: Returns all rows from the left table and matching rows from the right table.
RIGHT JOIN: Returns all rows from the right table.
FULL JOIN: Returns rows when there is a match in either table.
What is a stored procedure?

A precompiled SQL query stored in the database for reuse.
Example:
sql
Copy code
CREATE PROCEDURE GetStudents AS SELECT * FROM Students;
How to find duplicate records in a table?

sql
Copy code
SELECT Name, COUNT(*)  
FROM TableName  
GROUP BY Name  
HAVING COUNT(*) > 1;
Query to find the second highest salary:

sql
Copy code
SELECT MAX(Salary) AS SecondHighest  
FROM Employees  
WHERE Salary < (SELECT MAX(Salary) FROM Employees);
Final Tips:
Practice coding small programs and SQL queries.
Be clear and confident in your explanations.
When asked group questions, listen to others, provide precise answers, and engage respectfully.
Let me know if you want detailed code examples for any specific area! 🚀






Here are the answers to the common questions you might face in the interview for C#, ASP.NET, Entity Framework, and SQL Server:

C# Programming Questions
What are the key features of C#?

Object-oriented programming (OOP)
Strongly-typed language
Automatic garbage collection
Type safety
Exception handling
Delegates and events
LINQ (Language Integrated Query)
Explain OOP concepts: Inheritance, Polymorphism, Encapsulation.

Inheritance: One class (child) inherits the properties and behavior of another class (parent).
Example:
csharp
Copy code
class Parent { public void Show() => Console.WriteLine("Parent"); }
class Child : Parent { }  
Polymorphism: Ability to take multiple forms. It is achieved through method overriding or interfaces.
Example:
csharp
Copy code
public virtual void Display() { Console.WriteLine("Base"); }
public override void Display() { Console.WriteLine("Derived"); }
Encapsulation: Wrapping data (fields) and methods into a single unit (class) and restricting access using access modifiers (private, public, etc.).
Difference between const, readonly, and static:

const: Compile-time constant; value cannot change.
readonly: Value can be assigned at runtime but only once (e.g., in a constructor).
static: Belongs to the class, not an instance.
What is garbage collection in C#?

Automatic memory management that reclaims unused objects to free memory.
GC Methods: GC.Collect() forces garbage collection.
What are delegates and events?

Delegate: A reference type that holds a reference to a method.
Example:
csharp
Copy code
delegate void MyDelegate(string message);
MyDelegate del = Console.WriteLine;
del("Hello");
Events: Special delegates used for notification.
Example:
csharp
Copy code
public event MyDelegate MyEvent;
ASP.NET Questions
What is ASP.NET?

A web development framework by Microsoft for building dynamic web applications and APIs.
What is the Page Life Cycle in ASP.NET?

Stages: Initialization → Load → Postback Events → Rendering → Unload.
Explain MVC architecture.

Model: Represents data and business logic.
View: Represents the user interface (HTML).
Controller: Handles user requests, updates the model, and renders the view.
Difference between GET and POST methods:

GET: Retrieves data; data is visible in the URL.
POST: Sends data securely; data is not visible in the URL.
What is routing in ASP.NET MVC?

Maps incoming URLs to controller actions.
Example:
csharp
Copy code
routes.MapRoute("Default", "{controller}/{action}/{id}");
Entity Framework Questions
What is Entity Framework?

An ORM (Object Relational Mapping) tool that allows developers to interact with a database using C# objects.
Difference between Code First and Database First:

Code First: Write classes first; database is generated automatically.
Database First: Start with an existing database; generate classes from the database schema.
What is DbContext?

It is the bridge between your entity classes and the database.
Example:
csharp
Copy code
public class MyDbContext : DbContext  
{  
    public DbSet<Student> Students { get; set; }  
}  
Difference between Lazy Loading and Eager Loading:

Lazy Loading: Loads related data on demand.
Eager Loading: Loads related data immediately with the query.
Example:
csharp
Copy code
var students = context.Students.Include(s => s.Courses).ToList();
What is LINQ?

LINQ (Language Integrated Query) allows querying collections and databases using C#.
Example:
csharp
Copy code
var result = dbContext.Students.Where(s => s.Age > 20).ToList();
SQL Server Questions
What is a primary key and a foreign key?

Primary Key: Uniquely identifies each row in a table.
Foreign Key: A reference to a primary key in another table to establish a relationship.
Explain joins and their types:

INNER JOIN: Returns matching rows from both tables.
sql
Copy code
SELECT * FROM TableA INNER JOIN TableB ON TableA.ID = TableB.ID;
LEFT JOIN: Returns all rows from the left table and matching rows from the right table.
RIGHT JOIN: Returns all rows from the right table.
FULL JOIN: Returns rows when there is a match in either table.
What is a stored procedure?

A precompiled SQL query stored in the database for reuse.
Example:
sql
Copy code
CREATE PROCEDURE GetStudents AS SELECT * FROM Students;
How to find duplicate records in a table?

sql
Copy code
SELECT Name, COUNT(*)  
FROM TableName  
GROUP BY Name  
HAVING COUNT(*) > 1;
Query to find the second highest salary:

sql
Copy code
SELECT MAX(Salary) AS SecondHighest  
FROM Employees  
WHERE Salary < (SELECT MAX(Salary) FROM Employees);
Final Tips:
Practice coding small programs and SQL queries.
Be clear and confident in your explanations.
When asked group questions, listen to others, provide precise answers, and engage respectfully.
Let me know if you want detailed code examples for any specific area! 🚀






Here are the answers to the common questions you might face in the interview for C#, ASP.NET, Entity Framework, and SQL Server:

C# Programming Questions
What are the key features of C#?

Object-oriented programming (OOP)
Strongly-typed language
Automatic garbage collection
Type safety
Exception handling
Delegates and events
LINQ (Language Integrated Query)
Explain OOP concepts: Inheritance, Polymorphism, Encapsulation.

Inheritance: One class (child) inherits the properties and behavior of another class (parent).
Example:
csharp
Copy code
class Parent { public void Show() => Console.WriteLine("Parent"); }
class Child : Parent { }  
Polymorphism: Ability to take multiple forms. It is achieved through method overriding or interfaces.
Example:
csharp
Copy code
public virtual void Display() { Console.WriteLine("Base"); }
public override void Display() { Console.WriteLine("Derived"); }
Encapsulation: Wrapping data (fields) and methods into a single unit (class) and restricting access using access modifiers (private, public, etc.).
Difference between const, readonly, and static:

const: Compile-time constant; value cannot change.
readonly: Value can be assigned at runtime but only once (e.g., in a constructor).
static: Belongs to the class, not an instance.
What is garbage collection in C#?

Automatic memory management that reclaims unused objects to free memory.
GC Methods: GC.Collect() forces garbage collection.
What are delegates and events?

Delegate: A reference type that holds a reference to a method.
Example:
csharp
Copy code
delegate void MyDelegate(string message);
MyDelegate del = Console.WriteLine;
del("Hello");
Events: Special delegates used for notification.
Example:
csharp
Copy code
public event MyDelegate MyEvent;
ASP.NET Questions
What is ASP.NET?

A web development framework by Microsoft for building dynamic web applications and APIs.
What is the Page Life Cycle in ASP.NET?

Stages: Initialization → Load → Postback Events → Rendering → Unload.
Explain MVC architecture.

Model: Represents data and business logic.
View: Represents the user interface (HTML).
Controller: Handles user requests, updates the model, and renders the view.
Difference between GET and POST methods:

GET: Retrieves data; data is visible in the URL.
POST: Sends data securely; data is not visible in the URL.
What is routing in ASP.NET MVC?

Maps incoming URLs to controller actions.
Example:
csharp
Copy code
routes.MapRoute("Default", "{controller}/{action}/{id}");
Entity Framework Questions
What is Entity Framework?

An ORM (Object Relational Mapping) tool that allows developers to interact with a database using C# objects.
Difference between Code First and Database First:

Code First: Write classes first; database is generated automatically.
Database First: Start with an existing database; generate classes from the database schema.
What is DbContext?

It is the bridge between your entity classes and the database.
Example:
csharp
Copy code
public class MyDbContext : DbContext  
{  
    public DbSet<Student> Students { get; set; }  
}  
Difference between Lazy Loading and Eager Loading:

Lazy Loading: Loads related data on demand.
Eager Loading: Loads related data immediately with the query.
Example:
csharp
Copy code
var students = context.Students.Include(s => s.Courses).ToList();
What is LINQ?

LINQ (Language Integrated Query) allows querying collections and databases using C#.
Example:
csharp
Copy code
var result = dbContext.Students.Where(s => s.Age > 20).ToList();
SQL Server Questions
What is a primary key and a foreign key?

Primary Key: Uniquely identifies each row in a table.
Foreign Key: A reference to a primary key in another table to establish a relationship.
Explain joins and their types:

INNER JOIN: Returns matching rows from both tables.
sql
Copy code
SELECT * FROM TableA INNER JOIN TableB ON TableA.ID = TableB.ID;
LEFT JOIN: Returns all rows from the left table and matching rows from the right table.
RIGHT JOIN: Returns all rows from the right table.
FULL JOIN: Returns rows when there is a match in either table.
What is a stored procedure?

A precompiled SQL query stored in the database for reuse.
Example:
sql
Copy code
CREATE PROCEDURE GetStudents AS SELECT * FROM Students;
How to find duplicate records in a table?

sql
Copy code
SELECT Name, COUNT(*)  
FROM TableName  
GROUP BY Name  
HAVING COUNT(*) > 1;
Query to find the second highest salary:

sql
Copy code
SELECT MAX(Salary) AS SecondHighest  
FROM Employees  
WHERE Salary < (SELECT MAX(Salary) FROM Employees);
Final Tips:
Practice coding small programs and SQL queries.
Be clear and confident in your explanations.
When asked group questions, listen to others, provide precise answers, and engage respectfully.
Let me know if you want detailed code examples for any specific area! 🚀






