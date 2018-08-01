---
header:
  teaser: https://drive.google.com/file/d/12mt-qnUyewvp6NaKLkHsQMC_pT9dQB9C/view?usp=sharing
title: "Coding Period 7 (24th July - 6th Aug)"
comments: true
read_time: true
---



In continuation with the problems with the version-1 of our model (which was getting 11% BLEU accuracy), I discussed the output with mentors. After a day or two of error analysis, we realised that there were few trivial problems with our dataset, due to which our BLEU score was so low:

1. Double spaces: We found that there were double spaces in our dataset, and this may cause the neural network to learn different embeddings for each of the space; causing extra confusion for the NMT model.
2. URIs with () paranthesis: Some of the URIs have '(' but since we encode '(', ')' in SPARQL differently - for cases like order by(<attribute_name>) than that in NLQs - cases which contains entities like "dbr_Kalinga_(province)". These two paranthesis are being encoded, but in NLQs parathesis are a part of URI and need not be encoded (URIs should be as it is).

There were a few minor problems: such as some NLQs just did not made sense were noisy - for which we can keep a threshold frequency, but we chose to not do it right now.

After solving the above two troubles, we were good to prepare data and train the version-2 of our model. We both were hoping we get far better than mere 11%, because we guessed that "1" should be the major problem.

<figure>
    <img src="/assets/images/BLEU.png">
    <figcaption>Version-2 of our model</figcaption>
</figure>

After again a wait of 9 hours, we got ~80% BLUE accuracy for our model and this marked the correctness of this project :)..


