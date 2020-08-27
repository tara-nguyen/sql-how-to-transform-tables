```sql
-- Find the average sale price over both order_items and order_items_historic tables.

SELECT id, AVG(sale_price) FROM (
  SELECT id, sale_price FROM order_items
  UNION ALL
  SELECT id, sale_price FROM order_items_historic
)
GROUP BY 1;

-- Select the items in the category column that are both in the newly acquired new_products table and the legacy_products table.

SELECT category FROM new_products
INTERSECT
SELECT category FROM legacy_products;

-- Select the items in the category column that are in the legacy_products table and not in the new_products table.

SELECT category FROM legacy_products
EXCEPT
SELECT category FROM new_products;
```
