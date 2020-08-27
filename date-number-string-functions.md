```sql
-- Each of the baked goods is packaged by Baker’s Market exactly five hours, twenty minutes, and two days after the delivery (designated by delivery_time). Create a query returning all the packaging times for the goods in the baked_goods table.

SELECT 
  DATETIME(delivery_time, '+5 hours','20 minutes','2 days') AS package_time 
FROM baked_goods;

-- We also have information about cook time designated as cook_time and cool down time designated as cool_down_time in the baked_goods table. Find the greatest time value for each item in the table.

SELECT id, MAX(cook_time, cool_down_time)
FROM baked_goods;

-- Combine the first_name and last_name columns from the bakeries table as the full_name to identify the owners of the bakeries.

SELECT 
  first_name || ' ' || last_name AS full_name
FROM bakeries;

-- Any time enriched_flour appears in the ingredients list, we’d like to replace it with just flour. Apply this transformation.

SELECT REPLACE(ingredients, 'enriched_flour', 'flour') AS item_ingredients
FROM baked_goods;
```
