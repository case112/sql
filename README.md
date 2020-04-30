## SQL Samples

**Select query with limited rows**

    SELECT column, another_column, …
    FROM mytable
    WHERE condition(s)
    ORDER BY column ASC/DESC
    LIMIT num_limit OFFSET num_offset;


**Select query with LEFT/RIGHT/FULL JOINs on multiple tables**

> If tables are joined can select from multiple tables

    
    SELECT column, another_column, …
    FROM mytable
    INNER/LEFT/RIGHT/FULL JOIN another_table 
        ON mytable.id = another_table.matching_id
    WHERE condition(s)
    ORDER BY column, … ASC/DESC
    LIMIT num_limit OFFSET num_offset;

**Select with not existing in another table**

    SELECT DISTINCT building_name
    FROM buildings 
    LEFT JOIN employees
        ON building_name = building
    WHERE role IS NULL;


**Example query with both column and table name aliases**
    
    SELECT column AS better_column_name, …
    FROM a_long_widgets_table_name AS mywidgets
    INNER JOIN widget_sales
        ON mywidgets.id = widget_sales.widget_id;



**Select query with HAVING constraint**


    SELECT group_by_column, AGG_FUNC(column_expression) AS aggregate_result_alias, …
    FROM mytable
    WHERE condition
    GROUP BY column
    HAVING group_condition;
