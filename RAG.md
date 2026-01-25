# RAG

- is a technique to improve user prompts. (Dictionary look up and context retrieval)

eg: (Small Idea)
1. Multi shot prompting
2. Use of tools (like query DB)
3. Additional context to the LLM model.


Taking this to next level:

1. Build a database/knowledgebase
2. every time  user ask a question, look up the knowledge base and send the enhanced context to the prompt LLM.
3. help LLMs - ie, biasing the model. this will influence the token generation. Makes the user feel like LLMs knows about them.

# Task is to build AI RAG Knowledge Worker for a company.  (This is existing as commercial products) Much quicker to market compared to training the model with more and more data.

The blunt instrument implementation:

- run a few sql queries from our own knowledge base/DB which is based on the incoming text from user. And add this detail and shove that also into the prompt. May be this could help.  Nothing more complicated.
- read names of employees, look up the files in drive and enahance the prompt. (fake data /synthetic data generated) LLMS were fine tuned to produce very optimistic output for employee performance.

1. read all employee data from file into a key: value where pluck out name `context={tom: {details}, ...}`
2. From this lookup by name.
3. Time to call LLM.

var SYSTEM_PREFIX = "you represent insurance company. youll given all context. If you dont know the answer, say so"

Write a simply python fun to do this integration.
User input: "Who is Tom"
[who, is, tom] - iterate and look up each word.
- Then `context.search(eachWord);` and pull up full details.

pythonic air of superiority. with elegance.

Then simply call the openAPI chat completions API - rest is history.
Then bring it up with Gradio interface and search for middle name and you wont get it. (cos it wasnt fed as part of RAG context)



BIG IDea:

LLM Encodings & Vector Embedding.

AutoEncoding LLMs produce result/predict a future token based on "Full input"

AutoRegressive LLMs produce result based on "Past inputs also"
