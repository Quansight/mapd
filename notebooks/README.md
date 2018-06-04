# Example Notebooks

[![CircleCI](https://circleci.com/gh/Quansight/mapd.svg?style=svg)](https://circleci.com/gh/Quansight/mapd)

There are some example notebooks in this directory that should be run with Jupyterlab, with the mapd plugin installed.


* `Ibis + Altair.ipynb`: Creating a MapD query with Ibis and then visualizaing with Altair, with both the mapd vega backend and the browser backend.
* `Vega Rendering.ipynb`: Rendering vega and vega lite directly in the notebook to the mapd vega backend.

## Running Notebooks

### Docker

```bash
docker-compose up jupyterlab
```

### Conda

```bash
conda env create -f environment.yml
conda activate mapd
jupyter labextension install jupyterlab-mapd@0.3.0
jupyter lab
```

### Pip

This requires nodejs < 10 installed.

```bash
python -m venv venv
. venv/bin/activate
pip install -r requirements.txt
jupyter labextension install jupyterlab-mapd@0.3.0
jupyter lab
```


## ...With Local Version of `Quansight/jupyter-mapd-renderer`

### Docker

```bash
git clone git@github.com:Quansight/jupyter-mapd-renderer.git
docker-compose up jupyterlab-dev
```

Now you can edit the python and javscript files in `jupyter-mapd-renderer` and
see them reflected after you reload the page/kernel.