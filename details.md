# Quantization:

- All deep neural networks deal with numbers - lots of them , billions of them also called "parameters"
- All of them are 16 bit or 32 bit. (can handle a variety of large numbers, good precision)
- What if use fewer bits to load these numbers. (like a dimmer switch) 16 and 32 are very luxurious.
- If we use instead 8 bits, there are only 256 possible values. (suddenly dimmer switch is click click.. lesser, not continuously..)
- So we reduce the precision to 8 bits = Quantization. (Now it has discreet possible values)
- Squeeze "more" into "less" memory.
- Going to 16 bit to 4 bits - is saving 4 times memory.

- Are we saying we are reducing the parameters will degrade the quality? Not so much as we thought. So good. (This is called "DISTILLED")

- There is a data type called NF4. 


have a cuppa - things are about to get real!

# Model Internals

- Look at the lower level API of the transformer models that wrap the internal pyTorch code.
- connect to T4 box.
- do the pip installs
- Using bits&bytes library from huggingFace for quantization
- sign into hugging face


-llama 3.2 model is written by pyTorch ( a python library to develop neural networks )
- Neural network uses the transformer architecture invented by google scientists.
- I want to get an intuition to what a tranformer actually is.
- layers and layers like audio mixers.
- we can print out the code - to see the structure of the whole nerual network.
- 15 layers of neural network.
- how many dimensions come in and how many come out.
- over simplifying it. 
- This embedding layer is somtimes called "vector embedding"
- stack up on stack of audio mixers for an analogy.
- output ths probablity of the next token - it classifies the next token out of the 126000 tokens
- the 15 layers of neural network. are actually 15 modules called "decoder layer"
- attention is all you need.
- matrix calculations and multiplications - weighted combination of the inputs.
- a linear combination of linear combinations is itselft just a linear combination.
- 4 singers with mic phone - 4 voices blend -output from the mixer - send that through another mixer

can code with frontier llm models.
can build multi modal ai assistent with tools
use hugging face pipelines, tokenisers 




