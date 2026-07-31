# Customer Support Agent With LangGraph

This notebook develops an intelligent customer support agent using **LangChain & LangGraph**, a powerful library for building stateful, multi-step language model workflows.

## Purpose
The agent is designed to efficiently process and respond to customer queries by categorizing them, analyzing their sentiment, and providing tailored responses or escalating issues when necessary.

## Learning:
- **State Management**: Utilizes `TypedDict` to define and manage the state of each customer interaction, ensuring a clear and consistent flow of information throughout the workflow.
- **Query Categorization**: Automatically classifies incoming customer queries into three main categories: 'Technical', 'Billing', or 'General'. This allows for targeted handling of different types of issues.
- **Sentiment Analysis**: Analyzes the emotional tone of customer queries, classifying them as 'Positive', 'Neutral', or 'Negative'. This is crucial for prioritizing and handling sensitive interactions.
- **Response Generation**: Generates appropriate and contextually relevant responses based on the query's category and sentiment using a HuggingFace LLM.
- **Escalation Mechanism**: Implements an automatic escalation process for queries identified with a 'Negative' sentiment, ensuring that critical issues are promptly brought to the attention of human agents.
- **Workflow Graph**: Leverages LangGraph to construct a flexible and extensible finite state machine that orchestrates the flow of the customer support process, from initial categorization to final resolution or escalation.

## How it Works:
1. **Categorization**: The initial node identifies the type of query (Technical, Billing, General).
2. **Sentiment Analysis**: The next node assesses the sentiment of the query.
3. **Routing**: Based on the sentiment and category, the query is routed to the appropriate handling function:
    - If 'Negative' sentiment, it's immediately escalated.
    - Otherwise, it's directed to 'handle_technical', 'handle_billing', or 'handle_general' based on its category.
4. **Response/Escalation**: The designated function provides a response or triggers an escalation.

This agent provides a robust framework for automating customer support interactions, improving efficiency, and ensuring customer satisfaction.


