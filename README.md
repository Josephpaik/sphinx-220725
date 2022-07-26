# Example: Basic Sphinx project for Read the Docs

```{image} https://readthedocs.org/projects/example-sphinx-basic/badge/?version=latest
:alt: Documentation Status
:target: https://example-sphinx-basic.readthedocs.io/en/latest/?badge=latest
```

% This README.rst should work on Github and is also included in the Sphinx documentation project in docs/ - therefore, README.rst uses absolute links for most things so it renders properly on GitHub

This example shows a basic Sphinx project with Read the Docs. You're encouraged to view it to get inspiration and copy & paste from the files in the source code. If you are using Read the Docs for the first time, have a look at the official [Read the Docs Tutorial](https://docs.readthedocs.io/en/stable/tutorial/index.html).

📚 [docs/](https://github.com/readthedocs-examples/example-sphinx-basic/blob/main/docs/)

: A basic Sphinx project lives in `docs/`. All the `*.rst` make up sections in the documentation.

⚙️ [.readthedocs.yaml](https://github.com/readthedocs-examples/example-sphinx-basic/blob/main/.readthedocs.yaml)

: Read the Docs Build configuration is stored in `.readthedocs.yaml`.

⚙️ [docs/conf.py](https://github.com/readthedocs-examples/example-sphinx-basic/blob/main/docs/conf.py)

: Both the configuration and the folder layout follow Sphinx default conventions. You can change the [Sphinx configuration values](https://www.sphinx-doc.org/en/master/usage/configuration.html) in this file

📍 [docs/requirements.txt](https://github.com/readthedocs-examples/example-sphinx-basic/blob/main/docs/requirements.txt) and [docs/requirements.in](https://github.com/readthedocs-examples/example-sphinx-basic/blob/main/docs/requirements.in)

: Python dependencies are [pinned](https://docs.readthedocs.io/en/latest/guides/reproducible-builds.html) (uses [pip-tools](https://pip-tools.readthedocs.io/en/latest/)). Make sure to add your Python dependencies to `requirements.txt` or if you choose \[pip-tools\](<https://pip-tools.readthedocs.io/en/latest/>), edit `docs/requirements.in` and remember to run `pip-compile docs/requirements.in`.

💡 [docs/api.rst](https://github.com/readthedocs-examples/example-sphinx-basic/blob/main/docs/api.rst)

: By adding our example Python module `lumache` in the reStructuredText directive `:autosummary:`, Sphinx will automatically scan this module and generate API docs.

💡 [docs/usage.rst](https://github.com/readthedocs-examples/example-sphinx-basic/blob/main/docs/usage.rst)

: Sphinx can automatically extract API documentation directly from Python modules, using for instance the `:autofunction:` directive.

💡 [lumache.py](https://github.com/readthedocs-examples/example-sphinx-basic/blob/main/lumache.py)

: API docs are generated for this example Python module - they use *docstrings* directly in the documentation, notice how this shows up in the rendered documentation.

🔢 Git tags versioning

: We use a basic versioning mechanism by adding a git tag for every release of the example project. All releases and their version numbers are visible on [example-sphinx-basic.readthedocs.io](https://example-sphinx-basic.readthedocs.io/en/latest/).

📜 [README.rst](https://github.com/readthedocs-examples/example-sphinx-basic/blob/main/README.rst)

: Contents of this `README.rst` are visible on Github and included on [the documentation index page](https://example-sphinx-basic.readthedocs.io/en/latest/) (Don't Repeat Yourself).

⁉️ Questions / comments

: If you have questions related to this example, feel free to can ask them as a Github issue [here](https://github.com/readthedocs-examples/example-sphinx-basic/issues).

## Example Project usage

This project has a standard Sphinx layout which is built by Read the Docs almost the same way that you would build it locally (on your own laptop!).

You can build and view this documentation project locally - we recommend that you activate [a local Python virtual environment first](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#creating-a-virtual-environment):

```console
# Install required Python dependencies (Sphinx etc.)
pip install -r docs/requirements.txt

# Enter the Sphinx project
cd docs/

# Run the raw sphinx-build command
sphinx-build -M html . _build/
```

You can also build the documentation locally with `make`:

```console
# Enter the Sphinx project
cd docs/

# Build with make
make html

# Open with your preferred browser, pointing it to the documentation index page
firefox _build/html/index.html
```

## Using the example in your own project

If you are new to Read the Docs, you may want to refer to the [Read the Docs User documentation](https://docs.readthedocs.io/).

If you are copying this code in order to get started with your documentation, you need to:

1. place your `docs/` folder alongside your Python project. If you are starting a new project, you can adapt the `pyproject.toml` example configuration.
2. use your existing project repository or create a new repository on Github, GitLab, Bitbucket or another host supported by Read the Docs
3. copy `.readthedocs.yaml` and the `docs/` folder into your project.
4. customize all the files, replacing example contents.
5. add your own Python project, replacing the `pyproject.toml` configuration and `lumache.py` module.
6. rebuild the documenation locally to see that it works.
7. *finally*, register your project on Read the Docs, see [Importing Your Documentation](https://docs.readthedocs.io/en/stable/intro/import-guide.html).

## Read the Docs tutorial

To get started with Read the Docs, you may also refer to the [Read the Docs tutorial](https://docs.readthedocs.io/en/stable/tutorial/).
It provides a full walk-through of building an example project similar to the one in this repository.
