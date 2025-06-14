# AI-Text-Completion-Project

**Model Settings Used**

generator(
    prompt,
    max_new_tokens=100,
    temperature=0.9,
    top_p=0.95,
    do_sample=True,
    pad_token_id=50256,
    truncation=True
)

**Evaluation Summary**

Strengths: The model generates creative and readable responses. It performs especially well on casual, open-ended prompts (e.g., storytelling and explanations).

Weaknesses: It struggles with accuracy and structure in certain formats like poems (e.g., haikus), and sometimes lacks detail or context in educational prompts.

Parameter Impact: Lower temperature (e.g., 0.3) produced more conservative, factual answers. Higher values made the output more playful but less consistent.

**Improvements**

Add input templates for better user control.

Include a response validator or fact checker.

Build a simple UI using Streamlit or Gradio for ease of use.
