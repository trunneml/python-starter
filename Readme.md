# Python VSCode Sample

## About

This project is an example setup how to use VSCode for python development using common tools and configurations.

## Features

* Error Linting
* Style Linting
* Type Checking
* Refactoring Support
* Security Linting
* Code Formating
* Test Runner

## Usage

1. Setup the venv using pipenv

    ```sh
    pipenv sync
    ```

2. Start VSCode

    ```sh
    code .
    ```

3. Select the correct python interpreter
    1. `CMD+Shift+P` or `Ctrl+Shift+P`
    2. `> Python: Select Interpreter`
    3. Choose the created venv (PipEnv)


## Details

### Used Tools

* Python3
  * Pipenv
  * isort
  * Flake8 + Bugbear
  * Black
* VSCode
  * Python
  * Pylance
  * Flake8
  * Black Formatter
  * isort
  * editorconfig

### Feature Tool Matrix

| Feature        | Tool    | CLI | VSCode | Note                                           |
|----------------|---------|:---:|:------:|------------------------------------------------|
| Error Linter   | Pylance | no  |  yes   |                                                |
| Error Linter   | Flake8  | yes |  yes   |                                                |
| Style Linter   | Pylance | no  |  yes   |                                                |
| Style Linter   | Flake8  | yes |  yes   |                                                |
| Type Checking  | Pyright | no  |  yes   | Part of Pylance                                |
| Refactoring    | Pylance | no  |  yes   |                                                |
| Code Formating | isort   | yes |  yes   | With black profile                             |
| Code Formating | Black   | yes |  yes   |                                                |
| Test Runner    | Python  |     |  yes   | VSCode Python plugin has a buildin test runner |

### Pylance a microsoft language server

Pylance is a powerful language server for Python developed by Microsoft. It serves as a versatile tool within Visual Studio Code, offering numerous features to enhance Python development. It is designed to be a comprehensive solution for Python developers, offering a wide range of features to streamline your workflow and improve code quality.

Here's a closer look at what Pylance brings to the table:

**Built on Pyright**
: Pylance leverages Pyright, an open-source type checker, as its foundation. This integration provides advanced type checking, allowing you to catch errors and improve code correctness.

**Replaces MyPy**
: MyPy, a static type checker, has long been a staple for Python developers. Pylance offers an alternative that enhances type checking capabilities, making it easier to work with type annotations and improve code maintainability.

**Replaces Jedi**: Jedi has been a popular choice for autocompletion, static analysis, and refactoring in Python. Pylance takes over these responsibilities, offering an enhanced experience that helps you write code more efficiently and accurately.

**Provides linting**
: While not a direct replacement for pylint, Pylance incorporates essential functionality from Pylint. This includes features such as diagnostics (error and warning detection), quick fixes (for tasks like managing imports and refactoring), code completions, semantic colorization, and type checking. With these capabilities, Pylance reduces the need for additional linters and code analysis tools.

### Flake8

Flake8 is a comprehensive tool that combines static error checking, style enforcement, and complexity analysis (using McCabe) to enhance code quality and maintainability.
It is composed of several individual tools, each serving a specific purpose in the code analysis process:

#### Pyflakes

Pyflakes is a component of Flake8 responsible for checking your Python code for static errors. It analyzes your code for issues like undefined variables, unused imports, and other common mistakes that can lead to runtime errors or unexpected behavior. Pyflakes helps catch these issues early in the development process, saving you debugging time.

#### pycodestyle

The pycodestyle aka pep8 component, also known as pycodestyle, focuses on enforcing coding style guidelines in your Python code. It checks for compliance with the Python Enhancement Proposal (PEP 8), which outlines recommended coding conventions. By adhering to PEP 8 standards, your code becomes more readable and maintainable, and it aligns with Python community best practices.

#### McCabe

McCabe is a package included in Flake8 that calculates cyclomatic complexity, a measure of code complexity based on control flow analysis. It helps identify areas of your code that might be challenging to understand or maintain due to their complexity. McCabe provides valuable insights into your code's structure and can guide you in refactoring complex code segments.

### Black Formatter

Black Formatter is a VSCode plugin that seamlessly integrates the Black code formatter into your Python development workflow. Black ensures consistent and opinionated code formatting in accordance with PEP 8, automating style-related decisions. When used in VSCode, Black Formatter helps maintain code uniformity and readability, simplifying your coding experience.

## Links

* [VSCode - Python Tutorial](https://code.visualstudio.com/docs/python/python-tutorial)
* [VSCode - Python Environments](https://code.visualstudio.com/docs/python/environments)
* [VSCode - Linting Python in Visual Studio Code](https://code.visualstudio.com/docs/python/linting)
* [inventwithpython - Python linter comparision](https://inventwithpython.com/blog/2022/11/19/python-linter-comparison-2022-pylint-vs-pyflakes-vs-flake8-vs-autopep8-vs-bandit-vs-prospector-vs-pylama-vs-pyroma-vs-black-vs-mypy-vs-radon-vs-mccabe/)

## Future Stuff

* [https://python-packaging.readthedocs.io/en/latest/testing.html](https://python-packaging.readthedocs.io/en/latest/testing.html)
