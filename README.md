#  LLM-Powered Restaurant Assistant  
**Prompt Engineering · NLP · Evaluation Dashboard · Gradio UI**  
*By Carllos Watts-Nogueira*

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/CarllosWatts/llm-restaurant-assistant/blob/main/restaurant_assistant.ipynb)
![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--3.5-lightgrey?logo=openai)
![Gradio](https://img.shields.io/badge/Gradio-UI-green?logo=gradio)
![Status](https://img.shields.io/badge/Project-Complete-brightgreen)
![License](https://img.shields.io/badge/License-MIT-blue)

---

##  Project Overview

This project demonstrates how to build and evaluate a modular AI assistant for restaurant operations using OpenAI's GPT-3.5. It supports two core use cases:

- **Order Classification**: Categorize customer messages into predefined types (Dine-In, Takeout, Delivery, Reservation, Other)  
- **Staff Training Q&A**: Answer operational questions clearly and concisely for restaurant staff

---

##  Features

-  Prompt engineering with reproducible templates  
-  OpenAI GPT-3.5 integration via secure Colab secrets  
-  Gradio interface with 4 interactive tabs  
-  Static evaluation logic with test cases  
-  Sample training Q&A dashboard  
-  Ready for deployment on Hugging Face Spaces or Streamlit

---

##  Technologies Used

| Component         | Stack / Tool                  |
|------------------|-------------------------------|
| LLM Backend       | OpenAI GPT-3.5 (via API)       |
| Interface         | Gradio                        |
| Evaluation        | Pandas                        |
| Hosting           | Google Colab / Hugging Face   |
| Secrets Handling  | `google.colab.userdata.get()` |

---

##  Evaluation Results

| Message | Expected | Predicted | Match |
|--------|----------|-----------|-------|
| "I'd like to book a table for four at 7pm tonight." | Reservation | Reservation | True  
| "Can I get two burgers delivered to 5th Avenue?" | Delivery | Delivery | True  
| "Do you have vegan options?" | Other | Other | True  

**Accuracy:** 100% on static test set  
**Model Behavior:** Deterministic (temperature = 0.3)

---

##  Sample Training Q&A

| Question | Answer |
|---------|--------|
| How do I handle a customer complaint? | Apologize, listen actively, offer a resolution, and escalate if needed.  
| What’s the protocol for food safety in the kitchen? | Wash hands, sanitize surfaces, store food at correct temperatures, and follow hygiene guidelines.  
| How do I process a refund? | Use the POS system, confirm the transaction, and follow manager approval protocols.  

---

##  How to Run

1. Open the Colab notebook  
2. Add your OpenAI API key via `Tools → Secrets` as `OPENAI_API_KEY`  
3. Run all cells  
4. Launch the Gradio interface and interact via tabs

---

##  Deployment Options

- Hugging Face Spaces (`gradio deploy`)  
- Streamlit Cloud  
- GitHub Pages (for static report)

---

##  Next Steps

- Add LangChain or Hugging Face model comparison  
- Integrate LangFuse-style logging  
- Expand training Q&A with quiz scoring  
- Deploy permanently and track usage metrics

