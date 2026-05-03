```python
! pip install --upgrade pip
```

    Requirement already satisfied: pip in ./anaconda3/lib/python3.13/site-packages (26.0.1)
    Collecting pip
      Using cached pip-26.1-py3-none-any.whl.metadata (4.6 kB)
    Using cached pip-26.1-py3-none-any.whl (1.8 MB)
    Installing collected packages: pip
      Attempting uninstall: pip
        Found existing installation: pip 26.0.1
        Uninstalling pip-26.0.1:
          Successfully uninstalled pip-26.0.1
    Successfully installed pip-26.1



```python
import nltk
```


```python
! pip install requests beautifulsoup4
```

    Requirement already satisfied: requests in ./anaconda3/lib/python3.13/site-packages (2.32.3)
    Requirement already satisfied: beautifulsoup4 in ./anaconda3/lib/python3.13/site-packages (4.12.3)
    Requirement already satisfied: charset-normalizer<4,>=2 in ./anaconda3/lib/python3.13/site-packages (from requests) (3.3.2)
    Requirement already satisfied: idna<4,>=2.5 in ./anaconda3/lib/python3.13/site-packages (from requests) (3.7)
    Requirement already satisfied: urllib3<3,>=1.21.1 in ./anaconda3/lib/python3.13/site-packages (from requests) (2.3.0)
    Requirement already satisfied: certifi>=2017.4.17 in ./anaconda3/lib/python3.13/site-packages (from requests) (2025.4.26)
    Requirement already satisfied: soupsieve>1.2 in ./anaconda3/lib/python3.13/site-packages (from beautifulsoup4) (2.5)



```python
import requests
from bs4 import BeautifulSoup

url = "https://en.wikipedia.org/wiki/Natural_language_processing"


headers = {"User-Agent": "MyApp/1.0"}

response = requests.get(url, headers=headers)

soup = BeautifulSoup(response.text, "html.parser")

data = soup.get_text()


```


```python
#### sentence spilting 

import nltk
from nltk.tokenize import sent_tokenize  

nltk.download("punkt")

sentence = sent_tokenize(data)


```

    [nltk_data] Downloading package punkt to /home/s2000/nltk_data...
    [nltk_data]   Package punkt is already up-to-date!



```python
#### remove special characters using regex 
import re 

clean_data = []

for s in sentence:
    temp = re.sub("[^a-zA-Z]","",s)
    clean_data.append(temp)


```


```python
# tokenization 

import nltk
from nltk.tokenize import word_tokenize

nltk.download('punkt')

sentences = clean_data

tokens = []
for i in sentences:
    words = word_tokenize(i)
    tokens.append(words)


```

    [nltk_data] Downloading package punkt to /home/s2000/nltk_data...
    [nltk_data]   Package punkt is already up-to-date!



```python
### stop words 
import nltk
from nltk.corpus import stopwords

nltk.download('stopwords')



stop_words = stopwords.words("english")



filtered = []

for w in clean_data:
    if w not in stop_words:
        filtered.append(w)



```

    [nltk_data] Downloading package stopwords to /home/s2000/nltk_data...
    [nltk_data]   Package stopwords is already up-to-date!



```python
# stemming 

from nltk.stem import PorterStemmer

words = filtered

ps = PorterStemmer()

stemmed = []
for w in words:
    stemmed.append(ps.stem(w))


```


```python
import nltk

from nltk.stem import WordNetLemmatizer

nltk.download('wordnet')

words = ["test","lifes","turbos"]

lm = WordNetLemmatizer()

lemmanization = []

for w in words:
    lemmatized.append(lm.lemmatize(w))

print(lemmatized)
```

    ['running', 'better', 'car', 'test', 'life', 'turbos', 'test', 'life', 'turbos']


    [nltk_data] Downloading package wordnet to /home/s2000/nltk_data...
    [nltk_data]   Package wordnet is already up-to-date!



```python
# suffix stripping 

def strip_suffix(word):
    if word.endswith("ing"):
        return word[:-3]
    if word.endswith("ed"):
        return word[:-2]
    if word.endswith("ly"):
        return word[:-2]
    if word.endswith("s"):
        return word[:-1]

words = ["doing","ending","langihing","funny"]
result = []

for w in words:
    result.append(strip_suffix(w))

print(result)
```

    ['do', 'end', 'langih', None]



```python
#### same execrise repeat again 
### new stuff 
```


```python
text_new = "Natural Language Processing is a very interesting field of Artificial Intelligence. It helps computers understand human language. I am learning NLP and practicing different techniques every day. It includes tasks like tokenization, stop word removal, stemming, and lemmatization. Many applications like chatbots, translation systems, and voice assistants use NLP. I am enjoying learning it and improving my skills by working on examples, writing code, and testing different sentences."
```


```python
import nltk
import re

from nltk.tokenize import sent_tokenize , word_tokenize  ## word tokenize and sent_tokenize
from nltk.corpus import stopwords  # corpous for stop words 
from nltk.stem import PorterStemmer , WordNetLemmatizer #stemming and lemmanitozations 
```


```python
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
```

    [nltk_data] Downloading package punkt to /home/s2000/nltk_data...
    [nltk_data]   Package punkt is already up-to-date!
    [nltk_data] Downloading package stopwords to /home/s2000/nltk_data...
    [nltk_data]   Package stopwords is already up-to-date!
    [nltk_data] Downloading package wordnet to /home/s2000/nltk_data...
    [nltk_data]   Package wordnet is already up-to-date!





    True




```python
### sentence level splitting 

sentences = sent_tokenize(text_new)
print(sentences)
```

    ['Natural Language Processing is a very interesting field of Artificial Intelligence.', 'It helps computers understand human language.', 'I am learning NLP and practicing different techniques every day.', 'It includes tasks like tokenization, stop word removal, stemming, and lemmatization.', 'Many applications like chatbots, translation systems, and voice assistants use NLP.', 'I am enjoying learning it and improving my skills by working on examples, writing code, and testing different sentences.']



```python
## specail characters removal process - regex 
token_list = []
for s in sentences:
    temp = re.sub("[^a-zA-Z ]"," ",s)
    token_list.append(temp)

print(token_list)

```

    ['Natural Language Processing is a very interesting field of Artificial Intelligence ', 'It helps computers understand human language ', 'I am learning NLP and practicing different techniques every day ', 'It includes tasks like tokenization  stop word removal  stemming  and lemmatization ', 'Many applications like chatbots  translation systems  and voice assistants use NLP ', 'I am enjoying learning it and improving my skills by working on examples  writing code  and testing different sentences ']



```python
### word tokenization 

token_words= []
for s in token_list:
    token_words.append(word_tokenize(s))

print(token_words)


```

    [['Natural', 'Language', 'Processing', 'is', 'a', 'very', 'interesting', 'field', 'of', 'Artificial', 'Intelligence'], ['It', 'helps', 'computers', 'understand', 'human', 'language'], ['I', 'am', 'learning', 'NLP', 'and', 'practicing', 'different', 'techniques', 'every', 'day'], ['It', 'includes', 'tasks', 'like', 'tokenization', 'stop', 'word', 'removal', 'stemming', 'and', 'lemmatization'], ['Many', 'applications', 'like', 'chatbots', 'translation', 'systems', 'and', 'voice', 'assistants', 'use', 'NLP'], ['I', 'am', 'enjoying', 'learning', 'it', 'and', 'improving', 'my', 'skills', 'by', 'working', 'on', 'examples', 'writing', 'code', 'and', 'testing', 'different', 'sentences']]



```python
#### remove stop words 
token_words_filtered = []

stop_words = stopwords.words("english")

for sentence in token_words:
    for words in sentence:
        if words.lower() not in stop_words:
            token_words_filtered.append(words)

print(token_words_filtered)
            
```

    ['Natural', 'Language', 'Processing', 'interesting', 'field', 'Artificial', 'Intelligence', 'helps', 'computers', 'understand', 'human', 'language', 'learning', 'NLP', 'practicing', 'different', 'techniques', 'every', 'day', 'includes', 'tasks', 'like', 'tokenization', 'stop', 'word', 'removal', 'stemming', 'lemmatization', 'Many', 'applications', 'like', 'chatbots', 'translation', 'systems', 'voice', 'assistants', 'use', 'NLP', 'enjoying', 'learning', 'improving', 'skills', 'working', 'examples', 'writing', 'code', 'testing', 'different', 'sentences']



```python
#### stemming  -> filtered
stemp_list = []

ps = PorterStemmer()

print(ps)

for i in token_words_filtered:
    stemp_list.append(ps.stem(i))

print(stemp_list)
    
```

    <PorterStemmer>
    ['natur', 'languag', 'process', 'interest', 'field', 'artifici', 'intellig', 'help', 'comput', 'understand', 'human', 'languag', 'learn', 'nlp', 'practic', 'differ', 'techniqu', 'everi', 'day', 'includ', 'task', 'like', 'token', 'stop', 'word', 'remov', 'stem', 'lemmat', 'mani', 'applic', 'like', 'chatbot', 'translat', 'system', 'voic', 'assist', 'use', 'nlp', 'enjoy', 'learn', 'improv', 'skill', 'work', 'exampl', 'write', 'code', 'test', 'differ', 'sentenc']



```python
## lemmatization -> filtered list

lm = WordNetLemmatizer()

lemma_list_test = []

for text in token_words_filtered:
    lemma_list_test.append(lm.lemmatize(text))

print(lemma_list_test)

```

    ['Natural', 'Language', 'Processing', 'interesting', 'field', 'Artificial', 'Intelligence', 'help', 'computer', 'understand', 'human', 'language', 'learning', 'NLP', 'practicing', 'different', 'technique', 'every', 'day', 'includes', 'task', 'like', 'tokenization', 'stop', 'word', 'removal', 'stemming', 'lemmatization', 'Many', 'application', 'like', 'chatbots', 'translation', 'system', 'voice', 'assistant', 'use', 'NLP', 'enjoying', 'learning', 'improving', 'skill', 'working', 'example', 'writing', 'code', 'testing', 'different', 'sentence']



```python
## suffix stripping 

def strip_suffix(word):
    if word.endswith("ing"):
        return word[:-3]
    if word.endswith("ed"):
        return word[:-2]
    if word.endswith("s"):
        return word[:-1]
    return word 

new_custom_list = []

for words in token_words_filtered:
    new_custom_list.append(strip_suffix(words))

print(new_custom_list)
```

    ['Natural', 'Language', 'Process', 'interest', 'field', 'Artificial', 'Intelligence', 'help', 'computer', 'understand', 'human', 'language', 'learn', 'NLP', 'practic', 'different', 'technique', 'every', 'day', 'include', 'task', 'like', 'tokenization', 'stop', 'word', 'removal', 'stemm', 'lemmatization', 'Many', 'application', 'like', 'chatbot', 'translation', 'system', 'voice', 'assistant', 'use', 'NLP', 'enjoy', 'learn', 'improv', 'skill', 'work', 'example', 'writ', 'code', 'test', 'different', 'sentence']



```python
nltk.download('punkt')
nltk.download('averaged_perceptron_tagger') #  pos
```

    [nltk_data] Downloading package punkt to /home/s2000/nltk_data...
    [nltk_data]   Package punkt is already up-to-date!
    [nltk_data] Downloading package averaged_perceptron_tagger to
    [nltk_data]     /home/s2000/nltk_data...
    [nltk_data]   Package averaged_perceptron_tagger is already up-to-
    [nltk_data]       date!





    True




```python
## pos tagging 
import nltk

from nltk.tokenize import word_tokenize 

pos_tagged = nltk.pos_tag(token_words_filtered)

pos_tagged
```




    [('Natural', 'JJ'),
     ('Language', 'NNP'),
     ('Processing', 'NNP'),
     ('interesting', 'JJ'),
     ('field', 'NN'),
     ('Artificial', 'NNP'),
     ('Intelligence', 'NNP'),
     ('helps', 'VBZ'),
     ('computers', 'NNS'),
     ('understand', 'VBP'),
     ('human', 'JJ'),
     ('language', 'NN'),
     ('learning', 'VBG'),
     ('NLP', 'NNP'),
     ('practicing', 'VBG'),
     ('different', 'JJ'),
     ('techniques', 'NNS'),
     ('every', 'DT'),
     ('day', 'NN'),
     ('includes', 'VBZ'),
     ('tasks', 'NNS'),
     ('like', 'IN'),
     ('tokenization', 'NN'),
     ('stop', 'NN'),
     ('word', 'NN'),
     ('removal', 'NN'),
     ('stemming', 'VBG'),
     ('lemmatization', 'NN'),
     ('Many', 'JJ'),
     ('applications', 'NNS'),
     ('like', 'IN'),
     ('chatbots', 'JJ'),
     ('translation', 'NN'),
     ('systems', 'NNS'),
     ('voice', 'NN'),
     ('assistants', 'NNS'),
     ('use', 'VBP'),
     ('NLP', 'NNP'),
     ('enjoying', 'VBG'),
     ('learning', 'VBG'),
     ('improving', 'VBG'),
     ('skills', 'NNS'),
     ('working', 'VBG'),
     ('examples', 'NNS'),
     ('writing', 'VBG'),
     ('code', 'NN'),
     ('testing', 'VBG'),
     ('different', 'JJ'),
     ('sentences', 'NNS')]




```python
## CFG context free grammer 
### s (sentence)
### NP noun phrase
### VP verb phrase
#### Det N -> determiner + Noun
#### N (Noun)
#### V (verb)
#### V NP -> verb + Noun phrase

#### Adjective pharase
#### Adjp -> Adj | Adj AdjP
#### Adj -> 'big' | 'small'

#### Adverb Phrase
#### AdvP -> Adv
#### Adv -> 'quickly' \ 'slowly'

#### prepositional phrase
#### pp -> P NP
#### p -> 'in' | 'on' | 'with'

#### Expanded Verb phrase 
## VP -> V NP | V NP PP | v pp \ v Advp

##### pronoun 
### prp

##### conjeunction 
### S -> S Conj S \ and | but

nltk.download('punkt')
nltk.download('averaged_perceptron_tagger')
nltk.download('treebank')
nltk.download('maxent_treebank_pos_tagger')
nltk.download('maxent_ne_chunker')
nltk.download('words')



```

    [nltk_data] Downloading package punkt to /home/s2000/nltk_data...
    [nltk_data]   Package punkt is already up-to-date!
    [nltk_data] Downloading package averaged_perceptron_tagger to
    [nltk_data]     /home/s2000/nltk_data...
    [nltk_data]   Package averaged_perceptron_tagger is already up-to-
    [nltk_data]       date!
    [nltk_data] Downloading package treebank to /home/s2000/nltk_data...
    [nltk_data]   Package treebank is already up-to-date!
    [nltk_data] Downloading package maxent_treebank_pos_tagger to
    [nltk_data]     /home/s2000/nltk_data...
    [nltk_data]   Unzipping taggers/maxent_treebank_pos_tagger.zip.
    [nltk_data] Downloading package maxent_ne_chunker to
    [nltk_data]     /home/s2000/nltk_data...
    [nltk_data]   Unzipping chunkers/maxent_ne_chunker.zip.
    [nltk_data] Downloading package words to /home/s2000/nltk_data...
    [nltk_data]   Unzipping corpora/words.zip.





    True




```python
import nltk
from nltk import CFG
from nltk.parse import ChartParser


grammer = CFG.fromstring(
    """
    S -> NP VP
    NP -> DET N | 'I'
    VP -> V NP | V 

    Det -> 'the' | 'a'
    N -> 'dog' | 'cat'
    V -> 'saw' | 'ate'
    """
)
parser = ChartParser(grammer)

sentence = "I saw the dog"
words = sentence.split()

for tree in parser.parse(words):
    print(tree)
    tree.pretty_print()

```


```python
## ngram --> tokenized words 

import nltk

from nltk import ngrams 
from collections import Counter 

nltk.download('punkt')

text = token_words_filtered

unigram = list(ngrams(text,1))
bigram = list(ngrams(text,2))
trigram = list(ngrams(text,3))

dict_grams = {
    "unigram":unigram,
    "bigram":bigram,
    "trigram":trigram
}

uni_count = Counter(unigram)
bi_count = Counter(bigram)
trigram = Counter(trigram)

dict_gram_count = {
    "unigram_count":uni_count,
    "bigram":bigram,
    "trigram":trigram
}


```

    [nltk_data] Downloading package punkt to /home/s2000/nltk_data...
    [nltk_data]   Package punkt is already up-to-date!



```python

```


```python
#### hidden markov model
import nltk
from nltk.corpus import treebank
from nltk.tag import hmm

nltk.download('treebank')

train_data = treebank.tagged_sents()[:3000] ## train _ data tags 
test_data = treebank.tagged_sents()[3000:3100] ## test _ data tags

trainer = hmm.HiddenMarkovModelTrainer()
hmm_tagger = trainer.train(train_data)

### predict tags 
print(hmm_tagger.tag(token_words_filtered))

print("accuracy", hmm_tagger.evaluate(test_data))


```

    [nltk_data] Downloading package treebank to /home/s2000/nltk_data...
    [nltk_data]   Package treebank is already up-to-date!


    [('Natural', 'NNP'), ('Language', 'NNP'), ('Processing', 'NNP'), ('interesting', 'NNP'), ('field', 'NNP'), ('Artificial', 'NNP'), ('Intelligence', 'NNP'), ('helps', 'NNP'), ('computers', 'NNP'), ('understand', 'NNP'), ('human', 'NNP'), ('language', 'NNP'), ('learning', 'NNP'), ('NLP', 'NNP'), ('practicing', 'NNP'), ('different', 'NNP'), ('techniques', 'NNP'), ('every', 'NNP'), ('day', 'NNP'), ('includes', 'NNP'), ('tasks', 'NNP'), ('like', 'NNP'), ('tokenization', 'NNP'), ('stop', 'NNP'), ('word', 'NNP'), ('removal', 'NNP'), ('stemming', 'NNP'), ('lemmatization', 'NNP'), ('Many', 'NNP'), ('applications', 'NNP'), ('like', 'NNP'), ('chatbots', 'NNP'), ('translation', 'NNP'), ('systems', 'NNP'), ('voice', 'NNP'), ('assistants', 'NNP'), ('use', 'NNP'), ('NLP', 'NNP'), ('enjoying', 'NNP'), ('learning', 'NNP'), ('improving', 'NNP'), ('skills', 'NNP'), ('working', 'NNP'), ('examples', 'NNP'), ('writing', 'NNP'), ('code', 'NNP'), ('testing', 'NNP'), ('different', 'NNP'), ('sentences', 'NNP')]


    /tmp/ipykernel_229250/4046971709.py:17: DeprecationWarning: 
      Function evaluate() has been deprecated.  Use accuracy(gold)
      instead.
      print("accuracy", hmm_tagger.evaluate(test_data))


    accuracy 0.3767482517482518



```python
#### test
import nltk
from nltk.corpus import treebank
from sklearn_crfsuite import CRF

nltk.download('treebank')

# Load data
sentences = treebank.tagged_sents()

# -------- Feature function --------
def word2features(sent, i):
    word = sent[i][0]

    features = {}
    features['word'] = word
    features['lower'] = word.lower()
    features['is_upper'] = word.isupper()
    features['is_digit'] = word.isdigit()

    return features

# -------- Prepare training data --------
X = []
y = []

for sent in sentences:
    features_list = []
    label_list = []

    for i in range(len(sent)):
        features = word2features(sent, i)
        features_list.append(features)

        label = sent[i][1]
        label_list.append(label)

    X.append(features_list)
    y.append(label_list)

# -------- Train-test split --------
X_train = X[:3000]
X_test = X[3000:3100]

y_train = y[:3000]
y_test = y[3000:3100]

# -------- Train CRF model --------
crf = CRF(max_iterations=50)
crf.fit(X_train, y_train)

# -------- Test on new sentence --------
test_sentence = ["I", "saw", "a", "dog"]

test_features = []
for i in range(len(test_sentence)):
    temp = []
    temp.append((test_sentence[i], ""))   # dummy tag
    f = word2features(temp, 0)
    test_features.append(f)

prediction = crf.predict([test_features])

# -------- Print result --------
for i in range(len(test_sentence)):
    print(test_sentence[i], "->", prediction[0][i])
```

    [nltk_data] Downloading package treebank to /home/s2000/nltk_data...
    [nltk_data]   Package treebank is already up-to-date!


    I -> PRP
    saw -> VBD
    a -> DT
    dog -> NN



```python

```
