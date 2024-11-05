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
### So, what is a prefix? 
A prefix is a shortcut which references a URI. This prefix can then be referenced throughout the query and makes the code simpler, shorter, and more readable. Some prefixes are built into Wikidata, like property and entity. 

The property identifier prefix would be established like this:
```sql
PREFIX wdt: <http://wikidata.org/prop/direct/>
```
And the one for entity looks like this:
```sql
PREFIX wd: <http://www.wikidata.org/entity/
```
When you make more complicated queries or will use a particular URI, this will be especially helpful to create a shortcut to a particular part of the database you're querying. It is also good to know the built-in prefixes as they're used in most basic searches! Most commonly in simple queries, you will be using wdt: (for items) and wd: (for properties). Without using prefixes, the entire URI would have to be written out each time.

```sql
# Referencing Bryn Mawr College Special Collections without prefixes:
<http://wikidata.org/entity/Q101240133>

# With prefixes
wd:Q10124133
```
### SPARQL Hack!
After typing the prefix you want, press control + space on your keyboard to type out your entity/property name. This way, you don't need to memorize or search for long strings of numbers! However, if you did want to find the reference ID for a page on Wikidata, it will be in parenthesis after the title of the page. 


More information on prefixes and the list of built-in's can be found at this link: https://en.wikibooks.org/wiki/SPARQL/Prefixes#:~:text=For%20simple%20WDQS%20triples%2C%20items%20should%20be%20prefixed,fixed%20values%20%E2%80%93%20variables%20don%E2%80%99t%20get%20a%20prefix.

### Triples!
The key to SPARQL queries is understanding the semantic triple format, which will be familiar if you have prior knowledge of SQL. SPARQL views Wikidata (and all RDF databases) through being composed in this triple structure. A triple is a sequence of three entities (things) that creates a statement about semantic data. Some examples of this triple structure would be:

**Joan Baez** (subject) *has works in the collection* (predicate) **Bryn Mawr College Special Collections** (object)
**Vincent Van Gogh** (subject) *painted* (predicate) **Sunflowers** (object)

To create a SPARQL query, first think of what you want to search for in this triple format. For example, if you wanted to find all the archives located in the USA, 

### Select 
The SELECT clause defines the result set to be returned. Typically, you can select an ?item, but multiple things can be selected in one query, like an ?itemLabel or a picture (?pic). 

## Wikidata Query Builder
Wikidata offers a service to build simple SPARQL queries without knowledge of SPARQL. For the Query Builder, you will be asked to put in a property and a value, and the service will return the item and the itemLabel, creating a simple query! You can add as many conditions (using the blue button) to filter your search further, using the same property and value structure. 

Additionally, if you wanted to edit the query further, you can show the query in the Query Service. Viewing and editing the created query is also a great way to become familiar with the structure of SPARQL!

# Glossary 
There are a lot of terms relating to SPARQL and Wikidata, many of which are related but not interchangeable. SPARQL and Wikidata are built under the world and concepts of the 'Semantic Web.' If you're new to the Semantic Web, check out this article for a brief overview and explanation: https://www.ontotext.com/knowledgehub/fundamentals/what-is-the-semantic-web/#:~:text=The%20Semantic%20Web%20is%20a%20vision%20about%20an,otherwise%20existing%20content%20and%20data%20on%20the%20Web.

### Linked Data

Resource: https://www.ontotext.com/knowledgehub/fundamentals/linked-data-linked-open-data/

### Semantic Web
Machine readable version of the web. Wikidata stemmed from the concept of the Semantic Web, attemping to create (in a nutshell) a machine readable and searchable version of Wikipedia. 

### RDF (Resource Description Framework)

### Relational Database

### URI (Uniform Resource Identifier)
Provides a means of locating and retrieving information resources on a network (in this case, Wikidata). A URL (Uniform Resource Locator, which we use on the web everyday) is a specific type of URI that provides the specific location or address of a resource on the Internet (web page). However, a URI is used to define an item's identity, rather then just locate it. 
