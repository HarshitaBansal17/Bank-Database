# Bank-Database
The database includes the following entities (Tables):
People: Represents individuals who interact with the bank, including customers and employees.

Branches: Contains information about the different branches or offices of the bank.

Employees: Stores data about individuals who are bank employees.

Customers: Stores information about individuals who are bank customers.

Accounts: Represents the different accounts that customers or groups of customers can have in the bank.

AccountOwnerships: Stores the relationship between accounts and their owners.

Loans: Stores information about the loans granted by the bank to customers.

LoanPayments: Represents the scheduled payments associated with loans.

Transactions: Stores information about the various transactions performed in the bank.

Transfers: Represents transfers of funds between bank accounts.

Functional Requirements
Users should be able to perform the following actions with the database:

Add, retrieve, update, and delete information about people, including customers and employees.
Manage branch information, such as adding new branches and updating branch details.
Track and manage employee data, including their positions and branch assignments.
Manage customer information, including their customer type (regular or premium).
Create and manage different types of accounts for customers.
Track account ownership and associations between accounts and customers.
Manage loan information, including loan types, amounts, interest rates, and terms.
Track loan payments and their associated details. 9.Record and manage various types of transactions, such as deposits and withdrawals.
Perform fund transfers between bank accounts.
Representation
Entities
The entities represented in the database are:

People: Represented by the People table, with attributes like id, firstName, lastName, DateOfBirth, PhoneNumber, Email, and Address.

Branches: Represented by the Branches table, with attributes like id, branchName, branchCode, Address, and PhoneNumber.

Employees: Represented by the Employees table, with attributes like id, personId, branchId, and position.

Customers: Represented by the Customers table, with attributes like id, personId, and customerType.

Accounts: Represented by the Accounts table, with attributes like id, branchId, accountType, accountNumber, currentBalance, createdAt, closedAt, and accountStatus.

AccountOwnerships: Represented by the AccountOwnerships table, with attributes like id, accountId, and ownerId.

Loans: Represented by the Loans table, with attributes like id, customerId, loanType, loanAmount, interestrate, term, startDate, endDate, and status.

LoanPayments: Represented by the LoanPayments table, with attributes like id, loanId, scheduledPaymentDate, paymentAmount, principalAmount, interestAmount, paidAmount, and PaidDate.

Transactions: Represented by the Transactions table, with attributes like id, accountId, transactionType, amount, and transactionDate.

Relationships
The relationships between the entities in the database are as follows:

The Employees table has foreign key references to the People table (via personId) and the Branches table (via branchId).

The Customers table has a foreign key reference to the People table (via personId).

The Accounts table has a foreign key reference to the Branches table (via branchId).

The AccountOwnerships table has foreign key references to the Accounts table (via accountId) and the Customers table (via ownerId).

The Loans table has a foreign key reference to the Customers table (via customerId).

The LoanPayments table has a foreign key reference to the Loans table (via loanId).

The Transactions table has a foreign keyreference to the Accounts table (via accountId).

The Transfers table has foreign key references to the Accounts table (via originAccountId and destinationAccountId).

