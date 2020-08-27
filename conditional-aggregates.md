```sql
-- Find the percentage of flights from Delta by origin.

SELECT origin, 
  100. * SUM(
    CASE WHEN carrier = 'DL' THEN distance
    ELSE 0
    END
  ) / SUM(distance) AS percentage_flight_distance_from_delta
FROM flights
GROUP BY 1;
*/

-- Find the percentage of high elevation airports (elevation >= 2000) by state.

SELECT state,
  100. * COUNT(
    CASE WHEN elevation >= 2000 THEN 1 ELSE NULL
    END
  ) / COUNT(*) AS percentage_high_elevation_airports
FROM airports
GROUP BY 1;
```
