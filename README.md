# bodo-tokenizers
Pre tokenized models for Bodo. This project includes all the tokenized models to be used in the  Neural Machine Translation. The models include pre tokenized modelstrained using ByteLevelBPETokenizer,  BPETokenizer,  SentencePieceBPETokenizer,  BertWordPieceTokenizer
# Models file
There are two models in this repository
## Models build with Google Sentencepice

## Models build with Huggingface Tokenizer
In order to use
`pip install tokenizers`
```
from tokenizers import BPETokenizer

# Load a BPE Model
vocab = "./hf-models/brx-bpe-tokenizer-vocab.json"
merges = "./hf-models/brx-bpe-tokenizer-merges.txt"
tokenizer = BPETokenizer(vocab, merges)

# And then encode:
encoded = tokenizer.encode("साबद्राय बावबायसो। नों रेदि खुरनानैलʼ दोनखादों आं थांगासिनो दं ।")
print(encoded.ids)
[13173, 11108, 1309, 241, 9268, 7661, 272, 25759, 219, 6576, 323, 192]

print(encoded.tokens)
['▁साबद्राय', '▁बावबाय', 'सो।', '▁नों', '▁रेदि', '▁खुरनानै', 'लʼ', '▁दोनखादों', '▁आं', '▁थांगासिनो', '▁दं', '▁।']

```
