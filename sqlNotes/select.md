select, sql, select_distinct, case, like
  # SELECT Statement in SQL
  
  - use `LIKE` to search for a pattern
  `%` is a wildcard character representing any characters or none.
  
  ```sql
  SELECT name 
  FROM author
  WHERE name LIKE 'R%'
  ```
  
  - select values in a range
  ```sql
  -- use <=, >=
  SELECT title, pages
  FROM book
  WHERE pages >= 290 AND pages <= 300
  
  -- or use BETWEEN AND, which are inclusive
  SELECT title, pages
  FROM book
  WHERE pages BETWEEN 290 AND 300
  ```
  
  - retrieving rows using a set of values
  ```sql
  -- using OR
  SELECT name, country
  FROM author
  WHERE country = 'US' OR country ='CA'
  
  -- using IN
  SELECT name, country
  FROM author
  WHERE country IN ('US', 'CA')
  ```
  
  - use `ORDER BY` to order results
  ```sql
  -- order in ascending order
  SELECT name 
  FROM author
  ORDER BY name
  
  -- order in descending order
  SELECT name 
  FROM author
  ORDER BY name DESC
  
  -- order by columns sequence number 
  -- will be ordered by pages
  SELECT title, pages 
  FROM book
  ORDER BY 2
  ```
  
  - use `DISTINCT` to eliminate duplicates
  ```sql
  SELECT DISTINCT(country) 
  FROM author
  ```
  
  - use `CASE` for conditionals
  ```sql
  SELECT
  CASE 
      WHEN (a+b+c-GREATEST(a,b,c))/2 <= GREATEST(a,b,c)/2 THEN 'Not A Triangle'
      WHEN a=b AND a=c THEN "Equilateral"
      WHEN a=b OR a=c OR b=c THEN 'Isosceles'
      ELSE 'Scalene'
  END
  FROM triangles
  ``` 
  
  ### Grouping result sets
  
  - counting results
  ```sql
  SELECT country, count(country) AS count
  FROM author
  GROUP BY country
  ```
  - restricting restult sets with `HAVING`
  ! The `WHERE` clause works with the entiry result set, but the `HAVING` clause works only with the `GROUP BY` clause.
  ```sql
  SELECT country, count(country) AS count
  FROM author
  GOURP BY country
  HAVING count(country) > 4
  ```
  
  
  
  
  
  
  
'''
linesHighlighted: []
isStarred: false
isTrashed: false
