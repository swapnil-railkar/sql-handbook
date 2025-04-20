tags: #operators #dml 

#### Introduction : 

SQL defines strings by enclosing them into single quotes. A single quote character which is part of string is defined using double quote. For example the string "It's right" can be defined as 'It"s right'. SQL provides variety of functionalities to perform operations on strings such as string  comparisons, function on string, pattern matching.

#### String comparison : 

SQL standards specifies that comparing strings is case sensitive operation. That is, 'computer science' = 'Computer science' will be false. Some DBMS such as MYSQL and SQL server does not follow this standard and allows case insensitive comparison, in which case above example will yield true as result. This default behavior can be changed either at database level or at the level of specific attribute.

#### Function on Strings : 

SQL also permits variety of functions on strings. Few of them are listed below.
1. String concatenation (using "||").
2. Extracting substring ( using SUBSTRING(column_name, start_position, length) ).
3. Finding the length of the string (using LENGTH()).
4. Converting strings to uppercase (using UPPER(s) where s is string).
5. Converting strings to lowercase (using LOWER(s) where s is string).
6. Removing spaces at start and end of string if present (TRIM()).

#### Pattern matching : 

Pattern matching can be performed on string using keyword LIKE(). We define pattern by using two special characters : 
1. Percent (%) : The % character matches any substring.
2. Underscore (\_) : The \_ character matches any character.

Pattern matching is also case sensitive, that is, uppercase characters does not match with lowercase characters and vice versa. Consider following examples : 
- 'Intro%' matches any string beginning with 'Intro'.
- '%comp%' matches any string containing 'comp' as substring. ( ex : Introduction to computer science, computational biology).
- '\_ \_ \_' matches any string of exactly three characters.
- '\_ \_ \_ %' matches any string with at least three characters.

SQL uses function LIKE() for pattern mapping. For example :

```
SELECT *
FROM department
WHERE building LIKE '%10%';
```

For patterns to include special pattern characters like '%' or '\_', SQL defines special keyword called escape which is defined as '\\'. For example, 
- like 'ab\\%cd%' escape '\\' matches all strings beginning with 'ab%cd'.
- like 'ab\\\\cd' escape '\\' matches all string beginning with 'ab\\cd'.

