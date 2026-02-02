In database **ER modeling**, the common relationship types (based on **cardinality**) are **3 main ones**:

## ✅ 1) One-to-One (**1 : 1**)

Each entity instance relates to **at most one** instance of the other. </br>
`FACT: ` </br>
`1. One entity acquires the identifier of the other` </br>
`2. Fk is unique here` </br>
`3. The primary key of one table(any unique column from any table) is the Fk in the other table` </br>



Example:
Person ↔ Passport

---

## ✅ 2) One-to-Many (**1 : N**)

One entity instance can relate to **many** instances of the other.

`FACT: ` </br>
`1. Fk is not unique in a 1:N relation` </br>
`2. Parent table(oneside clientID) which is Pk of this table, during relationship move to the child table(manySide bankAccount) and work as FK` </br>
`3. So, in a 1:N relationship Foreign Key stay in the child table` </br>

Example:
client → Bank account 
Department → Employees

---

## ✅ 3) Many-to-Many (**M : N**)

Many instances on both sides can relate to many on the other side.

`FACT: ` </br>
`1. M:M relation cannot be directly impliment, to impliment this relationship we need a third table which called junction table, join table or link table ` </br>
`2. if a table has two foreign keys it is called M:M` </br>
`3. In this relationship there is no primary key, two table's Pk make a composit key during relationship` </br>

Example:
Students ↔ Courses

---


---


