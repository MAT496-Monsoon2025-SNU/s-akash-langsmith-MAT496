# S Akash - LangSmith Course Documentation for MAT496
Note: All source files available in the relevant folders (Module 1, Module 2) titled the same as each video along with videos numbered in the description of the commit.
## Module 1
### Vid 1 (Basics of Tracing)
Used @traceable decorator to trace how functions get executed in LangSmith. Understood what the basic idea of tracing is. 
Also changed up the prompts a little, made LLM answer physics questions. 
### Vid 2 (Types of Runs)
Learnt about the different types of runs in which I used the functionality behind 4 runs, namely LLM, Chain, Retriever and Tool. Was also able to track these runs in LangSmith and learnt how these types of runs were actually represented in a trace. 
![LLM Run](https://i.gyazo.com/dc261feadb1ae3e3707f49e2daeb0332.png)
![LLM Run](https://i.gyazo.com/86230112373f2c5bbf3a13286c95a63e.png)
LLM runs^
![Retriever Run](https://i.gyazo.com/4a2725eaa0ff01c9ed25329b907c8cdc.png)
Retriever Run^
![Tool and Chain Runs](https://i.gyazo.com/31ee29036534e2dd652e6322d605b9d1.png)
Tool Run and Chain Run^
I changed up the prompts behind the LLM, Retriever and Tool Runs quite a bit.

### Vid 3 (Alternate Ways to Trace)
Found out about a few alternate ways to trace other than using @traceable. Namely,
- LangGraph: automatically traces everything without manual setup in a graph-like sequence
- trace(): Chooses which inputs/outputs to log.
- wrap_openai – Wrapper for OpenAI calls (tracks token usage)
- RunTree API – For full manual control, quite advanced. requires LANGCHAIN_TRACING_V2 = false.
![RunTree](https://i.gyazo.com/8df3b6105fb98d599ce41e624904de9f.png)

### Vid 4 (Conversational Threads)
A Thread is a way of representing multiple traces that are linked through a unique thread identifier. Also learnt how to name threads with Python's UUID feature.
I tried to figure out if Threads meant that new traces are able to use previous user input to answer questions. This turned out to be false. Threads are just a way to store relevant traces together in Langsmith.
![traces](https://i.gyazo.com/c73681441f7bfdde7c470edc13afa115.png)
![traces2](https://i.gyazo.com/59f8c8e47868d6eab2a77435634ae694.png)

## Module 2
### Vid 1 (Datasets)
Datasets are essentially example input/outputs. In this module I created a custom dataset and uploaded the examples from code to LangSmith. Also generated three AI examples with OpenAI that seemed to be in line with all my other examples. 
Instead of the readymade examples pertaining to LangSmith, I wrote custom examples based on simple Minecraft navigation ranging from how Minecraft is played to some of its in-depth mechanisms
![dataset](https://i.gyazo.com/c2af697e03ac760c550e9029e69356e9.png)

### Vid 2 (Evaluators)
Evaluators use a Run and an Example to calculate metrics like how similar two outputs are. We used a reference output to measure the accuracy of the output we fed to the LLM on a scale of 1 to 10.
I changed up the questionnaire (input, output and reference outputs) to match the Minecraft examples that I uploaded to my dataset. I also made an evaluator on LangSmith using LLM-as-Judge
![evaluators](https://i.gyazo.com/dbff230f28afaf277577ffac1b36d86b.png)

### Vid 3 (Experiments)
Experiments evaluate datasets with a lot more flexibility on which version of your LLM and even which version of your dataset is taken. 
You can even run experiments multiple times to determine if the LLM model has much deviation in its responses, and you can even run it concurrently to give you a faster output (although this uses up OpenAI rate limits much quicker and I am cautiously sparing of my 5$ worth of it!)
I used my dataset of Minecraft questions (I am sorry in advance, I just really like Minecraft. I figured you could frame a lot of questions based on it) to evaluate the responses given by ChatGPT 4o as well as 3.5 Turbo



