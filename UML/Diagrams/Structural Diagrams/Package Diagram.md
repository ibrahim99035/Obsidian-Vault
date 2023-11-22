A structural Diagram that is used to depict the high-level structure of a system, illustrating how various elements are grouped into packages and how those packages depend on each other.
### Key Components of a Package Diagram:

1. **Package:**
    
    - Represents a namespace that organizes a set of related UML elements, such as classes, interfaces, and other packages.
    - Displayed as a rectangle with the package name at the top.
2. **Package Merge:**
    
    - Represents the combining of two or more packages into a single package.
    - Shown as a dashed arrow pointing from the merged package(s) to the target package.
3. **Dependency:**
    
    - Represents a relationship between packages, where one package depends on another.
    - Shown as a dashed arrow with an arrowhead pointing from the dependent package to the independent package.
4. **Element:**
    
    - Represents any UML element (e.g., class, interface) that is part of a package.
    - Displayed inside the package rectangle.

---
![[Pasted image 20231122115105.jpg]]

---
```
+---------------------+       +-----------------------+
|       Banking       |       |       Accounting      |
|       System        |       |        Package        |
+---------------------+       +-----------------------+
| - Customer          |       | - Account             |
| - Transaction       |       | - Ledger              |
| - Account           |       | - ReportGenerator     |
|                     |       +-----------------------+
| + CustomerService   |                 |
| + TransactionService|                 |
| + AccountService    |                 |
+---------------------+                 |
         |                              |
         v                              v
+----------------------+     +-----------------------+
|     Database         |     |        Reporting      |
|      Package         |     |        Package        |
+----------------------+     +-----------------------+
| - CustomerTable      |     | - FinancialReport     |
| - TransactionTable   |     | - TransactionReport   |
| - AccountTable       |     | - AuditReport         |
+----------------------+     +-----------------------+

```
##### In this example:
- The `BankingSystem` package contains classes related to customers, transactions, and accounts, as well as service classes.

- The `Accounting` package contains classes related to accounting, including accounts, ledgers, and a report generator.

- There is a dependency between the `Accounting` package and the `BankingSystem` package, indicating that the accounting functionalities depend on elements from the banking system.

- The `Database` and `Reporting` packages contain elements related to data storage and reporting, respectively.


#UML