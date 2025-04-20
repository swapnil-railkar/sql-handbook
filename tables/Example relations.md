
One note lookup for all relations.

| id  | name      | department_name  | salary |
| --- | --------- | ---------------- | ------ |
| 1   | John      | computer science | 2000   |
| 2   | Doe       | finance          | 2500   |
| 3   | Marc      | history          | 1000   |
| 4   | Bruce     | computer science | 3000   |
| 5   | Peter     | finance          | 3500   |
| 6   | Strange   | history          | 2300   |
| 7   | Tony      | computer science | 3900   |
| 8   | Spongebob | finance          | 2300   |
| 9   | Ferb      | history          | 2350   |
Note : 
1. do not add instructor for chemistry (Left join).
*table* : #instructor 

| course_id | title                            | department_name  | credits |
| --------- | -------------------------------- | ---------------- | ------- |
| cs        | introduction to computer science | computer science | 4       |
| fin       | introduction to finance          | finance          | 3       |
| hist      | history of Egypt                 | history          | 3       |
| ch        | introduction to chemistry        | chemistry        | 4       |
*table* : #course 

| department_name  | building | budget |
| ---------------- | -------- | ------ |
| computer science | B101     | 20000  |
| finance          | B102     | 10000  |
| history          | B103     | 15000  
*table* : #department 