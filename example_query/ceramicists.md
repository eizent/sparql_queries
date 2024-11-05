This query returns the ceramicists in Bryn Mawr College's Special Collections as an Image Grid. 

```sql
#defaultView:ImageGrid
SELECT ?item ?pic WHERE{
  ?item
        wdt:P106 wd:Q7541856;
        wdt:P6379 wd:Q101240133;
        wdt:P18 ?pic.
}
```
