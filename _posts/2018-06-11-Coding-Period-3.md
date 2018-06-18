---

title: "Coding Period 3 (28th May - 11th June)"
comments: true
read_time: true

---

During this week, I web-scraped [this](http://mappings.dbpedia.org/server/ontology/classes/Place) web page to get all the *important* metadata information about Place properties (for ontology mapping only) and stored them in a csv.

After capturing the metadata information of Place properties, we shifted back to our main aim - to think of ways to automate the query template generation using this metadata information. We mutually decided it would be best to try out completing query templates for a random set of properties manually to learn out pattern/heuristic to automate the task.

So, during the first week of the period, I completed the query templates manually for ~150 properties and shared with my mentor for feedback. And I was able to design a simple hueristics which could generate query for ~85% of properties with confidence score >=0.5 (this was a fuzzy score manually given by me again). The template generation for the remaining set, seemed trickier and hence I could not formulate a heuristic for this set. Also, there were couple of shortcomings:

1. For many of the properties, there were more than a single unique way in which an NLQ could be generated. This gave rise to the idea of having two expressions for a single property - a) Most Viable Expression (MVE) b) Optimal Expression
2. Since the entire annotation was done manually, there were cases where another NLQ *better* than the one I had mentioned existed. This gave rise to the possibility of having more than one verbal form for a given properties' query, and it became trickier to choose one out of the candidates. Due to this issue I proposed to take help from existing language tools/models which can help us predict the next word of a sequence and help us discriminate which query suits better among the candidates.

So, I shared these ideas with my mentors and we decided to spend the next week to develop two expressions for the manual annotation and try out existing language tools for the issue of verbal forms.

During the next week (4th June - 11th June), I developed MVE and Optimal Expressions for the same random set. This would essentially form gold-standard for our NLQ to SPARQL task. I got it reviewed from Tommaso sir after completion and made the required changes as suggested by him. 

During the later half of the week, I built a couple of language tools. I tried examples from the manual set to judge their performance and to see if these tools are helpful for the specific problem we have. None of them after testing prove to be of any help to us. 

After this period, we mutually concluded to move forward with the heuristics for ~85% properties and try to build a simple decision tree model over it. On the later stage, we can come back to looking at this problem. Also, before the decision tree model, it was important to map this manual annotated data with the actual URIs of the properties and also the number of occurrences of these properties. 

