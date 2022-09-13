
# Conda


<details>
  <summary>Example Install</summary>
  
  ## Setting Up Your Python Environment


If you are using conda (we recommend installing conda via [Miniforge](https://github.com/conda-forge/miniforge)), you can create a new environment as follows:

```bash
conda create -n "pyml" python=3.9 numpy=1.21.2 scipy=1.7.0 scikit-learn=1.0 matplotlib=3.4.3 pandas=1.3.2
```

After creating this environment, you can activate it via

```bash
conda activate "pyml"
```



**Pip and virtualenv**

If you prefer using `pip`, you can go ahead and install the required packages via

```bash
pip install numpy==1.21.2 scipy==1.7.0 scikit-learn==1.0 matplotlib==3.4.3 pandas==1.3.2
```

We additionally recommend creating a new virtual environment. 
You can create a new virtual environment with a specific Python version using [virtualenv](https://virtualenv.pypa.io/en/latest/) as follows:

```bash
pip install virtualenv
cd /path/to/where/you/want/your/environment
virtualenv pyml
source pyml/bin/activate 
```

After activating your environment, you can install the required packages via

```bash
pip install numpy==1.21.2 scipy==1.7.0 scikit-learn==1.0 matplotlib==3.4.3 pandas==1.3.2
```
## Checking Your Python Environment

To verify that your Python environment is set up for the following chapters, we recommend running the [`../python_environment_check.py`](../python_environment_check.py) script provided in the main folder of this repository.

You can run the `python_environment_check.py` script via

    python python_environment_check.py

Shown below is an example output:

```python

[OK] Your Python version is 3.9.6 | packaged by conda-forge | (default, Jul 11 2021, 03:35:11)
[Clang 11.1.0 ]
[OK] numpy 1.21.2
[OK] scipy 1.7.0
[OK] matplotlib 3.4.3
[OK] sklearn 1.0
[OK] pandas 1.3.2
```

## Jupyter Notebooks

Please see the https://jupyter.org/install website for the latest installation instructions.

We recommend installing Jupyter Lab via


```bash
conda install -c conda-forge jupyterlab
```

or 

```bash
pip install jupyterlab
```
</details>


<details open>
  <summary>Alternate Approach</summary>
  
  ## Setting Up Your Python Environment


If you are using conda (we recommend installing conda via [Miniforge](https://github.com/conda-forge/miniforge)), you can create a new environment as follows:

1.  Set up a [.yml file](https://github.com/SalMireles/package-demo/conda/environment.yml) with package specifications 

2.  Create a [Makefile](https://github.com/SalMireles/package-demo/conda/Makefile) to intall packages spin up your environment

3.  Install packages via Makefile then create your environment
```make
make install && make env
```

4.  Activate environment
```bash
conda activate machine-learning-book
```

**That's it!**

##### References
- [Creating an environment from an environment.yml file](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file) (source: Conda.io)



