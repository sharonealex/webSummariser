3 dimensions to LLM

1. Models
2. Tools
3. Techniques.



Models:

1 - Open source
Meta's llama (set themselves apart to make up for not having strongest models) ploy to keep the headlines.
llama 3.2 comes iwth 1B parameters. (slm)
Mistral (french company)
Qwen from alibaba (chinese company)
gemma from google
Phi from miscrosoft
deepseek from Deepseek AI

What makes Deepseek AI impressive is it could make a frontier model with fraction of training costs that whawt OpenAI (spend north of a 100 million) rather it did 4 million.
 

2- Close source (Frontier)
- GPT (5) from openAI, o-range models. 
- Anthropic (Claude) - ex open AI people. mortal enemy. (Sonnet version is the popular)
- Gemini (Google) very late to the party. Bard was a joke. But they caughtup in the market.
- Grok (x.ai) musk.

- perplexity, coherence ..etc second tier.

Three ways to use the models/

1. As a product with chat interfaces. UI. We are not using a model. We are using a product. It has features like memory, web search. (UX + Model)

2. LLMs that are running on the cloud. (OpenAI)

3. Call a managed service like Bedrock. Which will call the lLLM behind scene. (Vertex, Azure ML) this has benefit of having bigger machines for higher models.

Groq vs Grok. (TBL)

4. DIRECT Inference. using hugging face framework

5. Ollama is a product/platform to use "fixed/packaged" open source models. (Like docker hub)

3- architecture
4- how to select
5 Multi-modal (generate images & audio)


Tools/Libraries

1. Hugging face
2. Lang chain
3. Gradio
4. Weights & Biases
5. Modal


Techniques

1. APIs
2. Multi shot prompting
3. RAG
4. Fine tunining
5. Agentization.


Meta's llama is not open sourced. Its open weight. Only the weihts of the model is made available. The training material, methodologies etc to build the model are still unknown.

LLMs can come in 3 flavours.

1. Base model - complete sequence (sms and email) - predicting the char sequence. (Older versions of chatgpt used to be just that)
2. Chat / Instruct model. (prompt, reply) Chat varient. 
This is what got normal gpt to chat gpt.
3. Reasoning/Thinkingm model.

2 + 3 = hybrid model. (latest gpt 5), 

amount reasoning a model does is called "reasoning budget"

Foundation models = frontier models.

Generative Pre-trained Transformer

2017 - google seminar paper "all you need is attention"
2018 - OPen ai - GPT-1 (117 M)
2019 - GPT-2 (1.5B)
2020 - GPT 3 (100 B)
2022 - ChatGPT
2023 - GPT-4 (1 Trillion)
2024- GPT-40 (o series multi modal)
20125- GPT 5

1B -> 100B -> 1 T -> 10 Trillion. (more parameters, mean more intelligence) (not linear, it was logarithmic scale)

train more data - with more parameters

"transfer architecture" = take an input sequence of text and predict the next tokens.

"predictive text on steroids"

- Prompt engineers 
- Copiots (MS copilot / Github copilot)
- Context Engineering. (RAG) (give it more contextual input sequences)
- Agentic  AI - LLM controlling workflows. . reasoning & autonomous. 


"Hi my name is Ed"
[12194, 922, 1308, 382, 6117] - this is the token breakage for model gpt-4-1.mini
because Hi is a common used word - its high up in num value.

"I like banoffe"
[3357, 1299, 9171=ban, 28004=offee] word was fragmented!

every call to an llm is stateless - memory is illusion  (memory = input sequence)
we pass the entire conversation every time
LLM simply predicts most likely token in sequence.!!

This is expensive - we need to pay the bill - always worth reinforcing.  (need to pay for reasoning as well)

CONTEXT WINDOW: max number of tokens any model can consider when generating the next token.
= history + todays question + final output it returns.

For complete works of shakespear - 1 million tokens (only gemini can)

Know: transformers history, tokenising, context window, api costs


