# NLP Language-Model

The primary objective of this project is to learn a language model from different kind of corpuses 
and try to output a meaning full English sentence.

The corpuses selected for this purpose are as follows:
1. Brown corpus
2. Gutenberg corpus
3. Reuters corpus

The code consists of three main classes representing the language models namely:
1. Unigram
2. Bigram
3. Trigram

It also has a sampler class which is used to sample the words at random from the language model once the training is done.

Each of the corpus mentioned above is split into 3 sections as train/dev/test. 
The train section is used for training the language model and the dev test is used for cross validation

The measure of accuracy used in this project is perplexity which is defined as

Perplexity = 2^(-avg prob(w)) where w is a sequence of words in the sentence. Lower the perplexity better the language model
Perplexity = 1 Language model is very good
Perplexity = V(#words) language model is very bad

For each of the above mentioned model the project also trains an exponential backoff version.

<b>What is Exponential Backoff?:</b>
We add a small probability term to the language model in case it encounters a completely new sequence of words to solve the zero probability problem also called laplacian smoothing
 
The project evaluates the performance of the language model in terms of perplexity by varying the laplacian smoothing constant for trigram model.
 
It compares the different models learned from each corpus accross different corpuses and shows the results.
 
For code, results and graphs please view the <a href="https://github.com/adityajoshi1994/Language-Model/blob/master/Language%20modeling.ipynb"> file </a>
