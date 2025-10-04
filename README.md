# S Akash - LangSmith Course Documentation for MAT496
## Module 1
## Vid 1 (Basics of Tracing)
Used @traceable decorator to trace how functions get executed in LangSmith. Understood what the basic idea of tracing is. 
Also changed up the prompts a little, made LLM answer physics questions. 
## Vid 2 (Types of Runs)
Learnt about the different types of runs in which I used the functionality behind 4 runs, namely LLM, Chain, Retriever and Tool. Was also able to track these runs in LangSmith and learnt how these types of runs were actually represented in a trace. 
![LLM Run](https://i.gyazo.com/dc261feadb1ae3e3707f49e2daeb0332.png)
![LLM Run](https://i.gyazo.com/86230112373f2c5bbf3a13286c95a63e.png)
LLM runs^
![Retriever Run](https://i.gyazo.com/4a2725eaa0ff01c9ed25329b907c8cdc.png)
Retriever Run^
![Tool and Chain Runs](https://i.gyazo.com/31ee29036534e2dd652e6322d605b9d1.png)
Tool Run and Chain Run^
I changed up the prompts behind the LLM, Retriever and Tool Runs quite a bit.

## Vid 3 (Alternate Ways to Trace)
Found out about a few alternate ways to trace other than using @traceable. Namely,
- LangGraph: automatically traces everything without manual setup in a graph-like sequence
- trace(): Chooses which inputs/outputs to log.
- wrap_openai – Wrapper for OpenAI calls (tracks token usage)
- RunTree API – For full manual control, quite advanced. requires LANGCHAIN_TRACING_V2 = false.
![RunTree](https://i.gyazo.com/8df3b6105fb98d599ce41e624904de9f.png)





