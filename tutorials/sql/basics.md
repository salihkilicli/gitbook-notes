---
description: Basic SQL Structures & Command
---

# Basics

Order of basic clauses:

1. **WITH**
2. **SELECT** list-cols \[**INTO** new-table]\[**AS** col-alias]
3. **FROM** table-source \[**WHERE** search-condition]
4. **GROUP BY** groupby-expression
5. **WINDOW** windowfunc-expression
6. **HAVING** search\_condition (within groupby clause)
7. **ORDER BY** order-expression \[**ASC** ascending | **DESC** descending]
8. **LIMIT** num-results

**UNION**, **EXCEPT**, **INTERSECT**, **AND**, **OR**, **AS**, **RANGE**, **IN**, **BETWEEN,** etc. can be used between queries to combine or compare their results. However, the order of execution is different.

Order of execution in SQL commands:

1. **FROM / JOIN / ON**
2. **WHERE**
3. **GROUP BY**
4. **WITH CUBE** **| ROLLUP**
5. **HAVING**
6. **SELECT** (Window Functions **SUM**, **COUNT**, **AVG**, etc. are executed here!)
7. **DISTINCT**
8. **ORDER BY**
9. **TOP**
10. **LIMIT**

| Command           | Description                              | Example                                                                                                                                                                                                                                                                                                                                   |
| ----------------- | ---------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **SELECT**        | Selects given columns from a given table | <p><strong><code>SELECT</code></strong><code> age </code><strong><code>FROM</code></strong><code> table</code><br><code></code>selects age col from table</p>                                                                                                                                                                             |
| **FROM**          | Table source to display                  | <p><strong><code>SELECT</code></strong><code> * </code><strong><code>FROM</code></strong><code> table</code><br><code></code>selects all cols from table</p>                                                                                                                                                                              |
| **LIMIT**         | Limits the number of results             | <p><strong><code>SELECT</code></strong><code> * </code><strong><code>FROM</code></strong><code> table</code><br><code></code><strong><code>LIMIT</code></strong><code> 100</code><br>displays 100 rows of table</p>                                                                                                                       |
| **WHERE**         | Condition to filter table                | <p><strong><code>SELECT</code></strong><code> age </code><strong><code>FROM</code></strong><code> table</code><br><code></code><strong><code>WHERE</code></strong><code> age &#x3C; 20</code><br>display rows with age &#x3C; 20</p>                                                                                                      |
| **(I)LIKE**       | Matches similar values                   | <p><strong><code>SELECT</code></strong><code> * </code><strong><code>FROM</code></strong><code> table</code><br><code></code><strong><code>WHERE</code></strong><code> name </code><strong><code>(I)LIKE</code></strong><code> '%S%'</code><br>displays rows with name including (Ss)S</p>                                                |
| **IN (BETWEEN)**  | Including (within) values                | <p><strong><code>SELECT</code></strong><code> * </code><strong><code>FROM</code></strong><code> table</code><br><code></code><strong><code>WHERE</code></strong><code> age </code><strong><code>IN</code></strong><code> (19,20,21)</code><br>selects rows where 19&#x3C;=age&#x3C;=21</p>                                                |
| **AND (OR)**      | Logic and (or) operators                 | <p><strong><code>SELECT</code></strong><code> * </code><strong><code>FROM</code></strong><code> table</code><br><code></code><strong><code>WHERE</code></strong><code> age </code><strong><code>BETWEEN</code></strong><code> 19 </code><strong><code>AND</code></strong><code> 21</code><br>selects rows where 19&#x3C;=age&#x3C;=21</p> |
| **IS (NOT) NULL** | Is data  missing (or not)                | <p><strong><code>SELECT</code></strong><code> * </code><strong><code>FROM</code></strong><code> table</code><br><code></code><strong><code>WHERE</code></strong><code> age </code><strong><code>IS NOT NULL</code></strong><br>excludes rows where age is missing</p>                                                                     |
| **ORDER BY**      | Order data asc or desc                   | <p><strong><code>SELECT</code></strong><code> * </code><strong><code>FROM</code></strong><code> table</code><br><code></code><strong><code>GROUP BY</code></strong><code> age </code><strong><code>DESC</code></strong><br>orders data by age column</p>                                                                                  |
|                   |                                          |                                                                                                                                                                                                                                                                                                                                           |
|                   |                                          |                                                                                                                                                                                                                                                                                                                                           |
|                   |                                          |                                                                                                                                                                                                                                                                                                                                           |
|                   |                                          |                                                                                                                                                                                                                                                                                                                                           |
|                   |                                          |                                                                                                                                                                                                                                                                                                                                           |
|                   |                                          |                                                                                                                                                                                                                                                                                                                                           |
|                   |                                          |                                                                                                                                                                                                                                                                                                                                           |
