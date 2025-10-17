# List (لیست)

### [1. Introduction](#Introduction-مقدمه)
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
### [4. Functions And Operators (توابع و عملگرها)](#Functions-and-Operators-توابع-و-عملگرها)
### [5. Joins (روابط بین جدول‌ها)](#Joins-روابط-بین-جدول‌ها)

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

### 1. Data Type

```BYTE```           Bit data with a range of 1 to 255 (داده بیتی با رنج 1 تا 255).

```INT```            Integer data (داده عددی صحیح).

```FLOAT```          Decimal numeric data (داده عددی اعشاری).

```VARCHAR(N)```     Rendering characters with a variable number (ارایه کارکتر با تعداد متغیر).

```NVARCHAR(N)```    Representing a variable number of Unicode characters (ارایه کارکتر یونی کد با تعداد متغیر).

```TEXT```           String data (داده رشته ای).

```DATE```           Date data (داده تاریخ).

```TIME```           Time data (داده زمان).

```DATETIME```       Date and time data (داده تاریخ و زمان).

```BIT / BOOLEAN```  Boolean data (داده بولین).

```IMAGE```          Image data (داده تصویر).
<br>

### 2. Limitation

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
CHECK (X == Y)
```
```(X >= Y)```

```(X <= Y)```

```(X != Y)```
<br>

### 3. Feature

A property for numeric columns that automatically starts the value at number X and increases it by Y units each time (یک ویژگی برای ستون‌ های عددی است که مقدار را به‌ صورت خودکار از عدد اول شروع کرده و هر بار به اندازه عدد دوم افزایش می‌دهد).
```ruby
IDENTITY(X,Y)
```
If no value is entered, assigns a default value to the column (در صورت وارد نشدن مقدار، یک مقدار پیش‌فرض به ستون اختصاص می‌دهد).
```ruby
DEFAULT 'X'
```
```DEFAULT 0```

```DEFAULT False```

Assuming that columns X and Y have already been created in the table, to create a column with automatic calculation from the two columns X and Y, a new column can be created as follows (با فرض ساخته شدن ستون دلخواه از قبل در جدول، برای ساخت ستون با محاسبه خودکار از دو ستون دلخواه میتوان به حالت زیر یک ستون جدید ساخت).
```ruby
XY AS (X * Y)
```
```(X + Y)```

```(X - Y)```

```(X / Y)```

```(X % Y)```
<br>

### 4. Data Base (پایگاه داده)

Create a database with a custom name (ایجاد یک دیتا بیس جدید با نام دلخواه)
```ruby
CREATE DATABASE <My Name>
```

Using a database created with a custom name (استفاده از دیتا بیس ساخته شده با نام دلخواه)
```ruby
USE <My Name>
```
<br>

### 5. Table (جدول)
```ruby
CREATE TABLE <My Name>
(
    <My Name> <Data Tayp> <Limitation> <Feature>,

    ...

    <My Name> <Data Tayp> <Limitation> <Feature>
);
```
---
<br>

# Data Manipulation Language (دستورات مدیریت داده)

### 1. Add Value In Table
```ruby
INSERT INTO <My Name Table> (S, I, B, T)
    VALUES
    ('S1', 0, False, 0000/00/00 00:00),

    ...

    ('S10', 10, True, 1111/11/11 11:11);
```
<br>

---
<br>

# Functions and Operators (توابع و عملگرها)


---
<br>

# Joins (روابط بین جدول‌ها)


---
