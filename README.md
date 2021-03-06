# IASNLP15-Question_Answering_Google
This project aims at building a simple Web scale QA system, which uses Google search results for answer extraction and ranks the results with the help of the designed algorithm. It has mainly 4 steps involved

### 1. Question Classification
We use a Li-Roth based classifier using Support Vector Machines (SVM), where we get the coarse grained class as well as the fine grained class.

### 2. Answer Retrieval
In this step, we use the Google Web Search API for sending queries to Google, from which we can get maximum of 8 results for a page request. Then we fire up the complete question of the user to Google for retrieving the answers.

### 3. Phrase & Named Entity Extraction
The Phrase & Named Entity Extractor tries to extract the noun phrases from the search results content using the NLTK (Natural Language ToolKit) chunker. Then we try to extract named entities using Stanford's Named Entity Recognizer.

### 4. Answer Extraction & Ranking
This is the final step involved where we try to extract all the different noun phrases and compare its Entity with the Answer and its type of question. Then we rank the matched noun phrases based on the frequency of the noun phrase occurrence in different search results. The high ranked nouns will be given as output to the user.
