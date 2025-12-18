## How are tokens predicted, truly??

"man behind the curtain: - wizard of oz

Create a solution that makes meeting minute notes from audio recording.

1. Use Frontier Model to convert audio to text.
2. Use and open source model to generate minutes.
3. Stream them back and show in Markdown


The way models generate output =(do inference) is a multi step process.

The input is a sequence of token Ids. And their output is a "set of probabilities" 128,000 possible next tokens to this input sequence
Now take that "most likely output token" and give that whole sequence as a new input back in.
This back and forth repeat (typewriter animation) [distribution of probability]

Reasoning models will think through token after token. 

doesnt matter how i've implemented it - thats not the point here.

it doesnt seem so far fetched!.

You are getting to see some of the machinery of whats going on .

A little bit of the magic of next token prediction is fading.

Not untill you see it --- and really agonise over it  --- that you get to feel this for real --- to get a sense that these are the ingredients.

"When you ask for recipe it loses the sparkle a bit"...

tangible and concrete understanding.

When we call openAI - we can pass in temperature=0  [it simply always picks the token of highest probablity]
Meaning always consistently provide same output

higher temperature - use variation / imagination. [it samples from the token and looks beyong the highest probability]


TOOLS:
Google Colab
Whisper
mulimodal
open and closed models


- upload the mp3 file into google drive folder.
- 

audioFile = open(filenName, "rb");  # open the file

# Step 1:
convert audio to text (use hugging face pipeline)
- simply say the 

pipe = pipeline(task="automatic-speech-text-translation", model called whisper, device=cuda)
result = pipe(audioFile);
print(result)

Lots of text is now printed out from that audio file.

## option 2

Using open AI frontier model
look for gpt-4o-mini-transcribe model

# Step 2:

Report and Analyze.

Do systemMessage = "you are a analyser"
UserMessage = "this is the transcribed dat"

We can use this "TextIteratorStreamor" to stream back results into Gradio

This is a commercial tool. (build and practice)



-TODO
i can write a model to generate synthetic data eg: customer data and address etc

so using LLMs we build usefual models liek this.








