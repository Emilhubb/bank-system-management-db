# Bank System Management Database

A database architecture for a bank credit and cash management system built on MSSQL Server.

## 🚀 Technologies
* **RDBMS:** Microsoft SQL Server
* **Language:** T-SQL (Stored Procedures, Functions, Constraints)

## 📊 Tables and Structure (12 Core Tables)
* **Customer & Workplace:** `Customers`, `Workplace`, `CustomersWorkplace`
* **Credit & Contract:** `Contract`, `CreditType`, `Statement` (Payment schedule)
* **Structure & Staff:** `Branch`, `BankEmployees`, `BankPositions`
* **Finance & Transaction:** `Transaction`, `TransactionType`, `Currency`

## 🛡️ Applied Business Rules
* **Check Constraints:** `Fin_code` (7 characters) and `Account_number` (20 characters) validation. Credit-specific limit, interest rate, and employment history constraints implemented inside the `Contract` table.
* **Database Security:** An `IDK` Application Role for secure, application-level access control.

## ⚙️ Procedures and Functions
* `dbo.Ay`: Calculates date differences in months for credit terms.
* `dbo.Staj`: Verifies customer employment duration for credit eligibility.
* `dbo.SumOfSalary`: Analyzes total salary turnover across employees and customers.
* `dbo.UmumiSay`: Generates a dynamic report of total credit amounts issued per branch.
* `dbo.Exist` & `dbo.SelectByID`: Secure data retrieval procedures based on customer parameters.

## 🛠️ Setup
1. Clone the repo: `git clone https://github.com/Emilhubb/bank-system-management-db.git`
2. Open `bank_system.sql` in SSMS and press **Execute (F5)**.
