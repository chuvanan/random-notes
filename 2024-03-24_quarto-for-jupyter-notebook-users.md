

For Jupyter notebook users interested in utilizing Quarto for authoring technical documents or analytics reports, follow these steps:

# Setting up a Virtual environment

* To create a new Python virtual environment:

```bash
python3 -m venv env
```

* To activate the environment:

```bash
source env/bin/activate
```

* Verify environment activation

```bash
# This command should return the path to your Python executable
# within the environment directory
which python3
```

* Install required packages:

```bash
python3 -m pip install polars duckdb lets-plot jupyterlab-quarto
```

# Getting Quarto installed

* Visit the [Quarto website](https://quarto.org/docs/get-started/) and download the latest version

* Install Quarto:

```bash
sudo gdebi quarto-1.4.549-linux-amd64.deb
quarto --version
```

* Verify Quarto integration with virtual environment:

```bash
# Navigate to your project directory first
quarto check 
```

# Notebook template

* A notebook-based Quarto document consists of three main components: YAML header, Markdown cells, code cells

* A sample YAML header:
  - `toc`: to include auto-generated table of contents
  - `toc-depth`: to specify the number of section levels to include in the TOC
  - `number-sections`: to number section headings
  - `embed-resources`: to create self-contained HTML document
  - `monofont`: to set font-family on code elements
  - `mainfont`: to set font-family the HTML elements
  - `code-fold`: `true` to collapse code into an HTML tag so user can display it on demand
  - `code-tools`: `true` to include a code tools menu (for hiding and showing code in all code blocks)
  - `execute`: `enabled` to execute the cells when rendering the notebook

A full list of [HTML options](https://quarto.org/docs/reference/formats/html.html)

```
---
title: "A sample Quarto document"
format:
  html:
    theme:
      light: cosmo
    code-fold: true
    code-tools: true
    monofont: "Fira Code"
    mainfont: "Literata"
    number-sections: true
    toc: true
    toc-depth: 2
    embed-resources: true
jupyter: python3
execute: 
  enabled: true
---
```

