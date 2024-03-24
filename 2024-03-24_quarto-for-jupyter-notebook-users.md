

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
python3 -m pip install polars duckdb lets-plot
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


