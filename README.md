# Text-Summay-generation

TEXTRANK is an extractive and unsupervised text summarization technique.Unlike PageR-
ank Method,we are using Sentences in places of Webpages.Similarity between any
two sentences is used as an equivalent to the web page transition probability.The
similarity scores are stored in a square matrix, similar to the matrix M used for
PageRank.  
Flow of algorithm that we will be following:

STEP 1
The first step would be to concatenate all the text contained in the articles.Then split
the text into individual sentences.Remove punctuations, numbers and special char-
acters.Make alphabets lowercase.Get rid of the stopwords (commonly used words of
a language { is, am, the, of, in, etc.) present in the sentences.Removal of Stopwords
are necessary because these words occurs most number of times, frequency wise
dominate every sentences and serves no real purpose.

STEP 2
In the next step, we will find vector representation (word embedding) for each
and every sentence.Vectorizing of sentences means representing sentences in numer-
ical form. It is not possible to perform mathematical operations on words, alpha-
bets Hence vectorizing a sentence mean to convert and represent in mathematical
way.There are two ways of representing in vector format.In traditional textRank
method we use 0 and 1 for encoding sentences in vector format but in this technique
we are using TF-IDF technique so that we can more properly evaluates how relevant
a word is to a document in a collection of documents.

STEP 3
Similarities between sentence vectors are then calculated and stored in a matrix.A sim-
ilarity matrix is a matrix of scores which express the similarity between two data
points, In this case data points represent sentence vectors.It is basically a cosine dot
product. if two sentences are identical then we call it cosine value 1 and if have no
words in common then cosine value would turn out to be zero.

STEP 4
The similarity matrix is then converted into a graph, with sentences as vertices
and similarity scores as edges, for sentence rank calculation. This is then used for
iterations corresponding to PageRank Algorithm.
The PageRank algorithm outputs a probability distribution used to represent
the likelihood that a person randomly clicking on links will arrive at any particular
page. PageRank can be calculated for collections of documents of any size. It is
assumed in several research papers that the distribution is evenly divided among
all documents in the collection at the beginning of the computational process. The
PageRank computations require several passes, called "iterations", through the col-
lection to adjust approximate PageRank values to more closely reect the theoretical
true value.

STEP 5
Finally, a certain number of top-ranked sentences form the final summary,Based on
scores of each sentences.
