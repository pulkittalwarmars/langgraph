### LangChain - LangGraph

- Agent is a system powered by a language model (runtime basically runs the agent in a loop, takes action, records action and does it until the agent decides its enough)
- LangChain has been making it easier to make agents with LangChain expression language
- With langgraph, making it easy to customize the agent runtime
    - Agent runtime use to be an agent executor class
        - basically ran ina loop and called tools in a specific way and handled errors in a specific way

    - how we want to make it flexible and add CYCLES > running it in a loop 
    - Langchain expression language and other dag like frameworks are not cyclical

- This is now a way to create these cyclical agent runtimes
    - 2 major agent runtimes
        - agent executor - recreated with langgraph
            - we can now modify this agent executor and edit the functionality
            - add human in the loop
            - force a tool to be called first etc
        - chat agent executor 
            - takes in a list of messages
            - and then represents the AGENT STATE just as a list of messages
            - so it returns a list of messages
            - this is because the newer models are chat based models
            - this means they intrinsically represent function calling as basically parameters as a part of a message and function responses
        - modify the 
