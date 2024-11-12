## Find all of the Women Artists in Bryn Mawr's Special Collections

```sql
#selecting only unique
SELECT DISTINCT * 
WHERE{
#triple one filtering for those with works in BMC Special Collections 
  ?item wdt:P6379 wd:Q101240133;
#triple two filtering for women (*is an instance of* woman)
        wdt:P21 wd:Q6581072.}
```
