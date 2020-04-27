## SQL Samples

**Select query with limited rows**

    SELECT column, another_column, …
    FROM mytable
    WHERE condition(s)
    ORDER BY column ASC/DESC
    LIMIT num_limit OFFSET num_offset;


**Select query with INNER JOIN on multiple tables**

> If tables are joined can select from multiple tables

    SELECT column, another_table_column, 
    FROM mytable
    INNER JOIN another_table 
        ON mytable.id = another_table.id
    WHERE condition(s)
    ORDER BY column, … ASC/DESC
    LIMIT num_limit OFFSET num_offset;
