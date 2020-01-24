This code is using the following:

- Sentence Embeddings using BERT - https://github.com/UKPLab/sentence-transformers
- JR/Paul Shapiro google nlp cloud scripts - https://opensource.com/article/19/7/python-google-natural-language-api
And a few more super smart stuff! like clustering, dimensionality reduction algorithems and keyword extraction.

notice:
you need to get a services.json file see JR/Paul Shapiro google nlp cloud scripts.
this code can use txt file or url as input.
BERTs memory requirement grows quadratic with the length of the sentence / document. Therefore, there is a limit of 512 tokens. As many words are broken down into sub-tokens, you often can only encode texts with up to 300-400 words with BERT.In general I think BERT is the wrong choice for documents. BERT is strong on a sentence level, but it will not produce sensible results on a document level.

TF-IDF / BM25 is extremely strong on document level and really hard to beat, much much better than most fancy neural approaches. Another good option is also LSA and LDA, which produce also quite nice clusters.

For LDA see Rory Truesdale work - https://www.searchenginejournal.com/mine-serps-seo-content-customer-insights/311137/



