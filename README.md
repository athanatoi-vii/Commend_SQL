# List (لیست)
1. [Introduction](#Introduction-مقدمه)
- Data Base
- SQL
- Types of Commands
- Data
- Information
2. [Data Definition Language (دستورات تعریف داده)](#Data-Definition-Language-زبان-تعریف-داده)
- Data Type 
- Limitation
- Feature
- Data Base
- Table
3. [Functions And Operators (توابع و عملگرها)](#Functions-and-Operators-توابع-و-عملگرها)
4. [Joins (روابط بین جدول‌ها)](#Joins-روابط-بین-جدول‌ها)
---
<br>

# Introduction (مقدمه)
* **Data Base (دیتا بیس):**<br>
It is a structured collection of data used to store and manage information (مجموعه‌ای ساختارمند از داده‌هاست که برای ذخیره و مدیریت اطلاعات استفاده می‌شود).
  
* **SQL (زبان پرس‌ و جوی ساختار یافته):**<br>
It is a standard language for creating, reading, and editing data in relational databases (زبان استانداردی برای ایجاد، خواندن، و ویرایش داده‌ها در پایگاه‌داده‌های رابطه‌ای است).

* **Types Of Commands (انواع نوع دستورات)**<br>
  - DDL: Used to create, modify, or delete database structure (برای ایجاد، تغییر یا حذف ساختار پایگاه‌داده استفاده می‌شود).
  - DML: It is used to manage data within tables (برای مدیریت داده‌های داخل جداول استفاده می‌شود).
  - DCL: It is used to manage user access to data (برای مدیریت دسترسی کاربران به داده‌ها به کار می‌رود).

* **Data (داده):**<br>
Raw and unprocessed facts such as numbers, text, or dates (واقعیت‌های خام و پردازش‌نشده مانند عدد، متن یا تاریخ).

* **Information (اطلاعات):**<br>
Processed and organized data that provides meaning and context (داده‌های پردازش‌شده و سازمان‌یافته‌ای که معنا و مفهوم ایجاد می‌کنند).
---
<br>

# Data Definition Language (زبان تعریف داده)

### 1. Data Type

* ```BYTE```           Bit data with a range of 1 to 255 (داده بیتی با رنج 1 تا 255).

* ```INT```            Integer data (داده عددی صحیح).

* ```FLOAT```          Decimal numeric data (داده عددی اعشاری).

* ```VARCHAR(N)```     Rendering characters with a variable number (ارایه کارکتر با تعداد متغیر).

* ```NVARCHAR(N)```    Representing a variable number of Unicode characters (ارایه کارکتر یونی کد با تعداد متغیر).

* ```TEXT```           String data (داده رشته ای).

* ```DATE```           Date data (داده تاریخ).

* ```TIME```           Time data (داده زمان).

* ```DATETIME```       Date and time data (داده تاریخ و زمان).

* ```BIT / BOOLEAN```  Boolean data (داده بولین).

* ```IMAGE```          Image data (داده تصویر).

### 2. Limitation


```ruby
PRIMARY KEY
```

### 3. Feature


```ruby
IDENTITY(1,1)
```

### 4. Data Base (پایگاه داده)

Create a database with a custom name (ایجاد یک دیتا بیس جدید با نام دلخواه)
```ruby
CREATE DATA BASE <My Name>
```

Using a database created with a custom name (استفاده از دیتا بیس ساخته شده با نام دلخواه)
```ruby
USE <My Name>
```

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


---
<br>

# Functions and Operators (توابع و عملگرها)


---
<br>

# Joins (روابط بین جدول‌ها)


---

