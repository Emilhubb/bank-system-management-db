# Bank System Management Database

MSSQL Server üzərində hazırlanmış bank kredit və kassa idarəetmə sisteminin verilənlər bazası arxitekturası.

## 🚀 Texnologiyalar
* **RDBMS:** Microsoft SQL Server
* **Dil:** T-SQL (Stored Procedures, Functions, Constraints)

## 📊 Cədvəllər və Struktur (12 Əsas Cədvəl)
* **Müştəri & İş yeri:** `Müştərilər`, `İşYeri`, `Müştərilərinİşyeri`
* **Kredit & Müqavilə:** `Müqavilə`, `KreditNövü`, `Hesabat` (Ödəniş qrafiki)
* **Strukturu & Heyət:** `Filial`, `Bankİşçiləri`, `BankVəzifələri`
* **Maliyyə & Transaksiya:** `Transaksiya`, `TransaksiyaNövü`, `Valyuta`

## 🛡️ Tətbiq Olunan Biznes Qaydaları
* **Check Constraints:** `Fin_kod` (7 simvol) və `Hesab_nömrəsi` (20 simvol) validasiyası. `Müqavilə` cədvəlində kredit növlərinə görə limit, faiz və staj məhdudiyyətləri.
* **Security:** Verilənlər bazası səviyyəsində giriş kontrolu üçün `IDK` tətbiq rolu (Application Role).

## ⚙️ Prosedur və Funksiyalar
* `dbo.Ay`: İki tarix arasındakı fərqi ay olaraq hesablayır.
* `dbo.Staj`: Müştərinin iş stajını yoxlayır (Kredit müraciəti üçün).
* `dbo.SumOfSalary`: İşçi və müştərilərin ümumi maaş dövriyyəsini hesablayır.
* `dbo.UmumiSay`: Filiala görə verilən ümumi kredit miqdarını çıxarır.
* `dbo.Exist` & `dbo.SelectByID`: Müştəri ID-sinə görə təhlükəsiz sorğulama prosedurları.

## 🛠️ Quraşdırma
1. Reponu klonlayın: `git clone https://github.com/Emilhubb/bank-system-management-db.git`
2. `bank_system.sql` faylını SSMS-də açın və **Execute (F5)** edin.
