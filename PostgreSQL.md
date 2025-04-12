# PostgreSQL Command Reference

## Database Operations

### CREATE DATABASE dbname;
- Create new database

### \c dbname
- Connect to database

### DROP DATABASE dbname;
- Delete database

### \l
- List all databases

## Table Operations

### Create/Modify Tables

### CREATE TABLE tablename (col1 datatype, col2 datatype);
- Create basic table

### CREATE TABLE tablename (id SERIAL PRIMARY KEY, name VARCHAR(50));
- With auto-increment primary key

### ALTER TABLE tablename ADD COLUMN newcol datatype;
- Add new column

### ALTER TABLE tablename DROP COLUMN colname;
- Remove column

### ALTER TABLE tablename ALTER COLUMN colname TYPE newtype;
- Change column data type

### DROP TABLE tablename;
- Delete table

### TRUNCATE TABLE tablename;
- Remove all rows but keep table

### ALTER TABLE tablename RENAME TO newname;
- Rename table

## View Table Structure

### \d tablename
- Show table structure

### \dt
- List all tables in current database

## Data Querying

### Basic Queries

### SELECT * FROM tablename;
- Select all data

### SELECT col1, col2 FROM tablename;
- Select specific columns

### SELECT DISTINCT col1 FROM tablename;
- Get unique values

### SELECT COUNT(*) FROM tablename;
- Count rows

### Filtering Data

### SELECT * FROM tablename WHERE condition;
- Filter rows

### SELECT * FROM tablename WHERE col1 = 'value';
- Exact match

### SELECT * FROM tablename WHERE col1 LIKE 'A%';
- Pattern matching

### SELECT * FROM tablename WHERE col1 IN (1,2,3);
- Multiple values

### SELECT * FROM tablename WHERE col1 BETWEEN 10 AND 20;
- Range filter

### SELECT * FROM tablename WHERE col1 IS NULL;
- Null values

## Data Modification

### Inserting Data

### INSERT INTO tablename VALUES (val1, val2);
- Insert all columns

### INSERT INTO tablename (col1,col2) VALUES (val1,val2);
- Insert specific columns

### INSERT INTO tablename SELECT * FROM othertable;
- Copy data from another table

### Updating Data

### UPDATE tablename SET col1 = value WHERE condition;
- Basic update

### UPDATE tablename SET col1 = col1 + 1 WHERE id = 5;
- Increment value

### Deleting Data

### DELETE FROM tablename WHERE condition;
- Delete specific rows

### DELETE FROM tablename;
- Delete all rows (caution!)

## Advanced Features

### Indexes

### CREATE INDEX idx_name ON tablename(colname);
- Create index

### DROP INDEX idx_name;
- Remove index

### Views

### CREATE VIEW viewname AS SELECT col1,col2 FROM tablename;
- Create view

### DROP VIEW viewname;
- Remove view

### Transactions

### BEGIN;
- Start transaction

### COMMIT;
- Commit transaction

### ROLLBACK;
- Rollback transaction

## Utility Commands

### \?
- Show psql help

### \timing
- Toggle command timing

### \x
- Toggle expanded output

### EXPLAIN SELECT...;
- Show query execution plan

