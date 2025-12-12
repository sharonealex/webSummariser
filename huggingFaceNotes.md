Hugging Face Platform (more details):started off as a chat bot. (Ubiquitous Open Source) - Github for data science models  [previously the place to go was Kaggle]

2 million MODELS open source!!! (what to do with these? lol)

Half a million DATA SETS.

SPACES: ready made apps with built in gradio. Hosted apps cos it comes with gradio deployed. (similar to heroku) Any app that can go into a docker container can be deployed in spaces.

Text generation/ text to video etc is the most common Gen AI task people seach for models. (Under the hood these could be transformers made of pyTorch or Tensorflow)

nameOfCompany/<modelName>  (in some way its similar to amazons managed stuff like bedrock)

Unlike ollama, where its pre-baked software package. Hugging face allows you to see the code and make changes. And I can run the model
myself on my machine through cursor etc. I can play around with tokens. I can make changes to the neural network layers. Allowing with fine tuning. (nothing like this is possible with ollama).

lets not loose sight of that

So any open source models can be run using hugging face. eg. meta's llama.

Hugging face has 3 libraries.
1. Hub ( a client to connect to it)
2. Datasets
3. Transformers
4. Peft (to ) - parameter efficient fine tuning.



What I can do so far:
- build summariser with open source frontier models.
- build a multi modal ai assistant
- i know to navigate hugging face platform and to have an idea of how to run code on google colab similar to jupitor notebook.

NEXT:

- understand high level and low level APIs of hugging face
- use pipelines for a wide variety of "inference tasks"
- use pipelines to genereate text.

tokens and neural networks - where the really juicy stuff happens.

- Higher level APIS to do standard stuff pretty quickly. (out of the box pretrained stuff for business common use case)

These HIGHER LEVEL APIS =called= PIPELINES.

1. my_pipeline =  pipeline("the_task_i_want_to_do");
2. result = my_pipeline(my_input);

1. my_pipeline =  pipeline("I want to summarise a website");
2. result = my_pipeline("here is the website link");

"look at it glance at it - if something alarms you then sure, dig into it. otherwise takes notes move on. When something breaks later come back to it and compare notes - if there was correlation. 

For the time being - let it wash over you, for the various warnings.


 eg: 
 1.sentiment analysis of reviewrs
 2. classifier: 
 3. named entity recognition - like give name and select that tagged person from a huge album of photos.
 4. Question Answer model (like kahoot/Knowledge base)
 5. Summarising (we did for brochure)
 6. translation STT


- Lower level APIs to give most power and control and fine tuning.




.




