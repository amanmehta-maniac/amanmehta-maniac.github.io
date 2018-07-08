---

title: "Coding Period 4 (12th June - 25th June)"
comments: true
read_time: true

---

Moving forward with the experiment to automatically generate training data for NSpM learner, our next step is to remove noisy rows from the dataset. Since the properties are extracted from a web-page, it may have some properties which are errorneous and we do not want such rows. For this, I and Tommaso decided to categorize a row as legit or noisy depending number of occurences of a property in the entire DBpedia. During this week, we used SPARQL endpoint to fetch the number of occurrences of all properties of domain dbo:Place (Place class of DBpedia). 

Once this data was available, I built a python script *integrate.py* to integrate this data into our training data by adding two new columns - URI and Number of Occurrences correponding to the row. We will now use a *Threshold* value for number of occurrences of a property. Rows which fail to cross this threshold value will be labelled as noisy and will be removed from the dataset. We will solidify this threshold value later.

The NSpM learner's training queries in *NLQ* (English in our case) are ready at this stage. I, with the help mentors, have successfully build the NLQ portion of dataset **entirely automatic**. Our next step is to extend this training data to include the other half of each training sample - their correponsding queries in *SPARQL language*. 

Building queries in SPARQL language required two separate queries - a) SPARQL Query Template, b) Generator Query corresponding to a). SPARQL Query Template is a SPARQL query for NLQ with Placeholders for Objects. These Placeholders are populated using Generator Queries.

So, in the remaining half of the Period, I devised a simple algorithm to populate a) and b) columns of the training data *automatically* (using another python script - sparql_generator.py). This completes our second half of the training data for the Learner. 


