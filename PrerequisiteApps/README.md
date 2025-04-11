# [Windows Users Only] WSL2
* [Installation instructions](https://learn.microsoft.com/en-us/windows/wsl/install)
* Complete the *Get started*, *Set up your Linux username and password*, and *Update and upgrade packages* sections.
* **IMPORTANT:** You will always use WSL2 for installing Python dependencies and running Python code instead of the default command prompt.

# Git / GitHub
* **[Windows Users Only] IMPORTANT:** Setup Git in your WSL2 terminal.
* Install [Git](https://git-scm.com/downloads)
  * [Windows Users Only] WSL2 likely already ships with Git, but if needed, install the *Linux* version.
  * When installing, keep the default settings.
* `git config --global core.editor "nano"`
* Create a [GitHub](https://github.com/) account
* (Recommended) Connect GitHub with SSH
  1. [Setup SSH Key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
     * Reminder to select the correct platform (Mac or Windows or Linux).
     * Complete sections *Generating a new SSH key* and *Adding your SSH key to the ssh-agent*.
  2. [Add SSH Key to Your Account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?tool=webui)
     * Reminder to select the correct platform (Mac or Windows or Linux).
     * Complete section *Adding a new SSH key to your account*.

# Ollama
* Installation [instructions](https://ollama.com/download/)
* **[Windows Users Only] IMPORTANT:** Install the *Linux* version in your WSL2 terminal.

# Conda
* Installation [instructions](https://www.anaconda.com/download/success)
* **[Windows Users Only] IMPORTANT:** Install the *Linux* version in your WSL2 terminal.

# Editor
1. Install [VSCode](https://code.visualstudio.com/download)
2. Install the following extensions under the [extensions tab](./images/VSCode-Extension.png):
    * [Windows Users Only] [WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)
    * **IMPORTANT:** *Windows* users should only proceed in a [New WSL Window](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl#getting-started).
    * [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
    * [Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare)

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