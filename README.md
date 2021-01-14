# Valla Interview
Question 2a
Similar cases should relate in terms of their content: the deed/crime in question, whether it is an appeal or an application, the verdict.
To measure similarity, I would perhaps use the TF-IDF, since I have prior experience with it. It combines all words from the documents into a single corpus 
and then creates a vector for each file that takes into account how often a term both is used in a particular document and how often it is seen in the corpus. In that
way an objective measurement of term importance is created. Because of the law context, perhaps n-grams can have a massive importance here. For example, "violent assault"
/"aggravated assault" can easily be outlined as different from "assault and battery", despite containing the same word. Fortunately, it is really easy to integrate
n-grams into tf-idf. Of course, as with any text data, tokenisation, stemming and other NLP techniques ought to be used if needed. Once the tf-idf vectors are
completed, the difference between the vectors (a vector space model) can be used to compare and find similar documents. Since law is very dependent on using specific 
law jargon, similar cases must include similar phrases, no matter of the circumstances, such as final verdict, the main actors, etc. If there are other factors that
might be considered important, a more complicated system with many features can be created. Usually, each feature has a weight attributed to it to regulate how
important it is. If the final verdict have a reasonable impact on the similarity, then it can be included in the system as a feature and it can be given a bigger weight.

Question 2b
User feedback can be used with an artificial intelligence approach of choice to offer accurate suggestions to users. I have no previous experience doing this, but 
research shows that it can be done with both ML approaches when a lot of feedback data is available, and with simpler approaches, such as KNN where a rich database 
is not required. User feedback can be added as a feature to the previously mentioned system and be given its own weight to match its importance.

Question 2c
Perhaps an area of importance is the legitimacy of the feedback. Although the potential clients would most likely not purposefully give wrong feedback, it is entirely
possible that some people give feedback by accident or give an exaggerated opinion (e.g. "positive" feedback when a case is only slightly relevant).
Another consideration is how often the model should be updated and how extensively it should be tested, before being put in use.
