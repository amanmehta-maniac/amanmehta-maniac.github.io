---

title: "Coding Period - Week 2"
comments: true
read_time: true

---
After completing metadata extraction for a subset of properties, next step is to expand this to get ALL (more than 20k for large classes such as Place) properties for Place class. But, there is a notion of *timeout* which restricts the time that a single SPARQL query can take for it's execution. This timeout is kept, to distribute DBpedia's knowledge *equally* among all it's users and to make sure a sinlge user is not exhausting majority of resources. I, along with Tomasso, tried to tackle this using: 
> OFFSET
> LIMIT 
keywords but got strange results. 





* Found out few bugs while quering DBpedia SPARQL

