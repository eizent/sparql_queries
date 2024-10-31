This query will show all the artists that have works in the collectiong at the Art Institute of Chicage.

```sql
SELECT ?item ?itemLabel   
WHERE {  
    ?item wdt:P106 wd:Q483501;  
          wdt:P6379 wd:Q239303  
SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }  
} 
```

**Challenge**


How could you change this query to find all the artists in Bryn Mawr Special Collections (that have been added to Wikidata)?
