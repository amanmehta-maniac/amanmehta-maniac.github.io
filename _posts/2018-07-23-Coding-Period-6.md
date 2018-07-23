---

title: "Coding Period 6 (10th July - 23rd July)"
comments: true
read_time: true

---

During the initial stages of this duration, I completed final formatting steps to get the templates ready. In a few days, the training templates were ready to generate dataset! I began with generation of the dataset and finished it in a day, there were a couple of proxy issues which caught up my entire day [:|]. There is a hyper-parameter to create a dataset: EXAMPLES_PER_TEMPLATE (let's call it *ex* for ease), which as the name suggests, uses SPARQL endpoint to get that many number of <S,P,O> pairs in the dataset. For starters, (just to check if the data-generation process is flawless) I took *ex* = 1.

The data-preparation took around 8mins to complete. And as I had guessed, there were a few bugs in the preparation step, which I fixed and now we were ready to prepare the dataset for larger values of *ex* say, 300 or 600. The size of dataset with *ex* = 300 and *ex* = 600 were around 44k and 77k which looked alright and we are now ready to train!

The next step is to start training our model using the generated dataset and evaluate the model. This step involves large computations and takes way too longer to finish on CPUs. We had already talked out with Ricardo sir, who were going to provide me access to *Oculus* (one of University of Paderborn's server). But to use it remotely, I had to set-up a VPN connection to connect to their local college network. Even after a lot of disscussions with the servers guys at UPB and a lot of self-reading online, I wasn't able to successfully connect to their local college network remotely. The two major reasons of not-able-to-connect (IMO) are:
1. Auth-type = Certificates (TLS): I require network-certificates and a personal key (certified at UPB servers) to be able to connect to their servers, which I haven't yet been provided.
2. Auth-type = username-password: I was told that my login credentials to IMT server portal will indeed allow me to connect to their network, but the authorisation failed. 
This trying went on for around a week. I then decided to take help from one of my friend's server to run the training model. 


