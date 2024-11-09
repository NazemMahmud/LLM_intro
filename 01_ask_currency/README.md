## LangChain with Hugging Face and OpenAI Integration

This project demonstrates how to set up and use LangChain to interact with language models hosted on Hugging Face and OpenAI. Using LangChain's convenient wrappers, you can easily access various LLM (Large Language Model) capabilities for natural language processing tasks.

- **Installing Necessary Libraries**: Installation of `LangChain`, specific packages for integrating with `Hugging Face` and `OpenAI` models.
- **Configuring API Access**: Sets up environment variables for accessing `Hugging Face` and `OpenAI` APIs with API tokens.
- **Using LangChain Wrappers**: It introduces LangChain's wrappers (HuggingFaceEndpoint and ChatOpenAI) for interacting with large language models.
- **Generating Model Responses**: It demonstrates how to create an instance of a language model and pass a query to generate a response. \
The example query used is 
```
"What is the currency of USA?"
```

### Requirements

- Python 3.6+
- Pip (Python package installer)

## Installation

1. **Clone the repository**:
    ```bash
    git clone [repository-url]
    cd [repository-folder]
    ```

2. **Install the required packages**:
    Run the following command to install the LangChain, Hugging Face, and OpenAI integration packages.
    ```bash
    pip install langchain==0.3.0
    pip install langchain-huggingface==0.1.0
    pip install langchain-openai==0.2.0
    ```

## Usage

This guide walks through configuring API tokens, setting up environment variables, and creating a LangChain LLM instance for both Hugging Face and OpenAI models.

### 1. Setting up API Tokens

Obtain your API tokens from [Hugging Face](https://huggingface.co/) and [OpenAI](https://platform.openai.com/).

### 2. Configuring Environment Variables

In the Python script, set the environment variables for your API keys:

```python
import os

# Hugging Face API Token
os.environ["HUGGINGFACEHUB_API_TOKEN"] = "your_huggingface_token"

# OpenAI API Key
os.environ["OPENAI_API_KEY"] = "your_openai_api_key"
```

### 3. Using Hugging Face Models
LangChain provides a wrapper around Hugging Face APIs. Here’s how to set up a Hugging Face model using the HuggingFaceEndpoint class:

```python
from langchain_huggingface import HuggingFaceEndpoint

# Initialize the Hugging Face model
llm = HuggingFaceEndpoint(repo_id="mistralai/Mistral-7B-Instruct-v0.1")

# Define a query
our_query = "What is the currency of USA?"

# Get the model's response
completion = llm.invoke(our_query)
print(completion)
```

### 4. Using OpenAI Models
For OpenAI models, use the ChatOpenAI class from the langchain-openai library:

```python
from langchain_openai import ChatOpenAI

# Initialize the OpenAI model
llm = ChatOpenAI(model="gpt-4")

# Define a query
our_query = "What is the currency of USA?"

# Get the model's response
completion = llm.invoke(our_query)
print(completion.content)
```

### Example Output
The expected output for the query "What is the currency of USA?" would be:

```csharp
The currency of USA is the US Dollar (USD).
```
### Notes
Make sure to replace your_huggingface_token and your_openai_api_key with actual API tokens.
For additional functionality and options, refer to the LangChain documentation.

## License
This project is open-source and available under the MIT License.




