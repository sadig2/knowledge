## ALTER TABLE employees
  ADD last_name VARCHAR(50),
      first_name VARCHAR(40);

ALTER TABLE "table_name"
RENAME COLUMN "column 1" TO "column 2";

ALTER TABLE classics ALTER COLUMN year TYPE SMALLINT;

delete from classics where author='sadig';







INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');


UPDATE Customers
SET ContactName = 'Alfred Schmidt', City= 'Frankfurt'
WHERE CustomerID = 1;



SELECT*FROM
  databaseName.INFORMATION_SCHEMA.TABLES
WHERE
  TABLE_TYPE = 'BASE TABLE';


SELECT  *FROM
  databaseName.INFORMATION_SCHEMA.TABLES
WHERE
  TABLE_SCHEMA = ‘public';

DROP TABLE IF EXISTS table1;


CREATE TABLE images (
    id                serial PRIMARY KEY,
    data              bytea,
    mime_type         varchar(255)
);
create table images(id serial primary key, front_img bytea);

