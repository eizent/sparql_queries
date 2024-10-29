# SPARQL and SPARQL Queries!

## What is SPARQL? 
SPARQL (pronounced 'sparkle' :sparkles:) is a query language for the Semantic Web, including Wikidata. Using SPARQL, users can easily search and filter data within an RDF (Resource Description Framework) format to their specifications. It uses much of the same logic as SQL, and is composed using 'triple statements.' This takes the form of subject-predicate-object, where in SPARQL the URIs (Uniform Resource Identifiers) would be used, and a triple could also be described as entity identifier-attribute name-attribute value. 

## Basic Syntax of a Query

```sql
PREFIX prefix_short_name: <prefix_full_uri>

SELECT ?item
WHERE {
    subject_uri predicate_uri oject_uri.
}
```

## Wikidata Query Builder
Wikidata offers a service to build simple WIki 

# Glossary 
There are a lot of terms relating to SPARQL and Wikidata, many of which are related but not interchangeable. If you're new to the Semantic Web, check out this article for a brief overview: https://www.ontotext.com/knowledgehub/fundamentals/what-is-the-semantic-web/#:~:text=The%20Semantic%20Web%20is%20a%20vision%20about%20an,otherwise%20existing%20content%20and%20data%20on%20the%20Web.

### Linked Data

### Semantic Web
Machine readable version of the web. Wikidata stemmed from the concept of the Semantic Web, attemping to create (in a nutshell) a machine readable and searchable version of Wikipedia. 

### RDF (Resource Description Framework)

### URI (Uniform Resource Identifier)
Provides a means of locating and retrieving information resources on a network (in this case, Wikidata). A URL (Uniform Resource Locator, which we use on the web everyday) is a specific type of URI that provides the specific location or address of a resource on the Internet (web page). However, a URI is used to define an item's identity, rather then just locate it. 
