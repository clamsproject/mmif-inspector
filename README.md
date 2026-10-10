# MMIF Inspector

The inspector runs on a summary of a MMIF file created by the `mmif summarize` CLI command and it generates a mini website from the summary. See [docs/input-example.md](docs/input-example.md) for an example input file.

This code requries Python 3.10 or higher and the Jinja module:

```bash
$ pip install jinja2==3.1.*
```

An installable package is available on [PyPI](https://pypi.org/project/mmif-inspector/).

## Usage

The inspector is implemented as a Python package and comes with the `inspect` command utility. If you have installed the package you can use:

```bash
$ inspect -i SUMMARY_FILE -o DIRECTORY
```

If not installed, you can also use the  `run_inspector.py` script:

```bash
$ cd code
$ python run_inspector.py -i SUMMARY_FILE -o OUTPUT_DIR
```

Usage within Python code:

```python
>>> from inspector.inspect import create_www
>>> create_www('path_to_summary_file', 'output_directory')
```
