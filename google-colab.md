Google lets us run jupyter note book on the browser (in the cloud with a powerful runtime).
Bring up chrome browser and ssh into a google box.

Connects browser to a T4 box running in the GCP cloud (smaller free GPU - spot instance, so kick us off) - We can change run time type (CPU=normal computer, Tesla T4 GPU) (hosted run time)
every disconnect and delete - install pip etc, new machine each time.

get access to high GPU models, have tonnes and tonnes of parametrs (TB)

When working with Data Science models, you could be carrying out 2 very different activities: training and inference.

. Training
Training is when you provide a model with data for it to adapt to get better at a task in the future. It does this by updating its internal settings - the parameters or weights of the model. If you're Training a model that's already had some training, the activity is called "fine-tuning".

Inference is when you are working with a model that has already been trained. You are using that model to produce new outputs on new inputs, taking advantage of everything it learned while it was being trained. Inference is also sometimes referred to as "Execution" or "Running a model".

All of our use of APIs for GPT, Claude and Gemini in the last weeks are examples of inference. The "P" in GPT stands for "Pre-trained", meaning that it has already been trained with data (lots of it!)

I can also fine tune existing models.

The pipelines API in HuggingFace is only for use for inference - running a model that has already been trained. 

3 keywords of AI models = "Training" "Inference" "Parameters"

(The T4 is a professional, low-profile NVIDIA Tesla GPU launched in 2018)

PyTorch and TensorFlow are open-source deep learning frameworks (training of machine learning models, especially deep neural networks.)

Google will bump you out of a GPU box and on to a CPU box.

"Running the model" /"execution" that has been pre-trained before is called inference.

we can pin a data set version, just like we do for npm dependencies.

Using pipelines from hugging face:
= a common way to run a pipeline with sensible defaults.
step1: create a pipeline (a fun to call later)
my_pipeline = pipeline(task, model=xx, device=xx)

task  = sentiment_analysis

step2: call it as many times
my_pipeline("give me a nice poem from bach")

some examples for devices = CUDA (for NVIDIA GPU) or MPS on a mac.

Unlike transformers , "diffusion models are for image generation"

should you so desire,
a real sense 
a few mins for me and seconds for you
and as you can see sure enough - the GPU....bla

There is some approval process to use meta's llama3.1 model on hugging face.

TTS
Text To Speech model

------>   NVDIA A100 powerful model! (bbefy box)

you want it - who am i to hold that back from you?


encoding and decoding with tokenizers.
different models have different types of tokenizer meaning they break words into different types of chunks
eg: coconut= co + co + nut
or coco + nut

this is specific to the model itslef. And how they assign ids to each token chunk. (not a big deal in how performance is related to it)

<beginningOfText>
<endofText>

So hugging face gives us access to all the tokenizers (low level API). (converting words to numbers) 

the job of an AI engineer is to select, optimize, fine-tune and apply LLMs rather than to code a transformer in PyTorch

A tensor is a matrix of numbers. 

Causal LLMs (auto-regressive llm)

bits and bytes to reduce the precision to allow quantization.
We have to use "nf4" data type. ( a lot is floating point number type)

tensor is a fancy number for matrix of numbers. on the GPU.

There is an embedded layer that turns token into vectors. (token prediction generator). About 16 of these embedded layers.

