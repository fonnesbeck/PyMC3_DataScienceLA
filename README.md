# Tutorial: Probabilistic Programming using PyMC3 

**DataScience LA, 24 January, 2017**

[![Binder](http://mybinder.org/badge.svg)](http://mybinder.org/repo/fonnesbeck/PyMC3_DataScienceLA)

Probabilistic Programming allows for automatic Bayesian inference on user-defined probabilistic models. Recent advances in Markov chain Monte Carlo (MCMC) sampling allow inference on increasingly complex models. This class of MCMC, known as Hamiltonian Monte Carlo, requires gradient information which is often not readily available. [PyMC3](https://github.com/pymc-devs/pymc3 "GitHub - pymc-devs/pymc3: Probabilistic Programming in Python. Uses Theano as a backend, supports NUTS and ADVI.") is a new open source Probabilistic Programming framework written in Python that uses [Theano](http://deeplearning.net/software/theano/) to compute gradients via automatic differentiation as well as compile probabilistic programs on-the-fly to C for better performance. Contrary to other Probabilistic Programming languages, PyMC3 allows model specification directly in Python code. This workshop will introduce new users to the PyMC3 package, and demonstrate how to implement and fit models.

## Syllabus

### Introduction to PyMC3

* Variable types
* Probability models
* Simple case studies

### Markov Chain Monte Carlo

* Metropolis sampling
* Gradient-based sampling methods

### Approximation Methods

* MAP
* Variational inference
* ADVI

### Model Building with PyMC3

* Specifying priors and likelihoods
* Deterministic variables
* Factor potentials
* Custom variables
* Step methods
* Generalized linear models
* Missing Data

### Model Checking and Output Processing

* Storage backends
* Convergence diagnostics
* Goodness of fit
* Plotting and summarization


## Software Installation

Running PyMC3 requires a working Python interpreter, either version 2.7 (or more recent) or 3.4 (or more recent); we recommend that new users install version 3.5 (but see special note below if you are a Windows user). A complete Python installation for Mac OSX, Linux and Windows can most easily be obtained by downloading and installing the free [`Anaconda Python Distribution`](https://www.continuum.io/downloads) by ContinuumIO. 

`PyMC3` can be installed using `conda`, a package management tool that is bundled with Anaconda. PyMC3 also depends on several third-party Python packages which will be automatically installed when installing via `conda`. The four required dependencies are: `Theano`, `NumPy`, `SciPy`, `Matplotlib`, and `joblib`. To take full advantage of PyMC3, the optional dependencies `seaborn`, `pandas` and `Patsy` should also be installed. You can install PyMC3 and its dependencies by cloning this repository:

```
git clone https://github.com/fonnesbeck/PyMC3_DataScienceLA.git
```

Then move into the directory created by the clone, and install the required packages using `conda`:

```bash
cd PyMC3_DataScienceLA
conda env create -f environment.yml
```

This will create a *virtual environment* called `pymc_tutorial` that includes the dependencies for PyMC3 that is completely separate from any other Python installations you may have on your machine. To activate this environment to run the course materials, you can run the following command from the terminal:

```bash
source activate pymc_tutorial
```

**If you would rather not install the software yourself, you can use the MyBinder.org link at the top of the page to run the course materials on a remote server**
