# Exercise_5_Oracle_SQL

This directory contains **4 SQL exercises** written in **Oracle SQL**, focusing on topics such as:
- Transaction reporting and analysis
- Monthly and regional grouping
- Aggregation and conditional logic
- Terminal-based performance queries
- Real-world fee calculation scenarios

Each query is saved in a separate file: `q1.sql` to `q4.sql`

---

## Problem Descriptions

### 🔹 Question 1 – q1.sql  
*Description:*

به تفکیک استان و ماه، تعداد تراکنش، مجموع مبلغ تراکنش و تعداد کارت‌های یکتا را استخراج کنید.  

*For each province and month, extract transaction count, total amount, and count of unique cards.*

---

### 🔹 Question 2 – q2.sql  
*Description:*

جدولی ایجاد کنید که ستون‌های آن شامل شماره ترمینال، تعداد کل تراکنش‌ها، تعداد تراکنش‌های خرید(00=trantype)، مانده‌گیری(31=trantype)، خرید شارژ(50=trantype)، مجموع مبلغ تراکنش و جمع مبلغ voucher باشد. ترمینال‌های بدون تراکنش هم باید نمایش داده شوند (برای ماه دی).  

*Build a transaction summary per terminal in Dey 1401, including 0-transaction terminals, with details such as type-based counts, total amount, and voucher sum.*

---

### 🔹 Question 3 – q3.sql  
*Description:*

مطابق با فرمول زیر برای محاسبه کارمزد هر یک از انواع تراکنش، مجموع کارمزد تراکنش برای هر پایانه را در هر ماه محاسبه کنید.

تراکنش خرید:

1. مبالغ زیر 5000 تومان، 230 تومان
2. مبلغ بین 5000 الی 25000 تومان : 250 - amount ٪۰.۰1(مالیات بر ارزش افزوده نیز از آن کسر شود)
3. مبلغ باالی 25000 تومان ، 2060 تومان
4. تراکنش مانده گیری: 750 تومان
5. تراکنش خرید شارژ: 750 تومان

*Calculate the total transaction fee per terminal per month based on the following logic:*

*Purchase transactions:*

*Amount under 5,000 → 230 IRR*

*Amount between 5,000 and 25,000 → 250 IRR minus 0.01% of the amount (including VAT)*

*Amount above 25,000 → 2,060 IRR*

*Balance inquiry: 750 IRR*

*Mobile charge purchase: 750 IRR*

---

### 🔹 Question 4 – q4.sql  
*Description:*

برای ترمینال‌هایی که حداقل ۲ بار در دی ماه تراکنش داشته‌اند، تعداد تراکنش‌های آن‌ها در بهمن را به تفکیک ترمینال استخراج کنید.  

*Extract the number of Bahman transactions for terminals with at least 2 transactions in Dey.*

---

## 📝 Notes
These SQL queries were written in Oracle SQL to simulate realistic transaction analytics use cases in financial systems.  
They include dynamic grouping, subqueries, conditional logic, and transaction fee modeling using Shamsi (Persian) calendar dates.

---

## 📁 Supporting Files

The following files are included for reference and execution:

- `tb_transactions.txt` – Contains sample data for the `TB_TRANSACTIONS` table.
- `tb_merchants.txt` – Contains sample data for the `TB_MERCHANTS` table.
- `CREATE_TABLE_TB_MERCHANTS.sql` – SQL script to create the `TB_MERCHANTS` table structure.
- `CREATE_TABLE_TB_TRANSACTION.sql` – SQL script to create the `TB_TRANSACTIONS` table structure.

These files are helpful for testing the provided queries and replicating the data environment locally.
