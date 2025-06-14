# AI-Text-Completion-Project

!pip install transformers

from transformers import pipeline
generator = pipeline("text-generation", model="gpt2")

def ask_gpt2(prompt):
    response = generator(
        prompt,
        max_new_tokens=100,
        pad_token_id=50256,
        truncation=True
    )
    return response[0]["generated_text"]


while True:
    prompt = input("Enter a prompt (or 'exit' to quit): ")
    if prompt.lower() == 'exit':
        break
    if not prompt.strip():
        print("Please enter something.")
        continue
    print("\nResponse:", ask_gpt2(prompt))
