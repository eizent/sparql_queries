This query will return all the visual artists who have works in Bryn Mawr's Special Collections and in the Stedelijk Museum in Amsterdam.

```sql
SELECT ?item ?itemLabel WHERE{
#triple one selecting visual artist (item-occupation-visual artist)
  ?item wdt:P106 wd:Q3391743;
#triple two filtering BMC Special Collections (item-has works in collection-BMC Spec Col)
        wdt:P6379 wd:Q101240133;
#triple three filtering Stedelijk (item-has works in collection-Stedelijk)
        wdt:P6379 wd:Q924335.
#connecting to the label service to also return names
SERVICE wikibase:label { bd:serviceParam wikibase:language "en". } 
}
```
