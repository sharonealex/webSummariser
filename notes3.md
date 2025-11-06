router - unified interface for all the llms

chat variant / reasoning variant.

training time scaling / inference time scaling.

response = openai.chat.completetios.create(mode="llama", message=[], reasoning_effort="minimal")
by dialing up the model type and reasoning effort we can get better results.


Moving to abstraction - LangChain. (its heeavy weight)

import openai from langChain.
 we can import all llms like this. one place. (Other option: LiteLLM)

 from liteLLM import completion
 response = completion(model=openai/gpt, messages=[prompt]);  =?=> here we can pass in model from managed services like bedrock/claude-sonnet. 
 reply = response.choices[0]
 display(Markdown(reply))


 Toolokng

 code -> calls LLM -> LLM returns response -> executes a tool on my computer.

 Build an AI assistant using tools for enhanced experience.
 We can force an llm to run code written/function in our code.!

 ticket_prices = {"london": "$799", "paris": "$899", "tokyo": "$1400", "berlin": "$499"}

def get_ticket_price(destination_city):
    print(f"Tool called for city {destination_city}")
    price = ticket_prices.get(destination_city.lower(), "Unknown ticket price")
    return f"The price of a ticket to {destination_city} is {price}"


 tooling calls to function hooks + tooling call to a sql function calling local database for fetching data and returning in llm response.

 openai.images.generate() //expensive.
 openai.audio.speech.create //
 Using gradio and voice chat and image generator, we can easily create an AI assistant. for (customer support, emp onboarding assistant, ..) Ideas

