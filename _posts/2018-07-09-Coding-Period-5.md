---

title: "Coding Period 5 (26th June - 9th July)"
comments: true
read_time: true

---

Keeping in mind our ultimate goal of this project - We want to automatically generate training data using a single command or a sinlge script, it is important to devise another script which will automatically perform all the sub-tasks. In the current scenario, there are different scripts which perform a sub-task each in a serial fashion to five us the required training set. To club this in a single script, it is important to address each of the subtask and reduce the hard-coded portions and properly define all the parameters. 

The entire pipeline can be broken down into 5 sub-tasks. 
1. Fetch property metadata
2. Get number of occurrences and URI for all properties
3. Map the fetched properties (from 1.) correctly with its URI and number of occurrences (from 2.)
4. Generate Minimal Viable Expression (MVE) for each property
5. Generate SPARQL query template and Generator Query for each property
