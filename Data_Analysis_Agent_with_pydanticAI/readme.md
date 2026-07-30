```markdown
# Data Analysis Agent with PydanticAI

## Overview
This project demonstrates the creation of an AI-powered data analysis agent capable of interpreting and answering questions about a dataset using natural language. It combines large language models with data manipulation tools (specifically pandas) to enable intuitive data exploration without requiring specialized programming knowledge.

## Motivation
Traditional data analysis often requires specialized knowledge, limiting access to insights for non-technical users. By creating an AI agent that understands natural language queries, we democratize data analysis, allowing anyone to extract valuable information from complex datasets.

## Features
- **Natural Language Understanding**: Users can ask questions about the data in plain English.
- **Pandas DataFrame Interaction**: The agent executes pandas queries on a DataFrame (`df`) based on the natural language input.
- **Error Handling and Retries**: The agent is designed to retry queries, learning from errors and correcting its approach.
- **Accessibility**: Makes data insights more accessible to non-technical users.
- **Flexibility**: Handles various types of data queries, from simple statistics to complex aggregations.

## How it Works
1. **Data Generation**: A sample dataset of vehicle sales is generated using `pandas` and `numpy`.
2. **Agent Initialization**: An `Agent` from `pydantic-ai` is configured with an `OpenAIChatModel` (leveraging Hugging Face's router for model access).
3. **Tool Definition**: A `df_query` tool is defined, allowing the agent to execute arbitrary pandas code on the `df` DataFrame.
4. **System Prompt**: A detailed system prompt guides the agent to use the `df_query` tool exclusively and provides rules for error handling and retries.
5. **Interaction**: Users ask questions, and the agent translates these into pandas queries, executes them, and returns the results.



## Conclusion
This approach offers significant benefits:
- **Accessibility**: Empowers non-technical users to perform data analysis.
- **Flexibility**: Adapts to various query types.
- **Efficiency**: Facilitates rapid, ad-hoc data exploration.

By making data insights more accessible, this method can transform how organizations leverage their data for decision-making across various fields and industries.
```
