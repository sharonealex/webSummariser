- prompt engineering
- custom chat gpts
- copilots
- agentic AIs

linear prgoression model - between 20 amd 200 weights (Number of paramters)
GPT -1 in 2018 117 Million
GPT 2- 1.5 B
GPT 5 - 10 T

Tokens:

tokens and the atomic indvidual units that get passed into a model

early days- "predict the next char in the sequence"
nerual networks were trained off words. "whats the next word to follow"
later: happy medium between these 2 extremes
"chunks of words" = "tokens"

1 token = ~0.75 words


context window = total number of tokens that an LLM can process when generating the next token. (for long conversations) - multi shot prompting.

Illusion of  memory: - every time the entire tokens are passed in. 

API costs are per call. num of input token + num of output token.

Transformers are a type of neural network architecture that transforms or changes an input sequence into an output sequence.
ChatGPT's foundation is the Transformer architecture, but it only utilizes the decoder part of the original Transformer model.

zero shot prompting - no clue
one shot prompting - one example given
multi shot prompting - many samples given