# TextSummarization

Text summarization is the process of condensing a piece of text to its essential information, providing a concise and coherent summary while retaining the key ideas and important details, enabling readers to quickly understand the content without going through the entire text.

In this project, we have experimented with three popular pre-trained transformer language models to summarize news data (Found on Kaggle: https://www.kaggle.com/datasets/sunnysai12345/news-summary). We have applied the extractive summarization technique which tokenizes and encodes the input text using the respective tokenizer for each model i.e., *BertTokenizer, XLNetTokenizer, GPT2Tokenizer* from *transformers* package from HuggingFace Project (https://huggingface.co/docs/transformers/index) and then the pre-trained model was used to obtain embeddings for the input text and later, we applied a scoring mechanism such as cosine similarity, sentence embeddings, etc. to rank the sentences based on importance and selected the top sentences to deliver a summary of the data. 

The following are the models considered: 

**BERT (Bidirectional Encoder Representations from Transformers):** BERT is primarily designed for bidirectional context understanding, capturing relationships between words in both directions. We have used extractive summarization on this data where the BERT embeddings were used to determine the importance of sentences, and sentences with the highest importance scores can be selected for the summary. We used the *BartTokenizer* function from the *transformers* package, a part of the hugging face project. 


**GPT-2 (Generative Pre-trained Transformer 2):** GPT-2 is designed for autoregressive generation of text. It excels at generating coherent and contextually relevant text.
GPT-2 can also be used for extractive summarization by assigning importance scores to sentences. We used the *GPT2Tokenizer* function from the *transformers* package, a part of the hugging face project.


**XLNet (Transformer-XL based language model):** XLNet builds on BERT's bidirectional context understanding but also considers autoregressive modeling. It can capture long-range dependencies in a document. XLNet can perform extractive summarization by assigning importance scores to sentences or phrases. We used the *XLNetTokenizer* function from the *transformers* package, a part of the hugging face project.
