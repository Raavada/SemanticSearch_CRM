# SemanticSearch_CRM

Semantic search means search with meaning. Instead of searching only for keywords in search query, it infers implicit and explicit entities in the query, 
find related entities, derives user intent and provides much more meaningful results. 
It represents knowledge in suitable manner to retrieve meaningful results.

Nowadays word embeeding techniques like BERT have become very popular. Here words are represented as numeric vectors and we can use cosine similarity function to
compute similarity using cosine similarity. These word embeddings works great for individual words but not for sentences.
If we just average word vectors within sentence and use it as sentence embedding, the performance of resulting embeddings is poeerer than glove embeddings. 
Also if you want to train BERT from scratch, it is computationally very expensive.
Typically you need to feed in pair of sentences to BERT for training. So if we have corpus of 10,000 sentences, it would mean we would need to feed in all possible 
pairs of sentences which amounts to n*(n-1)/2) = 50 million training examples and it would take 65 hrs to finish training.
Sentence BERT (or SBERT) which is modification of BERT is much more suitable for generating sentence embeddings. It uses Siamese and triplet network structure to 
derive useful sentence embeddings that can be compared easily using cosine similarity. This reduces the effort for finding the most similar pair from 65 hours with 
BERT / RoBERTa to about 5 seconds with SBERT, while maintaining the accuracy from BERT.
