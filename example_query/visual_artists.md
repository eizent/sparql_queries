This query will return all the visual artists who have works in Bryn Mawr's Special Collections and in the Stedelijk Museum in Amsterdam.

```sql
SELECT ?item WHERE{
  ?item wdt:P106 wd:Q3391743;
        wdt:P6379 wd:Q101240133;
        wdt:P6379 wd:Q924335.
}
```
