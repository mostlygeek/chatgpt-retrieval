# chatgpt-retrieval

(adapted to try with made up (gpt4 generated) info about a student)

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

Place your own data into `data/data.txt`.

## Example Questions to ask 

### Personal information questions 

* tell me everything you know about john
* what is john's favorite food? 
* How old is john on Jan 1, 2023? 
* If john ate his favorite food once a week since he was 10 years old, how much of it would he have eaten?
* If today is Sept 10, 2023, and john ate his favorite food once a week since he was 10 years old, how much of it would he have eaten?

### Psych-Ed Assessment questions 

* who performed his psych ed assessment
* what did the doctor recommend? 
* what did the doctor's diagnosis in the psych-ed assessment?
  * it seems to struggle with this

### IEP questions 

* Who were the teachers that wrote the 2020, 2021 and 2022 individual education plans?
* Who was his teacher in 2021 individual education plan?
* Who was his teacher in 2022 individual education plan?

Notes: the test code seems to do pretty badly on this.  Maybe a result of the IEP docs not being loaded into the context?