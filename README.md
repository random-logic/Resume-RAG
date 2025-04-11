# Resume-RAG
This project is for DDSC S25. We will be using simple RAGs to query information from a resume and return relavent information to the LLM, which will answer the user query. If time, we will tackle on the challenge of using modular RAGs.

# Prerequisites
Here are the [apps used](/PrerequisiteApps/README.md) for this project.

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