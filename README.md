

Language Translation Using LLM

This project demonstrates the use of Hugging Face's Transformers library to perform language translation with large language models (LLMs). Specifically, it uses the Helsinki-NLP/opus-mt-en-hi model for translating text from English to Hindi.

Features
Translate text between different language pairs.
Utilizes pre-trained models from Hugging Face for efficient and accurate translations.
Simple setup and minimal code for translation tasks.
Easily extendable for other language pairs supported by Hugging Face.
Requirements
Python 3.7 or higher
Hugging Face Transformers
PyTorch
Hugging Face Hub
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/translation-llm.git
cd translation-llm
Install the required libraries:

bash
Copy code
pip install transformers torch huggingface-hub
Authenticate with Hugging Face (if needed):

bash
Copy code
huggingface-cli login
Use your Hugging Face token for authentication. Obtain it from your Hugging Face account settings.

Usage
Import and configure the translation pipeline:

python
Copy code
from transformers import pipeline
from huggingface_hub import login

# Log in to Hugging Face
login(token="your_hugging_face_token")

# Load the translation model
nlp = pipeline("translation", model="Helsinki-NLP/opus-mt-en-hi")
Translate your text:

python
Copy code
text_to_translate = "Hello, how are you?"
translation = nlp(text_to_translate)

print("Translated Text:", translation[0]["translation_text"])
Run the script and see the translated output.

Example Output
Input: "Hello, how are you?"
Output: "नमस्ते, आप कैसे हैं?"

Extending to Other Language Pairs
Replace the model in the pipeline with any other supported model. For example:

English to French: Helsinki-NLP/opus-mt-en-fr
English to German: Helsinki-NLP/opus-mt-en-de
Explore available models on Hugging Face Model Hub.
