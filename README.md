# **Function Calling Calculator**

##**Step 1**

      !pip install -q -U langchain langchain_community langchain_google_genai

**code**

**🔹 what does this do?**

This command installs three essential libraries:

* langchain → A framework for building applications using
  LLMs (Large Language Models).
* langchain_community → Community-contributed tools and
  integrations.
* langchain_google_genai → Allows us to use Google's Gemini
  models in LangChain.

  **🔹 Real-World Example:**

Imagine you want to build a house. You first install the necessary tools like a hammer, saw, and measuring tape. Similarly, before working with AI models, we need to install the required libraries.


## **Step 2**


**code**

**🔹 What does this do?**

* userdata.get('GOOGLE_API_KEY') → Retrieves your Google API key from Colab's userdata.
* os.environ['GOOGLE_API_KEY'] = ... → Stores the API key as an environment variable so the LangChain model can use it.

**🔹 Why is this important?**

This API key acts as a password to access Google’s Gemini model. Without it, we wouldn’t be able to interact with the AI.

**🔹 Real-World Example:**

Think of an API key like a ticket to a concert. You can’t enter without showing your ticket, just like you can’t use Google’s AI without an API key.




## **Step 3**

**code**

**🔹 What does this do?**

* ChatGoogleGenerativeAI → Creates a chatbot using Google's Gemini model.
* model="gemini-2.0-flash-exp" → Specifies the model version.
* verbose=True → Enables logging to see more details.
* llm.invoke("Who is Shehroz?").content → Asks the model a
  question and gets a response.

  **🔹 Real-World Example:**

This is like setting up a voice assistant (like Siri or Google Assistant) and asking, “Who is Shehroz?”



## **Step 4**

**code**

**🔹 What does this do?**

Tool and tool → Allow us to create custom functions (tools) that the AI can call when needed.

**🔹 Real-World Example:**

Think of this as importing different kitchen tools like a knife, spoon, and blender before cooking.



## **Step 5**

**code**



**🔹 What does this do?**

* Defines a function that adds two numbers.
* Uses @tool decorator, which makes the function accessible  
  to the AI.
* Prints a message when the tool is called.

**🔹 Real-World Example:**

Imagine you are teaching a calculator how to add numbers. The AI will call this function when someone asks, “What is 2 + 3?”

🔹 Other Tools: The same pattern is followed for:

* subtract(a, b) → Subtracts two numbers.

* multiply(a, b) → Multiplies two numbers.

* divide(a, b) → Divides two numbers, with a check for division by zero.

**🔹 Additional Tools:**

There are also tools for introducing Shehroz, providing social accounts, and saying goodbye.



## **Step 6**

**code**


🔹 **What does this do?**

* Groups all the custom tools into a list.

* Later, we will pass this list to the AI agent so it knows what functions it can use.

**🔹 Real-World Example:**

Think of this like a toolbox where you store all your tools (hammer, screwdriver, wrench) in one place.



## **Step 7**

**code**

🔹 **What does this do?**

* Creates an AI agent using the tools and the LLM.
* Agent Type: STRUCTURED_CHAT_ZERO_SHOT_REACT_DESCRIPTION → A
  structured agent that follows a reasoning process before acting.
* max_iterations=50 → Limits the agent to 50 steps per query.


**🔹 Real-World Example:**

This is like hiring a virtual assistant that can answer questions, do calculations, and provide information about Shehroz.


## **Step 8**



🔹 **What does this do?**

* Greets the user and explains the chatbot’s purpose.
* Starts a loop that continuously takes user input.
* Checks for exit commands and stops if the user says "exit" or "goodbye."
* Uses agent.invoke({"input": user_query}) to process the query and return an answer.

**🔹 Real-World Example:**

This is like a customer support chatbot where you ask questions, and it responds based on what it knows.


## **Summary**

* You created a chatbot agent using LangChain and Google Gemini AI.
* It can perform calculations and answer questions about Shehroz.
* It has a structured chat system with multiple tools.

**🔹 Real-World Analogy:**

This is like building a smart assistant that can do math, introduce people, and answer queries just like Siri or Alexa but customized for Shehroz.