202212030800
Status: #idea
Tags: [[Computational Linguistics]], [[Vector Semantics and Embeddings]], [[Word Embeddings]], [[Word2vec]]

# skip-gram

>[!Definition]-
>Skip-gram is an algorithm which assigns probabilities if a window of words  can be the context for a given target word (1) or can not (2). It does so by encoding by finding an embedding for each target and context word. Then we have two embeddings for each word. We compare the two embeddings with cosine similarity (3) and use a logisitic/sigmoid function to obtain probabilites (4). w and c are the word embeddings of the target and context word respectively, but how to we get to our embeddings?
>(1) $$P(+|w,c)$$
>(2)$$P(-|w,c) = 1 - P(+|w,c)$$
>(3)$$Similarity(w,c) = c.w$$
>(4)$$P(+|w,c) = sigmoid(c.w) = \frac{1}{1 + exp(-c.w)}$$

>[!Training of embeddings]-
>1. Take corpus of text and vocabulary size N as input
>2. Assign random embedding for each word in N
>3. Sample positive examples $c_{\text {pos }}$ and negative examples $c_{\text {neg }}$ with size of $k*|c_{\text {pos }}|$
>4. Minimize the loss function $L_{CE}$ using stochastic gradient descent
>5. Compute the gradients in respect to the different embeddings
>6. Update our embeddings by step learning

>[!Loss function]-
>$\begin{aligned} L_{C E} & =-\log \left[P\left(+\mid w, c_{p o s}\right) \prod_{i=1}^k P\left(-\mid w, c_{\text {neg }_i}\right)\right] \\ & =-\left[\log P\left(+\mid w, c_{p o s}\right)+\sum_{i=1}^k \log P\left(-\mid w, c_{\text {neg }}\right)\right] \\ & =-\left[\log P\left(+\mid w, c_{\text {pos }}\right)+\sum_{i=1}^k \log \left(1-P\left(+\mid w, c_{n e g_i}\right)\right)\right] \\ & =-\left[\log \sigma\left(c_{\text {pos }} \cdot w\right)+\sum_{i=1}^k \log \sigma\left(-c_{\text {neg }} \cdot w\right)\right]\end{aligned}$

>[!Motivation]

# References
[[@jurafskySpeechLanguageProcessing]](p. 118)