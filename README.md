# Resume-RAG
This project is for DDSC S25. We will be using simple RAGs to query information from a resume and return relavent information to the LLM, which will answer the user query. If time, we will tackle on the challenge of using modular RAGs.

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
