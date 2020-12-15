# Gender Bias

The research on bias in language models has attracted a lot of attention in recent years. Gender bias, or sexism, is defined as discrimination against a certain gender, principally women. Besides spoken language, gender bias is also expressed in many forms of written language, such as news articles. This allows it to be reflected in language models as well, influencing metrics and pulling specific words towards one gender. In the case of workspace, those words can be related to jobs, occupations and roles. 

In English, jobs such as businessman, surgeon, and lieutenant are considered to be more male, while housewives and nurses are more associated with women. So, some job titles exhibit the stereotype towards male and some towards female cases. With the emergence of job interviews based on AI and Natural language processing (NLP) technology, a strong stereotype, i.e. bias in language models can affect people's careers and lives. 

This notebook presents an investigation of gender bias in word embedding models for the Serbian language. Specifically, we focus on job titles and gender determining words, i.e. we test whether some job titles are more associated with one gender than the other.

# Data

The training corpus was created by parsing the [Serbian Wikipedia dump](https://dumps.wikimedia.org/srwiki/) from June 2020 and by scraping news articles from [Večernje Novosti’s 2013-2020 news archive](https://www.novosti.rs/dodatni_sadrzaj/arhiva.347.html). The corpus was lemmatized using the [ParCoTrain-Synt corpus](https://github.com/aleksandra-miletic/serbian-nlp-resources).

Job titles were collected from the [Job Codex](http://kodekssifara.minrzs.gov.rs/documents/Sifarnik_zanimanja.pdf) and lemmatized as well. 

# Word Embeddings Models

We have employed Word2Vec [[1]](#1), FastText [[2]](#2) and Doc2Vec [[3]](#3) models using [gensim](https://radimrehurek.com/gensim/) library. Since most of the job titles are phrases, we represented them with Word2Vec by summing the vectors and learning the model on bigrams and trigrams. 

Please refer to the notebook for the results.

# References
<a id="1">[1]</a> Mikolov T, Chen K, Corrado G, Dean J. (2013). Efficient Estimation of Word Representations in Vector Space. CoRR abs/1301.3781

<a id="2">[2]</a> Bojanowski, P., Grave, E., Joulin, A., & Mikolov, T. (2017). Enriching word vectors with subword information. Transactions of the Association for Computational Linguistics, 5, 135-146.

<a id="3">[3]</a> Le, Quoc, and Tomas Mikolov. "Distributed representations of sentences and documents." International conference on machine learning. 2014.

