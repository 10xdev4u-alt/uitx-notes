---
title: "Unit IV: Python Setup for Web Scraping"
id: unit4-topic3-python-setup
tags:
  - unit-4
  - web-scraping
  - python
  - pip
  - virtual-environment
aliases:
  - "Python for Scraping"
links:
  - "[[UITx/Unit_04_Topic_02_Programming_Languages_for_Scraping.md|Programming Languages for Scraping]]"
  - "[[UITx/Unit_04_Topic_04_Scraping_Data_with_Python.md|Scraping Data with Python]]"
---

# Unit IV, Topic 3: Python Setup for Web Scraping

> [!quote] A craftsperson is only as good as their tools and their workshop. Before we can begin the art of web scraping with Python, we must first prepare our environment. This involves installing Python, managing packages with `pip`, and creating isolated virtual environments to ensure our projects are clean and reproducible. Let us now set up our digital workshop.

## 1. Download and Installation of Python

Python is the language of choice for this course's web scraping section. If you don't have it installed, you can download it from the official website.

-   **Official Website:** [python.org](https://www.python.org/)
-   **Recommendation:** Download the latest stable version of Python 3 (e.g., Python 3.10, 3.11, etc.).
-   **Installation Process:**
    -   **Windows:** Run the installer. **Crucially, check the box that says "Add Python to PATH"** during the installation process. This allows you to run Python from your command prompt.
    -   **macOS:** Python 2 might be pre-installed, but you should install Python 3. You can use the installer from python.org or a package manager like Homebrew (`brew install python`).
    -   **Linux:** Most Linux distributions come with Python pre-installed. You can check your version with `python3 --version`. If needed, you can install it using your distribution's package manager (e.g., `sudo apt-get install python3` on Debian/Ubuntu).

### Verifying the Installation
Open a terminal or command prompt and type:
```bash
python3 --version
# or on some systems
python --version
```
You should see the Python version number printed, confirming the installation was successful.

## 2. `pip`: The Python Package Installer

**`pip`** is the standard package manager for Python. It allows you to install and manage additional libraries and dependencies that are not part of the standard Python library. `pip` is automatically installed with Python 3.4 and later.

### Verifying `pip` Installation
```bash
pip3 --version
# or
pip --version
```

### Installing Packages with `pip`
To install a Python library for web scraping, you use the `pip install` command.

-   **To install `requests`:**
    ```bash
    pip install requests
    ```
-   **To install `beautifulsoup4`:**
    ```bash
    pip install beautifulsoup4
    ```
-   **To install a specific parser for Beautiful Soup (recommended):**
    ```bash
    pip install lxml
    ```

## 3. Virtual Environments: The Key to Project Isolation

When you work on multiple Python projects, they might have different dependencies or require different versions of the same library. Installing all packages globally can lead to conflicts and make projects difficult to manage.

A **virtual environment** is a self-contained directory tree that contains a Python installation for a particular version of Python, plus a number of additional packages. It allows you to create an isolated environment for each project.

**This is a critical best practice for all Python development.**

### Creating and Using a Virtual Environment

Python 3 includes the `venv` module for creating virtual environments.

#### a) Create the Virtual Environment
1.  Navigate to your project directory in the terminal.
2.  Run the following command to create a virtual environment named `venv` (a common convention):
    ```bash
    python3 -m venv venv
    ```
    This will create a `venv` folder in your project directory.

#### b) Activate the Virtual Environment
You must "activate" the environment before you can use it. The activation command differs by operating system.

-   **Windows (Command Prompt):**
    ```bash
    venv\Scripts\activate
    ```
-   **macOS and Linux (bash/zsh):**
    ```bash
    source venv/bin/activate
    ```
    Once activated, your command prompt will usually change to show the name of the virtual environment (e.g., `(venv) C:\Users\YourUser\Project>`).

#### c) Install Packages in the Virtual Environment
With the environment activated, any `pip install` command will install packages *only* inside this isolated environment, not globally.

```bash
(venv) > pip install requests
(venv) > pip install beautifulsoup4
```

#### d) Deactivate the Virtual Environment
When you are finished working on the project, you can deactivate the environment.

```bash
(venv) > deactivate
```

## 4. Summary of a Typical Project Setup

1.  Create a new project folder.
2.  Open a terminal and navigate into the folder.
3.  Create a virtual environment: `python3 -m venv venv`
4.  Activate the virtual environment: `source venv/bin/activate` (or `venv\Scripts\activate` on Windows).
5.  Install the necessary packages: `pip install requests beautifulsoup4 lxml`.
6.  Start writing your Python scraping script.

## 5. Exam-Oriented Insights

Setting up a proper development environment is a practical skill.

> [!question] **Potential 2-Mark Questions:**
> 1.  **What is `pip` in the context of Python?**
>     *Answer:* `pip` is the standard package manager for Python, used to install and manage third-party libraries and dependencies.
> 2.  **Why is it considered a best practice to use a virtual environment for Python projects?**
>     *Answer:* To create an isolated environment for each project, preventing dependency conflicts between projects and keeping the global Python installation clean.
> 3.  **Which command is used to create a virtual environment named `venv` using Python 3's built-in module?**
>     *Answer:* `python3 -m venv venv`.
> 4.  **Name two essential Python libraries you would install for a basic web scraping project.**
>     *Answer:* `requests` (for making HTTP requests) and `beautifulsoup4` (for parsing HTML).

> [!tip] **For Higher Mark Questions:**
> Be prepared to describe the step-by-step process of setting up a new Python project for web scraping, including creating and activating a virtual environment and installing the necessary packages. Explain the problems that virtual environments solve. Discuss the roles of `requests` and `Beautiful Soup` in the scraping process.
