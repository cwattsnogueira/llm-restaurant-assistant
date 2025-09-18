#  LLM-Powered Restaurant Assistant  
**Prompt Engineering · NLP · Evaluation Dashboard · Gradio UI**  
*By Carllos Watts-Nogueira*

<a href="https://colab.research.google.com/github/cwattsnogueira/llm-restaurant-assistant/blob/main/LLM_PoweredRestaurantAssistant.ipynb" target="_parent">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT--3.5-lightgrey?logo=openai)
![Gradio](https://img.shields.io/badge/Gradio-UI-green?logo=gradio)
![Status](https://img.shields.io/badge/Evaluation-80%25-yellow)
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

## 📊 Evaluation Results

Static evaluation was performed on 5 test cases using predefined prompts and expected categories.

| Message                                             | Prediction  | Expected     | Match |
|-----------------------------------------------------|-------------|--------------|-------|
| I'd like to book a table for four at 7pm tonight.   | Reservation | Reservation  | True  
| Can I get two burgers delivered to 5th Avenue?      | Delivery    | Delivery     | True  
| I'll pick up my order in 20 minutes.                | Takeout     | Takeout      | True  
| We’re dining in tonight, please prepare a table.    | Dine-In     | Dine-In      | True  
| Do you have vegan options?                          | Dine-In     | Other        | False  

**Accuracy:** 80%  
**Model Behavior:** Deterministic (`temperature = 0.3`)  
**Observation:** The assistant misclassified a general inquiry as “Dine-In” instead of “Other”

---

##  Sample Staff Training Q&A

These examples simulate how the assistant supports restaurant staff with clear, actionable guidance.

| **Training Question**                          | **Answer**                                                                                                                                                      |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| How do I handle a customer complaint?          | 1. Listen to the customer's complaint attentively. <br> 2. Apologize for the inconvenience and assure them that you will address the issue. <br> 3. Offer a solution or compensation to resolve the complaint. <br> 4. Follow up with the customer to ensure they are satisfied with the resolution. |
| What’s the protocol for food safety in the kitchen? | Proper handwashing, using separate cutting boards for raw meats and produce, cooking food to the correct temperature, storing food properly, and sanitizing surfaces regularly. |
| How do I process a refund?                     | Access the POS system, locate the original transaction, select the refund option, enter the refund amount, and issue a receipt to the customer.                 |

---

##  How to Run

1. Open the Colab notebook using the badge above  
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

