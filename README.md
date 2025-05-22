# Resume-RAG
This project is for DDSC S25. We will be using simple RAGs to query information from a resume and return relavent information to the LLM, which will answer the user query. If time, we will tackle on the challenge of using modular RAGs.

# Why RAG
We want a model that works on different resumes without costly retraining and requires minimal data. Here's a full overview of how it compares to fine-tuning LLMs, one of the most popular alternatives.

| **Feature**               | **RAG (Retrieval-Augmented Generation)**                          | **Fine-tuned LLM**                                         |
|---------------------------|--------------------------------------------------------------------|-------------------------------------------------------------|
| **Definition**            | Combines external knowledge retrieval with a base LLM for responses | A base LLM that’s specifically fine-tuned on custom data     |
| **Data Handling**         | Retrieves relevant documents at inference time                    | Ingests custom data during training                          |
| **Cost**                  | Lower training cost; compute at inference                         | High training cost                         |
| **Speed to Deploy**       | Faster, no need to retrain the model                              | Slower; retraining can take hours or days                   |
| **Flexibility**           | Easy to update knowledge base                                     | Harder to update — requires retraining                      |
| **Hallucination Risk**    | Reduced, as answers are grounded in retrieved data                | Higher risk if model overfits or lacks accurate training data |
| **Real-Time Data Updates**| Supported — just update the knowledge base                        | Not supported unless re-finetuned                           |
| **Best For**              | Dynamic knowledge needs, QA systems, document-based answers       | Custom task-specific behavior, nuanced domain language      |
| **Inference Latency**     | Slightly higher (due to retrieval step)                           | Typically faster (no retrieval step)                        |
| **Example Use Cases**     | Customer support, legal/finance QA, Resume QA                     | Sentiment analysis, code generation, summarization          |

# Required Apps
Here are the [apps used](/docs/prerequisite-apps.md) for this project.

# Prerequisites
1. Follow this [tutorial](https://docs.smith.langchain.com/administration/how_to_guides/organization_management/create_account_api_key) to get your `LANGSMITH_API_KEY`.
2. Fill in the `LANGSMITH_API_KEY` in `.env.txt`.
3. Rename `.env.txt` to `.env`.
4. `ollama run llama3:8b`, can ctrl+c when finished with running this project to save system resources.

# Installation process
1. Pull from GitHub.
    * [SSH] `git clone git@github.com:random-logic/Resume-RAG.git`.
    * [Default] `git clone https://github.com/random-logic/Resume-RAG.git`.
2. `cd BasicRAGTutorial`.
3. `conda create -n ResumeRAG python=3.12`.
4. `conda activate ResumeRAG`.
5. `pip install poetry`.
6. `poetry install`.
7. Run `main.ipynb` in the `BasicRAGTutorial` conda env.

# Configure Environment on VSCode
1. Enter `Cmd+Shift+p` on Mac or `Ctrl+Shift+p` on PC.
2. Type `Python: select interpreter`.
3. Select the Anaconda `BasicRAGTutorial` env.

# Contribution guidelines
* All code should be in Jupyter Notebook (`.ipynb` files).
* All files should use intuitive and descriptive names.
* Code should be ran using the `ResumeData` Conda environment.
* Modularize different code functions and parts in different cell.
* Explain what each code cell does in markdown cells above it.
* Code unrelated parts in different files to reduce merge conflicts.
  * Example: Scraping each webpage should be in separate files, as these web pages are unrelated to each other.
* Contributors should code in different branches, and create pull requests to the main branch.
  * This is a good habit to learn as it applies to contributing with others in industry.
  * Please review the Git cheatsheet to use the appropriate commands and create a new branch.

# Adding a dependency
`poetry add [pip package name]`

# Removing a dependency
`poetry remove [pip package name]`

# Pulling updates
* Run `git pull`
* Run `poetry install`
