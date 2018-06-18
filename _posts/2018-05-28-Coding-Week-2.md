---

title: "Coding Period - Week 2"
comments: true
read_time: true

---
After completing metadata extraction for a subset of properties, next step is to expand this to get ALL (more than 20k for large classes such as Place) properties for Place class. But, there is a notion of *timeout* (around 20 sec) which restricts the time that a single SPARQL query can take for it's execution. This timeout is kept, to distribute DBpedia's knowledge *equally* among all it's users and to make sure a sinlge user is not exhausting majority of resources. I, along with Tomasso, tried to tackle this using: 
> OFFSET and LIMIT keywords

but got strange results. 

So, we decided to switch from SPARQL to http://mappings.dbpedia.org/. This web page has properties majorly from ontology namespace which are correct (with more confidence). 

The next step, hence became to systematically web-scrape the web page and store it.  I began with web-scraping during the end of the week.




