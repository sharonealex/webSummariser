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


chatGPT - is a product with UI etc (with llm behind it)
cloudAPIs - managed LLMs like bedrock from amazon, vertex from google etc. (we call bedrock and bedrock calls the llms)
frameworks like langchain.
open source - hugging face transformers library || ollama (ollama is for fixed packaged open source models, very specific versions.)

Ollama is hosted on a server.
ollama pull <modelname>

1. direct API call

response = requests.post(OLLAMA_API, json=payload, headers=HEADERS)
print(response.json()['message']['content'])

OLLAMA_API = "http://localhost:11434/api/chat"
HEADERS = {"Content-Type": "application/json"}
MODEL = "llama3.2"

messages = [
    {"role": "user", "content": "Describe some of the business applications of Generative AI"}
]
payload = {
        "model": MODEL,
        "messages": messages,
        "stream": False
    }

response = requests.post(OLLAMA_API, json=payload, headers=HEADERS)
print(response.json()['message']['content'])    

2. openai python sdk package for ollama


from openai import OpenAI
ollama_via_openai = OpenAI(base_url='http://localhost:11434/v1', api_key='ollama') #initialise

response = ollama_via_openai.chat.completions.create(
    model=MODEL,
    messages=messages
)

print(response.choices[0].message.content)

- Extend the same api and use different base url. and use ollama or qwen.
