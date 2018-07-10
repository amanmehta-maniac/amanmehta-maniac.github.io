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

Each of these sub-tasks were performed on individual level and to combine them into a single automatic step, it is important to clearly input all the requirement parameters including all the files and automize as many internal parameters as possible. Apart from this, it is also important to check if output of one command acts as a input to other (here, output of *ith* step will act as a input to *(i+1)th* step), we want to align them to such a format which is acceptable to all the sub-tasks.

During this coding duration, I precisely made improvements in the above mentioned areas. Also, another problem which occurs: currently my algorithm is able to automatically create the training data automatically only for *ontology* namespace, so there is an additional task to devise algortithms of automatization for other namespaces such as rdf-scheme, foaf, etc.

I have completed majority portions of automatization and merging of these sub-tasks until the end of this period and hope to complete minor stuff in a couple of more days to get the training dataset ready for the learner to train on! Soon, we will be able to run our first (version-1) training of NSpM learner, where the dataset is entirely automatically developed :)

