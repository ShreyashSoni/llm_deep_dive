# LLM Deep-dive
A repo for the code of my LLM deep-dive

## Repository structure
1. #### Tokens and Embeddings

## Code files
1. #### Tokens and Embeddings
   - **01_text2numbers.ipynb:** Text can be split into words via spaces, although this is not done in real tokenization. Encoder and decoder functions are simple look-up tables. Tokenization (encoding text using integers) is conceptually straightforward.
   - **02_make_a_tokenizer.ipynb:** Encoders and decoders are created using dictionary comprehension and functions. The “context” of a token is its neighbors (before and possibly after); “context window” is the number of neighbors. "One-hot encoding” is a sparse tokenization, with one row per token and one column per vocab item.
   - **03_preparing_text_for_tokens.ipynb:** Real text from the web is easy to import but a pain to clean. Creating a tokenizing scheme is tricky and involves many choices with few clear optimal decisions Encoders and decoders are easy to create and use.
   - **04_tokenizing_time_machine.ipynb:** Randomly generated tokens are usually nonsensical. There is a mathematical relationship between word length and frequency, which has implications for LLM performance. Tokenizers need special characters to deal with unknown tokens.
   - **05_tbyte_pair_encoding.ipynb:** The BPE algorithm is based on replacing frequent token sequences with new tokens. The basic BPE algorithm is simple and easy to implement. Production-level tokenizers add several more steps to ensure accuracy, efficiency, and speed.