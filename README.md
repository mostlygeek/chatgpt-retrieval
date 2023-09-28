# ChatGPT with Retrival

* Generated a fake student's information 
* Using ChatGPT, Langchain and Chroma vector DB
* Ask some questions about the data 
* check out the files in the `data/` directory
* installation instructions below

![demo video](demo.gif)


## Original Repo

[https://github.com/techleadhd/chatgpt-retrieval](techleadhd/chatgpt-retrieval)

Simple script to use ChatGPT on your own files.

Here's the [YouTube Video](https://youtu.be/9AXP7tCI9PI).

## Installation

Install [Langchain](https://github.com/hwchase17/langchain) and other required packages.
```
$ virtualenv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
```
Modify `constants.py.default` to use your own [OpenAI API key](https://platform.openai.com/account/api-keys), and rename it to `constants.py`.

Place your own data into `data/`.

## Example Questions to ask 

### Personal information questions 

* tell me everything you know about john
* what is john's favorite food? 
* How old was john on Jan 1, 2023? 
  * (this works better?) today is sept 28, 2023, how old is john today? think it through take it step by step
* If today is Sept 10, 2023, and john ate his favorite food once a week since he was 10 years old, how much of it would he have eaten?
  * should be 404 weeks, 1 day

### Psych-Ed Assessment questions 

* who performed his psych ed assessment
* what did the doctor recommend? 
* what was the doctor's diagnosis in the psych-ed assessment?
  * it seems to struggle with this
* was john diagnosed with autism?
  * no it was adhd

### IEP questions 

* Who were the teachers that wrote the 2020, 2021 and 2022 individual education plans?
* Who was his teacher in 2021 individual education plan?
* Who was his teacher in 2020 individual education plan?

Notes: the test code seems to do pretty badly on the IEP questions.  Maybe a result of the IEP docs not being loaded into the context?

Definitely lots of room for improvement, but good enough for an evening hack! 