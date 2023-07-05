# LangChain for LLM Application Developement - DeepLearningAI


## Overview

Crash course on LangChain for LLM Application Developement by [DeepLearning.AI](https://learn.deeplearning.ai/langchain/lesson/1/introduction) and lectured by `Andrew Ng` and `Harrison Chase` [LangChain](https://python.langchain.com/docs/get_started/introduction.html) Founder.

## Course Plan

- [Lesson0: Introduction](#)
- [Lesson1: Models, Prompts and Parsers](#)
- [Lesson2: Memory](#)
- [Lesson3: Chains](#)
- [Lesson4: Question & Answer](#)
- [Lesson5: Evaluation](#)
- [Lesson6: Agents](#)
- [Conclusion](#)

> All notebook examples are available in the [lab](./lab/) folder.


## Setup & Dependencies

Setup & import your openai key  : 

- [OpenAI Key](https://platform.openai.com/account/api-keys)

```python
import os
import openai

from dotenv import load_dotenv, find_dotenv
_ = load_dotenv(find_dotenv()) # read local .env file
openai.api_key = os.environ['OPENAI_API_KEY']
```

- Open API call 

```python
def get_completion(prompt, model="gpt-3.5-turbo"):
    messages = [{"role": "user", "content": prompt}]
    response = openai.ChatCompletion.create(
        model=model,
        messages=messages,
        temperature=0, 
    )
    return response.choices[0].message["content"]
```
## References

Main Course : 
- https://learn.deeplearning.ai/langchain/lesson/1/introduction

LangChain resources : 
- https://learn.deeplearning.ai/langchain/lesson/1/introduction

Others short Free Courses available on DeepLearning.AI : 
- https://learn.deeplearning.ai/





