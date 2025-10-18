# List (لیست)

### [1. Introduction (مقدمه)](#Introduction-مقدمه)
- Data Base
- SQL
- Types of Commands
- Data
- Information
### [2. Data Definition Language (دستورات تعریف داده)](#Data-Definition-Language-زبان-تعریف-داده)
- Data Type 
- Limitation
- Feature
- Data Base
- Table
### [3. Data Manipulation Language (دستورات مدیریت داده)](#Data-Manipulation-Language-دستورات-مدیریت-داده)
- Value
- Select
- Update
- Delete
### [4. Functions And Operators (توابع و عملگرها)](#Functions-and-Operators-توابع-و-عملگرها)
### [5. Joins (روابط بین جدول‌ها)](#Joins-روابط-بین-جدول‌ها)
### [6. Online SQL compiler (کامپایلر آنلاین زبان پرس‌ و جوی ساختار یافته)](#Online-SQL-compiler-کامپایلر-آنلاین-زبان-پرس‌-و-جوی-ساختار-یافته)
- Online SQL compiler

---
<br>

# Introduction (مقدمه)

### 1. Data Base (دیتا بیس):
It is a structured collection of data used to store and manage information (مجموعه‌ای ساختارمند از داده‌هاست که برای ذخیره و مدیریت اطلاعات استفاده می‌شود).

### 2. SQL (زبان پرس‌ و جوی ساختار یافته):
It is a standard language for creating, reading, and editing data in relational databases (زبان استانداردی برای ایجاد، خواندن، و ویرایش داده‌ها در پایگاه‌داده‌های رابطه‌ای است).

### 3. Types Of Commands (انواع نوع دستورات)
- DDL: Used to create, modify, or delete database structure (برای ایجاد، تغییر یا حذف ساختار پایگاه‌داده استفاده می‌شود).
- DML: It is used to manage data within tables (برای مدیریت داده‌های داخل جداول استفاده می‌شود).
- DCL: It is used to manage user access to data (برای مدیریت دسترسی کاربران به داده‌ها به کار می‌رود).

### 4. Data (داده):
Raw and unprocessed facts such as numbers, text, or dates (واقعیت‌های خام و پردازش‌نشده مانند عدد، متن یا تاریخ).

### 5. Information (اطلاعات):
Processed and organized data that provides meaning and context (داده‌های پردازش‌شده و سازمان‌یافته‌ای که معنا و مفهوم ایجاد می‌کنند).

---
<br>

# Data Definition Language (زبان تعریف داده)

### 1. Data Type (نوع داده ای)

```BYTE``` &nbsp; Bit data with a range of 1 to 255 (داده بیتی با رنج 1 تا 255).

```INT``` &nbsp; Integer data (داده عددی صحیح).

```FLOAT``` &nbsp; Decimal numeric data (داده عددی اعشاری).

```VARCHAR(N)``` &nbsp; Rendering characters with a variable number (ارایه کارکتر با تعداد متغیر).

```NVARCHAR(N)``` &nbsp; Representing a variable number of Unicode characters (ارایه کارکتر یونی کد با تعداد متغیر).

```TEXT``` &nbsp; String data (داده رشته ای).

```DATE``` &nbsp; Date data (داده تاریخ).

```TIME``` &nbsp; Time data (داده زمان).

```DATETIME``` &nbsp; Date and time data (داده تاریخ و زمان).

```BIT / BOOLEAN``` &nbsp; Boolean data (داده بولین).

```IMAGE``` &nbsp; Image data (داده تصویر).

### 2. Limitation (محدودیت)

It is a constraint that makes the value of each row unique and non-empty so that each row in the table has a unique identification (یک محدودیت است که مقدار هر ردیف را منحصر‌به‌فرد و غیرخالی می‌کند تا هر ردیف در جدول شناسایی یکتا داشته باشد).
```ruby
PRIMARY KEY
```
Establishes a relationship between two tables by connecting a column in one table to the primary key of another table (با اتصال یک ستون در یک جدول به کلید اصلی جدول دیگر، بین دو جدول رابطه برقرار می‌کند).
```ruby
FOREIGN KEY
```
Ensures that all values ​​in a column are unique and there are no duplicate values (اطمینان می‌دهد تمام مقادیر در یک ستون منحصربه‌فرد باشند و مقدار تکراری وجود نداشته باشد).
```ruby
UNIQUE
```
Ensures that there is a value in the column (اطمینان می‌دهد حتما مقداری در ستون وجود داشته باشد).
```ruby
NOT NULL
```
Ensures that column values ​​match a specified condition (اطمینان می‌دهد مقادیر ستون با یک شرط مشخص سازگار باشند).
```ruby
CHECK (<Column Name> == X)
```
```(<Column Name> >= X)```

```(<Column Name> <= X)```

```(<Column Name> != X)```

### 3. Feature (ویژگی)

A property for numeric columns that automatically starts the value at number X and increases it by Y units each time (یک ویژگی برای ستون‌ های عددی است که مقدار را به‌ صورت خودکار از عدد اول شروع کرده و هر بار به اندازه عدد دوم افزایش می‌دهد).
```ruby
IDENTITY(X,Y)
```
If no value is entered, assigns a default value to the column (در صورت وارد نشدن مقدار، یک مقدار پیش‌فرض به ستون اختصاص می‌دهد).
```ruby
DEFAULT <Value>
```

Assuming that columns X and Y have already been created in the table, to create a column with automatic calculation from the two columns X and Y, a new column can be created as follows (با فرض ساخته شدن ستون دلخواه از قبل در جدول، برای ساخت ستون با محاسبه خودکار از دو ستون دلخواه میتوان به حالت زیر یک ستون جدید ساخت).
```ruby
<Column Name> AS (<Column Name Previous N> * <Column Name Previous M>)
```
```(<Column Name Previous N> + <Column Name Previous M>)```

```(<Column Name Previous N> - <Column Name Previous M>)```

```(<Column Name Previous N> / <Column Name Previous M>)```

```(<Column Name Previous M> % <Column Name Previous M>)```

### 4. Data Base (پایگاه داده)

Create a database with a custom name (ایجاد یک دیتا بیس جدید با نام دلخواه)
- The number of databases can be one or more (تعداد دیتابیس می تواند یک یا بیشتر باشد).
```ruby
CREATE DATABASE <Database Name N>,   ...   ,<Database Name M>
```

Using a database created with a custom name (استفاده از دیتا بیس ساخته شده با نام دلخواه)
```ruby
USE <Database Name>
```

### 5. Table (جدول)

Create a table with a custom name (ایجاد یک جدول جدید با نام دلخواه)
- The number of constraints and features can be zero or more (تعداد محدودیت و ویژگی ها می تواند صفر یا بیشتر باشد).
```ruby
CREATE TABLE <Table Name>
(
    <Value Name> <Data Tayp> <Limitation N> ... <Limitation M> <Feature N> ... <Feature M>,

    ...

    <Value Name> <Data Tayp> <Limitation N> ... <Limitation M> <Feature N> ... <Feature M>
);
```
---
<br>

# Data Manipulation Language (دستورات مدیریت داده)

### 1. Value (مقدار)

Insert any number of values ​​into the table (درج هر تعداد مقدار در جدول).
```ruby
INSERT INTO <Table Name> (S, I,   ...   , B, DT)
    VALUES
    ('SN', 1,   ...   , False, 0000/00/00 00:00),

    ...

    ('SM', 10,   ...   , True, 1111/11/11 11:11);
```

### 2. Select (انتخاب)

Retrieves columns from tables (ستون ها را از جدول ها بازیابی می‌کند).
* The number of columns and tables can be one or more (تعداد ستون ها و جدول ها میتواند یک یا بیشتر باشد).
* If you SELECT only one table, you do not need to enter the table name in the SELECTION section (در صورت انتخاب تنها یک جدول نیاز به نام جدول در بخش انتخاب نیست).
```ruby
SELECT <Table Name N>.<Columns Name X>,   ...   , <Table Name M>.<Columns Name Y>
FROM <Table Name N>,   ...   , <Table Name M>
```
Retrieves columns from tables with specified conditions (ستون ها را از جدول ها با شرط ها های گفته شده بازیابی می‌کند).
* The number of columns, tables, and conditions can be one or more (تعداد ستون ها، جدول ها و شرط ها میتواند یک یا بیشتر باشد).
* If you SELECT only one table, you do not need to enter the table name in the SELECTION section (در صورت انتخاب تنها یک جدول نیاز به نام جدول در بخش انتخاب نیست).
```ruby
SELECT <Table Name N>.<Columns Name>,   ...   , <Table Name M>.<Columns Name>
FROM <Table Name N>,   ...   , <Table Name M>
WHERE <Table Name N>.<Column Name N> = <Table Name M>.<Column Name M> AND   ...   AND <Table Name K>.<Column Name K> = <Table Name I>.<Column Name I>;
```
The selected columns are created and copied with the new selected name and can be used (ستون های انتخاب شده با نام جدید انتخاب شده ساخته و کپی شده و می تواند مورد استفاده بگیرد).
* The number of columns and tables can be one or more (تعداد ستون ها و جدول ها میتواند یک یا بیشتر باشد).
* If you SELECT only one table, you do not need to enter the table name in the SELECTION section (در صورت انتخاب تنها یک جدول نیاز به نام جدول در بخش انتخاب نیست).
* You can use the same condition as above (میتوان از شرط هم مانند بالا استفاده کرد).
```ruby
SELECT <Table Name N>.<Columns Name>,   ...   , <Table Name M>.<Columns Name>
FROM <Table Name N> AS <New Name>,   ...   , <Table Name M> AS <New Name>
```
<br>

❗You can also use the following two options instead of all Table Names (میتوان به جای تمام نام جدول ها از دو حالت زیر هم استفاده کرد)<br>
* ``` * ``` &nbsp; To select all columns (برای انتخاب تمام ستون های جدول).<br>
* ```<Column Name N>,   ...   , <Column Name M>``` &nbsp; To select multiple columns from a table (برای انتخاب چند ستون مورد نظر از یک جدول).<br>

### 3. Update (بروزرسانی)

Changes the data in the table (داده های موجود در جدول را تغییر می دهد).
* The number of columns and tables can be one or more (تعداد ستون ها و جدول ها میتواند یک یا بیشتر باشد).
```ruby
UPDATE <Table Name N>,   ...   , <Table Name M>
SET <Column Name N> = X,   ...   , <Column Name M> = Y
WHERE <Column Name N> = X AND   ...   AND <Column Name M> = Y;
```

### 4. Delete (حذف)

Deletes records from the table (رکوردهایی را از جدول حذف می‌کند).
* The number of columns and tables can be one or more (تعداد ستون ها و جدول ها میتواند یک یا بیشتر باشد).
```ruby
DELETE FROM <Table Name N>,   ...   , <Table Name M>
WHERE <Column Name> = X AND   ...   AND <Column Name> = Y;
```

---
<br>

# Functions and Operators (توابع و عملگرها)


---
<br>

# Joins (روابط بین جدول‌ها)


---
<br>

# Online SQL compiler (کامپایلر آنلاین زبان پرس‌ و جوی ساختار یافته)

### [1. Online SQL compiler (کامپایلر آنلاین زبان پرس‌ و جوی ساختار یافته)](https://sqliteonline.com/)
---
