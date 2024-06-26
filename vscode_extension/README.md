<div align="center">
  <img src="https://github.com/lavague-ai/lavague/blob/main/vscode-assets/logo.png" width=140px: alt="LaVague Logo">
  <h1>Welcome to the LaVague VSCode Extension</h1>
  <p>🪄 Copilot for automating automation</p>
<h1></h1>
</div>

## 🌊 What is LaVague?

The LaVague VSCode extension is an **open-source** project designed to automate automation for devs! 

It enables you to leverage AI to turn your **natural language instructions** into Python code for automation leveraging **Selenium**.

Behind the scenes, we use **advanced AI techniques** (RAG, Few-shot learning, Chain of Thought) to enhance performance - check out [our documentation to find out more](https://docs.lavague.ai/en/latest/)!

## 🔧 Pre-requisites

To use our VSCode extension you will need:

- A version of VSCode >= 1.80

- The Jupyter notebooks VSCode extension
<img src="https://github.com/lavague-ai/lavague/blob/main/vscode-assets/jupter-extension.png?raw=true" alt="Jupyter extension" width=75%>

- You will also need to install the chrome webdriver & LaVague. You can do this by running our `setup.sh` LaVague installation script [available here](https://github.com/lavague-ai/LaVague)

See the LaVague installation instructions [for more details](https://docs.lavague.ai/en/latest/docs/get-started/setting-up-la-vague/)!

## 🏄‍♀️ Getting started

Let's now take a look at how to get started with the LaVague VSCode extension.

### Opening a new project

- Firstly, you'll need to download the `LaVague` extension from VSCode marketplace.

- Now, you can open your first LaVague project. You can do this by opening the VSCode Command Palette with Ctrl+Shift+P

- Type or search and find the 'LaVague: New project' command
<img src="https://github.com/lavague-ai/lavague/blob/main/vscode-assets/command-2.png?raw=true" alt="open new project" width=60%>

This will open a new LaVague Jupyter notebook file in VSCode with some pre-filled cells of code.
<img src="https://github.com/lavague-ai/lavague/blob/main/vscode-assets/window-1.png?raw=true" alt="initial browser"  width=75%>


### Adding your URL and instruction

You can add the URL you wish to generate automation code for in the first cell block.

<img src="https://github.com/lavague-ai/lavague/blob/main/vscode-assets/add-url.png?raw=true" alt="modify URL" width=75%>

If we now run this first block of code, we can see a new VSCode window opens displaying our target site.

We're now ready to add an instruction for the action we'd like to automate:

<img src="https://github.com/lavague-ai/lavague/blob/main/vscode-assets/instruction.png?raw=true" alt="add instruction" width=75%>

> Note you will need to have an OpenAI API key set in your notebook environment. If you don't have yours set in this environment, you can add the following code into a cell:

  ```
  import os
  os.environ['OPENAI_API_Key'] = ''
  ```

Your automation code will populate the next cell.

<img src="https://github.com/lavague-ai/lavague/blob/main/vscode-assets/instruction-and-code.png?raw=true" alt="generated code" width=75%>

By running this cell, we can now see the result of our automation code in our VSCode browser window:

<img src="https://github.com/lavague-ai/lavague/blob/main/vscode-assets/new-screen.png?raw=true" alt="updated browser" width=75%>

### Tips

Note, it is possible to include a sequence of actions in one instruction as follows:

`%lavague_exec "click on the files and versions tab, then scroll down to the bottom of the page"`

⚠️ Also note the extension always expects the cell following the cell with our `%lavague_exec` command to be empty so it can populate it with the generated automation code. 

If you don't have an empty cell, you will see the following error:

<img src="https://github.com/lavague-ai/lavague/blob/main/vscode-assets/empty-cell-warning.png?raw=true" alt="empty cell warning" width=60%>

Therefore, to run a new command now, we can move the previous generated code above our `%lavague_exec` command:

<img src="https://github.com/lavague-ai/lavague/blob/main/vscode-assets/move-old-code-up.png?raw=true" alt="layout" width=75%>

## 🙋 Get support

You can report a bug by opening a [new issue](https://github.com/lavague-ai/lavague/issues) on our GitHub repo. We regularly track bug reports and try to respond as soon as possible!

You can also chat with us on our [Discord server](https://discord.com/invite/SDxn9KpqX9)!