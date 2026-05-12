# Homework 3

## Problem 1. [100pts] 

Consider the following schema of a bank:

```text
   customer (name: text, credit: integer)
   loan (no: string, type: text, minCredit: integer, amount: integer)
   borrower (cname: text, lno: text, due: date)
```

where `borrower.cname` and `borrower.lno` are foreign keys referencing customer, respectively loan, whose primary keys
are `name`, respectively `no` (number).
Attribute `loan.minCredit` indicates the minimum credit required of a customer to qualify for that loan.
 
Write the following queries in RA.

1. (10 pts): Find the names of customers who took out a “jumbo mortgage” loan (a loan of type "jumbo mortgage"). 
The output should be a table with a "name" column.
2. (10 pts): Find the names of customers who took out a “jumbo mortgage” loan or have a credit rating
of at least 750. The output should be a table with a "name" column.
3. (10 pts): Find the names of customers who took out a “jumbo mortgage” loan and a “student” loan.
The output should be a table with a "name" column.
4. (10 pts): Find pairs of names of customers who share the same loan. Avoid listing a customer with
herself (e.g. do not list (Jane,Jane)). Also avoid repeating pairs which are equal modulo swapping the
components (e.g. do not list both (John,Jane) and (Jane,John) - list only (Jane,John) once). 
Sort the output pairs by the first name, then by the second. 
The output should be a table with a "name1" and a "name2" column.
5. (10 pts): Find the loan numbers ("no") shared by at least two different customers. The output should
be a table with a "loanNo" column.
6. (10 pts): Find the customers who borrowed a total of at least 13000. 
The output should be a table with a "name" column.
7. (10pts): Find the loans with the maximal amount (there may be multiple tied loans, output all of them).
the output should be a table with a "loanNo" column.
8. (15 pts): Find the total amount borrowed by "John Smith". If he took out no loans, then output 0. 
The output should be a table with a "borrowedAmount" column. 
9. (15 pts): Among the loans taken by a borrower named "John Smith", find those with highest minCredit requirement
(note that multiple loans taken by John could be tied for the highest minCredit). If John took out no loans, the result is empty.
The output should be a table with a "loanNo" column.

You will of course us the RA dialect supported by RADB.

Submit files q1.ra, q2.ra, ..., q9.ra.