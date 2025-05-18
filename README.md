# LLaMA-Based Support Ticket Automation

This project showcases the automation of customer support ticket classification and intelligent response generation using the LLaMA 2 13B Chat Model.





## Project Overview

- **Objective**:\
  Automate the classification, tagging, priority assignment, ETA suggestion, and first-response generation for support tickets using a fine-tuned LLaMA 2 model.

- **Tech Stack**:

  - Python
  - Jupyter Notebook
  - Hugging Face Hub
  - llama-cpp-python
  - Pandas, JSON
  - LLaMA 2 (13B chat model, quantized 6-bit GGUF format)

- **Approach**:

  - Load and preprocess support ticket dataset.
  - Construct detailed system prompts including classification criteria, tagging rules, sentiment-based response generation.
  - Use prompt engineering with few-shot examples to guide the LLaMA model behavior.
  - Parse and clean LLM outputs into structured JSON.
  - Aggregate structured outputs into a final dataset with new fields: Category, Tags, Priority, Suggested ETA, and Generated Response.



## How to Run Locally

1. Clone this repository:

   ```bash
   git clone https://github.com/shubhrashishir/llama-support-ticket-automation.git
   cd llama-support-ticket-automation
   ```

2. Set up the environment:

   ```bash
   pip install pandas transformers llama-cpp-python huggingface_hub
   ```

3. (Optional) Download model manually if needed:

   - TheBloke/Llama-2-13B-chat-GGUF (from Hugging Face)

4. Open the `llama_support_ticket_automation.ipynb` notebook and run all cells sequentially.

5. View the structured results for support ticket automation.



## Key Components

| Component              | Description                                                     |
| ---------------------- | --------------------------------------------------------------- |
| **Data Preprocessing** | Loaded and cleaned a CSV of 21 support tickets                  |
| **Prompt Engineering** | Combined system message and ticket text to guide LLaMA          |
| **LLM Inference**      | Used LLaMA 2 13B (6-bit quantized) model for text generation    |
| **Post-processing**    | Extracted JSON responses, handled malformed outputs             |
| **Final Dataset**      | Added 5 new fields (category, tags, priority, ETA, first reply) |



## Results and Observations

- **Ticket Categories**:

  - Technical Issues
  - Hardware Issues
  - Data Recovery

- **Priority Distribution**:\
  Most tickets were marked as **High Priority**, requiring **ASAP** resolution.

- **Actionable Insights**:

  - Majority of tickets indicated urgent, business-critical issues.
  - Intelligent routing and auto-responses can drastically reduce resolution time.



## Author

- **Name**: Shishir Shrivastava
- (Done as part UT Austin AI/ML post grad program
- **LinkedIn**: https\://www\.linkedin.com/in/shishir-s-9763971/



## Repository Structure

| File                                    | Description                                            |
| --------------------------------------- | ------------------------------------------------------ |
| `llama_support_ticket_automation.ipynb` | Complete Jupyter Notebook with code and outputs        |
| `README.md`                             | This file explaining project goals, setup, and results |



## Future Enhancements

- Migrate to latest LLaMA model
- Fine-tune LLaMA model on domain-specific ticket datasets.
- Deploy as an API endpoint for real-time ticket processing.
- Incorporate reinforcement learning from human feedback (RLHF) to improve output quality over time.



## License

This project is for educational purposes only.\
Use of LLaMA model must comply with Meta AI licensing terms.
