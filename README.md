# SQL To Slick Memo


## Sample Tables:

### Tables - tbA:
| Column Name   | Data Type     | Sample Value |
| ------------- |:-------------:| ------------:|
| id            | Long          | 1            |
| name          | String        | Test         |
| age           | Int           | 10           |

### Tables - tbB:
| Column Name   | Data Type     | Sample Value |
| ------------- |:-------------:| ------------:|
| id            | Long          | 1            |
| tbA_id        | Long          | 1            |
| email         | String        | test@test.te |
| address       | String        | Test Address |

## Basic Select Statements:

SQL:
```sql
SELECT * FROM tbA
```

Slick:
```scala
Query(tbA)
.result
```

-----------------------

SQL:
```sql
SELECT id, name FROM tbA
```

Slick:
```scala
Query(tbA)
.map{ case tbA => (tbA.id, tbA.name) }
.result
```
