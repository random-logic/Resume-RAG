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

# Prerequisites
Here are the [apps used](/docs/prerequisite-apps.md) for this project.

# Setting up this project
* **IMPORTANT:** *Windows* users should only proceed in a WSL terminal.
1. Pull from GitHub
    * [SSH] `git clone git@github.com:random-logic/Resume-RAG.git`
    * [Default] `git clone https://github.com/random-logic/Resume-RAG`
2. `cd Resume-RAG`
3. `conda env create -f environment.yml --name ResumeRAG`
4. `code .`
5. Enter `Cmd+Shift+p` or `Ctrl+Shift+p`
6. Type `Python: select interpreter`
7. Select the Anaconda ResumeRAG env that we just created.
8. Every time you launch VSCode with this project, your Conda environment will automatically be opened.

# Coding guidelines
1. All code should be in Jupyter Notebook (*.ipynb* files) files in the *src* folder.
2. Modularize different code functions and parts in different cell.
3. Explain what each code cell does in markdown cells above it.
4. Each person should have their own Jupyter Notebook files to avoid merge conflicts.

# Adding dependencies
* For good practice, only add dependencies when absolutely neccessary.
* **IMPORTANT:** Run `conda install` instead of `pip install`.
* After adding new dependencies, run `conda env export --from-history | grep -v '^prefix:' > environment.yml`.

# Pulling updates
* Run `git pull`
* After pulling, run `conda env update --file environment.yml --prune`
