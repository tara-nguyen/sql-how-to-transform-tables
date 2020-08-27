```sql
-- Find the average total distance flown by day of week and month. Use a non-correlated subquery.

SELECT f.dep_month, f.dep_day_of_week,
  AVG(f.flight_distance) AS average_distance
FROM (
  SELECT dep_month, dep_day_of_week, dep_date,
    SUM(distance) AS flight_distance
  FROM flights
  GROUP BY 1,2,3
) f
GROUP BY 1,2
ORDER BY 1,2;

-- Find the id of the flights whose distance is below average for their carrier. Use a correlated subquery.

SELECT id FROM flights f
WHERE distance < (
  SELECT AVG(distance) FROM flights
  WHERE carrier = f.carrier
);

-- Write a query to view flights by origin, flight id, and sequence number. Use a correlated subquery.

SELECT origin, id,
  (
    SELECT COUNT(*) FROM flights f
    WHERE f.id < flights.id
    AND f.origin = flights.origin
  ) + 1 AS flight_sequence_number
FROM flights;
```
