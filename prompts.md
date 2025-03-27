# Prompt Engineering:
- Prompt engineering is all about how you desing the text inputs(prompts) for the LLMs to generate the most relevant and conxtual responses.   
- LLMs are use probability to predict the text so the quality of the prompt effects the responses is being generated.
- If the task is straight forward then LLMs might give precise result but for complex task the prompt engineering helps a lot.
- There are some key points which a structure prompt should have:
    - `Role`: The role we can assign to the model to change it's tone and behaviour while responding to a prompt. 
    - `Task`: The text in the prompt that the user want the model to provide the responses for.
    - `Contextual Information`: This is the information in our prompt that the model have reference and context which is used to generate the responses.
    - `Constraints`: It is used to bound the response of the model in specific limits.
    - `System Instructions`: These are the instructions which goes to the model before the user input in the prompt. The system remember these instructions while generating the response.
    - `Few-shot Examples`: These are few examples that we provide to the model in our prompt to show the model what getting right look like.

- |Worse    | Better    |
  |-----------|-----------|
  |Write code to calculate the Fibonacci sequence.|	Write a Python function to efficiently calculate the Fibonacci sequence. Comment the code liberally to explain what each piece does and why it's written that way.|

### The users are different and they can ask different type of task to the model. Some are mentioned below:

1. **Text Summarization:** Text summarization is one of the ability of a LLM which can summarize the articles and concepts into quick and easy to read summaries.

***Prompt***:
```plain text
Antibiotics are a type of medication used to treat bacterial infections. They work by either killing the bacteria or preventing them from reproducing, allowing the body’s immune system to fight off the infection. Antibiotics are usually taken orally in the form of pills, capsules, or liquid solutions, or sometimes administered intravenously. They are not effective against viral infections, and using them inappropriately can lead to antibiotic resistance.

Explain the above in one sentence:
```

***Output***:
```plain text
Antibiotics are medications used to treat bacterial infections by either killing the bacteria or stopping them from reproducing, but they are not effective against viruses and overuse can lead to antibiotic resistance.
```
2. **Information Extraction:** While LLMs are built to do natural language generation amd related task, it also capable to perform natural language processing tasks.

***Prompt***:
```plain text
Author-contribution statements and acknowledgements in research papers should state clearly and specifically whether, and to what extent, the authors used AI technologies such as ChatGPT in the preparation of their manuscript and analysis. They should also indicate which LLMs were used. This will alert editors and reviewers to scrutinize manuscripts more carefully for potential biases, inaccuracies and improper source crediting. Likewise, scientific journals should be transparent about their use of LLMs, for example when selecting submitted manuscripts.

Mention the large language model based product mentioned in the paragraph above:
```
***Output***:
```plain text
The large language model based product mentioned in the paragraph above is ChatGPT.
```
3. **Text Classification:** The LLMs are also be used for clafficition tasks.

***Prompt***:
```plain text
Classify the text into neutral, negative or positive. 

Text: I think the food was okay. 
Sentiment:
```
***Output***:
```plain text
Neutral
```
4. **Code Generation:** LLMs are quite effective in code generation. Copilot is a great example of this. There are a vast number of code-generation tasks you can perform with clever prompts.

***Prompt***:
```plain text
"""
Table departments, columns = [DepartmentId, DepartmentName]
Table students, columns = [DepartmentId, StudentId, StudentName]
Create a MySQL query for all students in the Computer Science Department
"""
```
***Output***:
```plain text
SELECT StudentId, StudentName 
FROM students 
WHERE DepartmentId IN (SELECT DepartmentId FROM departments WHERE DepartmentName = 'Computer Science');
```

- Here's a general prompt format for a precise responses:
```plain text
[ROLE]: Assume you are [expert/profession] in [field/industry].  

[TASK]: Your goal is to [clearly define task].  

[CONTEXT]: The project is about [describe the problem, company type, and intended outcome].  

[CONSTRAINTS]: Ensure that the response follows [specific rules, security policies, compliance standards].  

[FORMAT]: Return the response in [bullet points, numbered steps, table, JSON, YAML, code block].  

[EXAMPLES]: Here are some examples of expected output: [provide a sample output or similar examples].  

[FOLLOW-UP]: If clarification is needed, ask before assuming.  
```
- Example Prompt : 
```plain text
[ROLE]:
Assume you are a senior Python developer with expertise in software development, scripting, automation, and best coding practices.

[TASK]:
Your goal is to help developers write efficient, clean, and Pythonic code while following best practices. Provide optimized solutions, debugging help, and explanations when needed.

[CONTEXT]:
The project is about "PyAssist", an AI-powered assistant integrated into a developer’s IDE to help with Python coding, debugging, and optimization. The assistant will:
- Provide efficient Python solutions to coding problems.
- Suggest best practices and performance optimizations.
- Help debug errors by explaining issues clearly.

[CONSTRAINTS]:
- Follow PEP 8 coding style and Python best practices.
- Avoid using outdated or deprecated libraries.
- Ensure security by not suggesting hardcoded credentials or unsafe functions.
- Responses should be clear, concise, and include code examples.

[FORMAT]:
Return the response in:
Code snippets with comments
Step-by-step explanations where needed
Bullet points for best practices
```
![Prompt Engineering Diagram](https://flyaps.com/blog/content/images/2024/10/Prompt_Engineering_examples-.png)
