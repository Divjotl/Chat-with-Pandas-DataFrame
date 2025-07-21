# 🦜 LangChain + Gemini: Chat with Your DataFrame

This Streamlit app lets you upload a CSV/Excel file and interact with it using natural language, powered by **LangChain** and **Google's Gemini (Generative AI)**. It's a powerful, fast, and flexible tool to explore and understand your data without writing code.


## Features

-  Upload `.csv`, `.xls`, `.xlsx`, `.xlsm`, or `.xlsb` files  
-  Chat with your uploaded dataset using natural language  
-  Understand patterns, summaries, column stats, and more

## How It Works
Communicating with pandas DataFrames makes data analysis accessible to non-technical users. Using a chat-like interface, users can ask data-related questions, request insights, and navigate through data as if they were chatting with a friend.

This web app integrates LangChain’s `create_pandas_dataframe_agent` to set up a **Pandas agent** that interacts with both the uploaded DataFrame and **Google's Gemini 2.5 Flash LLM** via the `ChatGoogleGenerativeAI` class.

- The agent takes three main inputs: `df`, the Gemini LLM model, and the user’s natural language question.
- Under the hood, the LLM generates Python code to perform the analysis on the DataFrame.
- That code is executed, and the output is converted into a conversational reply by the LLM.
- The result is then displayed back to the user in an intuitive chat interface.

## File Support

- `.csv`
- `.xls`, `.xlsx`, `.xlsm`, `.xlsb`

## Sample Questions

- “What is this dataset about?”
- “How many columns this data has?”
- “Describe the columns”

## Run Streamlit:
 streamlit run app.py
