# Python Programming Language

# Getting Started with VS Code

This guide explains how to get started with Python development using **Visual Studio Code (VS Code)**. It covers creating a Python environment with Conda, activating the environment, running `.py` files, working with Jupyter Notebooks, installing `ipykernel`, and maintaining project dependencies.

## 1. Why Use VS Code?

VS Code is used as the IDE for this Python series because it provides several useful features:

- Run Python `.py` files.
- Run Jupyter Notebook `.ipynb` files.
- Create and manage Python environments.
- Use extensions for additional functionality.
- Get code assistance and other development features.

The tutorial uses **Python 3.12**.

---

## 2. Why Create a Separate Environment?

A separate environment is useful whenever you start a new Python project.

Python projects may require multiple packages and libraries. These packages are regularly updated and new features may be added over time. Different projects may also require different versions of the same package.

Using a separate environment for each project helps:

- Avoid package conflicts.
- Keep project dependencies isolated.
- Use different Python or package versions for different projects.
- Maintain projects more easily when packages are updated.

The Python version you choose can depend on the requirements of your project and the packages you need.

---

## 3. Create a Python Environment Using Conda

Open **Command Prompt** rather than PowerShell.

Use the following Conda command to create an environment:

```bash
conda create -p venv python==3.12
```

### Explanation

- `conda create` creates a new Conda environment.
- `-p venv` creates the environment at the specified path, here named `venv`.
- `python==3.12` specifies Python 3.12.

Conda may automatically install some basic packages required by the environment.

When Conda asks for confirmation, press:

```text
Y
```

The installation may take some time depending on your internet speed.

The created environment contains the basic files and directories required for a Python project, such as:

- `DLLs`
- `include`
- Other environment files and packages

---

## 4. Activate the Environment

After creating the environment, activate it using:

```bash
conda activate venv
```

Once activated, the terminal will use the Python environment you created.

You can now run Python files using this environment.

---

## 5. Create and Run a Python File

Create a Python file, for example:

```text
app.py
```

Add simple Python code:

```python
print(1 + 1)
```

Make sure that:

1. You are in the correct folder.
2. The `venv` environment is activated.
3. The Python file is located in the current folder.

Run the file using:

```bash
python app.py
```

The output will be:

```text
2
```

You can also create other Python programs, for example:

```python
print("Hello World")
```

Run them in the same way:

```bash
python app.py
```

---

## 6. Create a Project Folder

For the Python series, create a separate folder for the project or lesson.

For example:

```text
Python Basics
```

Inside this folder, you can create:

- Python `.py` files
- Jupyter Notebook `.ipynb` files
- `requirements.txt`

Keeping the files organized inside a project folder makes it easier to manage your code and dependencies.

---

## 7. Working with Jupyter Notebooks in VS Code

VS Code can also be used to create and run Jupyter Notebook files.

Create a notebook such as:

```text
test.ipynb
```

A Jupyter Notebook contains **cells** where you can write and execute Python code.

### Code Cells

A code cell is used to write Python code.

For example:

```python
1 + 1
```

You can create multiple code cells and execute them individually.

### Markdown Cells

Jupyter Notebooks also support **Markdown cells**.

Markdown cells can be used for:

- Titles
- Headings
- Notes
- Explanations
- Other documentation

For example:

```markdown
# Python Example
```

To execute the selected cell, press:

```text
Shift + Enter
```

This runs the current cell and moves to the next cell.

VS Code also provides additional options for running cells through the notebook interface.

---

## 8. Select the Python Environment in VS Code

When you open a Jupyter Notebook, VS Code may ask you to select a kernel.

Select the Python environment that you created earlier.

For example:

```text
venv - Python 3.12
```

VS Code may also display other Python environments available on your system.

Choose the environment that belongs to your current project.

---

## 9. Install `ipykernel`

When you try to run a Jupyter Notebook using the newly created environment, you may see an error indicating that the `ipykernel` package is required.

Install it using:

```bash
pip install ipykernel
```

### What is `ipykernel`?

`ipykernel` provides the Python kernel required for executing Python code inside a Jupyter Notebook.

After installing it, run the notebook cell again.

For example:

```python
1 + 1
```

The notebook should now be able to connect to the selected kernel and execute the code.

---

## 10. Create `requirements.txt`

It is useful to maintain a `requirements.txt` file for the packages required by your project.

Create:

```text
requirements.txt
```

For example:

```text
ipykernel
```

As the project grows, other packages can be added, such as:

```text
ipykernel
pandas
numpy
```

The purpose of this file is to keep track of the packages required by the project so they can be installed and maintained consistently.

---

## 11. `.py` Files vs Jupyter Notebooks

### Python `.py` File

A `.py` file contains Python code that can be executed directly from the terminal.

Example:

```bash
python app.py
```

### Jupyter `.ipynb` File

A `.ipynb` file is a Jupyter Notebook that allows you to organize Python code into cells.

To run a cell in VS Code:

```text
Shift + Enter
```

Jupyter Notebooks are useful when you want to combine code with explanations, headings, and other documentation.

---

## 12. Basic Project Workflow

A simple workflow based on the tutorial is:

```text
1. Open VS Code
        ↓
2. Create a project folder
        ↓
3. Create a Conda environment
        ↓
4. Activate the environment
        ↓
5. Create .py or .ipynb files
        ↓
6. Select the environment/kernel in VS Code
        ↓
7. Install required packages
        ↓
8. Add dependencies to requirements.txt
        ↓
9. Write and execute Python code
```

---

## 13. Important Commands

### Create Environment

```bash
conda create -p venv python==3.12
```

### Activate Environment

```bash
conda activate venv
```

### Install Jupyter Kernel

```bash
pip install ipykernel
```

### Run a Python File

```bash
python app.py
```

---

## 14. Key Takeaways

- **VS Code** can be used for both Python files and Jupyter Notebooks.
- **Python 3.12** is used in this tutorial.
- A separate environment helps prevent dependency conflicts between projects.
- **Conda** can be used to create and manage the environment.
- Activate the environment before working with the project's Python code.
- `.py` files can be executed using the `python` command.
- `.ipynb` files can be executed inside VS Code using Jupyter.
- Select the correct Python environment as the Jupyter kernel.
- Install `ipykernel` when the Jupyter environment requires it.
- Use `requirements.txt` to keep track of project dependencies.
- Use **Shift + Enter** to execute a Jupyter Notebook cell.

---

## 15. Project Structure Example

A basic project can look like this:

```text
Python Basics/
│
├── venv/
│
├── app.py
│
├── test.ipynb
│
└── requirements.txt
```

The exact project structure can be organized according to the needs of the project.

---

## Conclusion

VS Code provides a convenient environment for learning and developing Python applications. By creating a separate Python environment, activating it, selecting it as the Jupyter kernel, installing the required packages, and maintaining a `requirements.txt` file, you can keep your Python projects organized and isolated.

The next step is to begin learning the **basics of the Python programming language**.
