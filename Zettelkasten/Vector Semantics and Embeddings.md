***
## Table of contents
[TF-IDF](##TF-IDF)



## Words and Vectors
- word representation as sparse long vectorwith dimensions corresponding to words in vocabulary or documents
### Term-document matrix: column vector
### Term-document matrix: row vector
### Term-term matrix
- use window around to count context words around the word

## Cosine for measuring similarity

## TF-IDF: Weighin terms in the vector

> **Problem**
> Each word in co-occurrence term-document matrix is represented by frequency. However a lot of words are just used a lot like "the", "it", etc. in every documents and hence are not a good discriminator.

> **Solution
> $w_{t,d} = tf_{t,d} * idf_t$

term frequency in the document: $tf_{t,d} = log_{10}(count(t,d)+1)$ 
inverse document frequence: $idf_t = log_{10}(\frac{N}{df_t})$
- in how many documents does the word occur
- omits the impact of words which occur in every document

## Pointwise Mutual Information (PMI)

>**Idea**
>How often do two eventy x and y occur, compared with what we would expect if they were independent: $$\operatorname{PMI}(w, c)=\log _2 \frac{P(w, c)}{P(w) P(c)}$$

> $P(w,c)$ tells how often we saw words together
> $P(w)P(c)$ tells how often we would expect the two words co-occuring independently

>It's more common to use PPMI$$\operatorname{PPMI}(w, c)=\max \left(\log _2 \frac{P(w, c)}{P(w) P(c)}, 0\right)$$
