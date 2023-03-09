# Text-Analysis-Using-Spacy-NLTK
![Capture](https://user-images.githubusercontent.com/109751694/223887566-2b1f984b-9fcb-45dc-b0fc-e8fd15bd8877.JPG)

## Install Packages
### Requirments 
autocorrect - spacy==3.0.5 - spacytextblob - wordcloud
nltk.download(type here) >>> ["stopwords","wordnet","averaged_perceptron_tagger","maxent_ne_chunker"]
!python -m spacy download en_core_web_sm

## DATA PREPROCESSING
### Preliminary Analysis


## Sentence Tokenization
### For any corpus, we first divide a huge entity into smaller entities so that they can be treated individually. Tokenization also does a similar task but upon 
### sentences in text. First, the text is broken down into sentences and that is further broken down into words. The input is given as text or a corpus. The output 
### generates a list of sentences. For example, in the text, "I love dogs. I have a dog", the output is ["I love dogs,” I have a dog”]
![download](https://user-images.githubusercontent.com/109751694/223888133-5002f43e-3197-4873-8598-4896eaacc111.png)

## Word Tokenization
### Word tokenization is the same as sentence tokenization. But, rather than applying it to sentences, it is used on words so that individual words are separated as items in a list. For example, in the sentence, "Chennai is humid,” the result is ["Chennai,” “is,” “humid”].
![download](https://user-images.githubusercontent.com/109751694/223888268-03ddccf0-46e9-43e3-8a07-1f507c5cef6e.png)

## Stopword Removal
### The dataset may contain words like ‘after,’ ‘every’ and ‘I.’ These words are not relevant to important NLP applications like the sentiment detection process. Thereby, these words can be deleted to minimize the burden on the system.
![download](https://user-images.githubusercontent.com/109751694/223888379-aa99fba2-a29f-4d04-9938-439e380a548b.jpg)

## Removal of Tags
### During web scraping, the data is scraped from web pages residing on the website, and they contain HTML tags. These tags do not provide any necessary information and hence, can be erased. For example, a tag like < body > (Body Tag) is deleted.
![download](https://user-images.githubusercontent.com/109751694/223888490-93a707a0-c00e-4c42-ad03-7243890cabf5.jpg)

## FEATURE ENGINEERING
### Encoding
#### Encoding is the process of encrypting data in a format that computers can understand. Humans comprehend natural language. However, a machine is capable of decoding only 0s and 1s. Encoding converts text to digits. For example, the words 'positive' and 'negative' are mapped to the numbers '0' and '1'.
![download](https://user-images.githubusercontent.com/109751694/223888591-10c37ff7-5302-443f-a74e-0ee99b0b5be4.png)

## POS Tagger
### POS tagger is parts of speech tagger that is an in-built function found in a standard library. It tags the words in the sentences according to the grammar of the langauge. For example, in the text, “The pizza was disgusting but the location was beautiful”, the result after implementing POS tagger will be [“The [DT]”, “pizza [NN]”, “is [VB]”, “disgusting [VBG]”, “but [CC]”, “the [DT]”, “location [NN]”, “was [VBD], “beautiful [JJ]].
![download](https://user-images.githubusercontent.com/109751694/223888646-d1e95660-56c6-4fc1-b3ad-d38c0ad6739b.png)


## N-Gram 
### N-gram is a language model widely used in NLP and is applied to statistical problems involving text and audio. It is a probabilistic model that predicts the next series of words. For example, in the sentence, “The movie was boring.” Unigram processes the text as [“The”, “movie”, “was”, “boring”]. Bi-gram processes the text as [“The movie”, “movie was”, “was boring”]. Tri-gram processes the text as [“The movie was”, “movie was boring”]

![download](https://user-images.githubusercontent.com/109751694/223888712-8999ad0f-4901-45cd-990c-5c2fccb0fb25.png)

## Bag of Words
### The bag of words carries out sentence tokenization and word tokenization. After that, it counts the number of appearances of each word. For example, in a sentence, “It is nice but horrid, and that’s not a nice thing.” The word “nice” is extracted and countered with two occurrences.

![download](https://user-images.githubusercontent.com/109751694/223888763-d38aadb3-cfdb-43f0-965a-5570a4ab9ca0.jpg)

## Term Frequency

### TF – Term Frequency is described as the number of times that a term occurs in a document. It considers all the terms of equal importance. For example, the word “Fruit” appears five times in a document of 100 words, then the TF for “Fruit” is 5/100 = 0.05.
![download](https://user-images.githubusercontent.com/109751694/223888906-f295db72-da59-4bc9-9c20-ad47ec3d5a11.png)

## Term Frequency - Inverse Document Frequency

### TF-IDF – Term Frequency-Inverse Document Frequency is described as the importance of a word in a document, which is proportional to the number of times the word appears in the document. For example, the word “Fruit” appears in 100 of 10000 documents and the term frequency is 5 then the TF-IDF is 0.05 * log(10000/100) = 5 * 2 = 10.

![download](https://user-images.githubusercontent.com/109751694/223888921-205c3d82-062d-4e36-b750-af3776cee706.png)

## Dependency Parser

### Stanford dependency parser establishes the relationship between entities in the language using grammatical rules. The output of the parser is a tree structure that is annotated. For example, in the sentence “The funny boy joked,” “funny” is an adjective for the noun “boy.”
![download](https://user-images.githubusercontent.com/109751694/223889048-fee08fcc-9405-4458-b94a-18c199972b2d.png)
![Capture3](https://user-images.githubusercontent.com/109751694/223889133-4b8c877f-8810-4a84-a831-91a65ba3419c.JPG)

## Named Entity Recognition

### NER - Named Entity Recognition is the process of extracting proper nouns or proper noun phrases. For example, in the sentence 'Robert is interested in Amazon', the entities 'Robert' (Name) and 'Amazon' (Organization) are selected.


## Sentiment Analysis

### Sentimental analysis plays a significant role in determining the polarity of a review or a comment. It is used to know whether the person is talking about something in a positive way or a negative way. It can be classified broadly into positive, negative, and neutral. For example, on a tourism website, a person leaves a remark stating, “There are beautiful tourist spots in Switzerland. “The word ‘beautiful’ is positive as it describes Switzerland as pretty.

![download](https://user-images.githubusercontent.com/109751694/223889250-4b1e38bf-a898-4dd8-bd14-f28ebc549d22.png)

## Subjectivity Detection

### Subjectivity Detection relies upon the answer to the question "Is it based on facts or opinions?". For example, the sentence 'I love cats' is subjective and the sentence 'Cats have tails' is objective.

![download](https://user-images.githubusercontent.com/109751694/223889538-ae077a89-2a02-4509-aa2e-df8bd64423ff.jpg)


