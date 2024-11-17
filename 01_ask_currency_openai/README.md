## LangChain with Hugging Face and OpenAI Integration

This is an initial demonstration of how to set up and use LangChain to interact with language models hosted on Hugging Face and proprietary LLMs from OpenAI for natural language processing tasks.

The notebook includes setup, configuration, and examples of generating responses from these models.

### Prerequisites
1. Python 3.10+
2. Pip (Python package installer)
3. API tokens for:
   4. [Hugging Face Hub](https://huggingface.co/)
   5. [OpenAI](https://openai.com/)

### Installing Necessary Libraries: 

- follow the notebook instruction to install necessary packages

### Environment Setup
**API Tokens**: Add the following environment variables for authentication:

* Hugging Face Token: `HUGGINGFACEHUB_API_TOKEN`
* OpenAI API Key: `OPENAI_API_KEY`

### Output
The notebook generates responses to queries such as:

The example query used is 
```
"What is the currency of USA?"
```

**Result:**
```
"The currency of USA is the US Dollar (USD)."
```