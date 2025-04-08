# Git / GitHub
* Install [Git](https://git-scm.com/downloads)
  * When installing, keep the default settings.
  * After installation, run `git config --global core.editor "nano"` in your terminal or command prompt.
* Create a [GitHub](https://github.com/) account
* (Optional) Connect GitHub with SSH
  1. [Setup SSH Key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
     * Reminder to select the correct platform (Mac or Windows or Linux).
     * Complete sections *Generating a new SSH key* and *Adding your SSH key to the ssh-agent*.
  2. [Add SSH Key to Your Account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account?tool=webui)
     * Reminder to select the correct platform (Mac or Windows or Linux).
     * Complete section *Adding a new SSH key to your account*.

# [Windows Users Only] WSL2
* [Installation instructions](https://learn.microsoft.com/en-us/windows/wsl/install)
* Complete the *Get started*, *Set up your Linux username and password*, and *Update and upgrade packages* sections.
* **IMPORTANT:** You will always use WSL2 for installing Python related extensions and running Python code instead of the default command prompt.

# Editor
* Install [VSCode](https://code.visualstudio.com/download)
* Install the following extensions under the [extensions tab](./src/VSCode-Extension.png):
  * [Windows Users Only] [WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)
  * **IMPORTANT:** *Windows* users should install the following extensions in a New WSL Window in VSCode.
  * [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
  * [Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare)

# Ollama
* Installation [instructions](https://ollama.com/download/)
* **IMPORTANT:** *Windows* users should install the *Linux* version in their WSL2 terminal.
