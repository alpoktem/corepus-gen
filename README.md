# corepus-gen
Build sentence collections that respect the most frequent vocabulary in a language

Corepus-gen is built for compiling source sentences for parallel corpus construction. You get to choose its size and the vocabulary set that you'd like it to cover. 

In order to run corepus-gen you need the following:

- A large source corpus with lots of sentences (like [Tatoeba](https://tatoeba.org))
- A vocabulary set with words sorted with respect to their frequency

And if you like you can also use a list of words to avoid.

## Run

Follow the ipython notebook `corpus-generator.ipynb` filling in parameters like CORPUS_SIZE, REFERENCE_VOCAB_SIZE, MAX_TOKENS, CORPUS_ID etc. to your like.

## Example output

An example corpus of 10k sentences created with corepus-gen is placed under `testcore` directory. Its vocabulary includes 96.18% of the the most frequent 5000 words in the English OPUS Corpus. 

## References

* Files under `src` are taken from other sources with only structural modification. 
	- `opus_en_50k.txt` is the most common 50k words in the [English OPUS corpus](http://opus.nlpl.eu/).
	- `tatoeba_sentences_CC_EN.csv` contains English sentences in the Tatoeba corpus with CC license. 
	- `tatoeba_sentences_CC0_EN.csv` contains English sentences in the Tatoeba corpus with CC0 license

* `etc/avoidlist.txt` contains a subset of the bad words compiled by Google. [Source](https://github.com/RobertJGabriel/Google-profanity-words)


