# Tutorial: Probabilistic Programming using PyMC3 

Original repository: [PyMC3 DataScienceLA](https://github.com/fonnesbeck/PyMC3_DataScienceLA), modifications by CEAi.

The original material is taken from Chris Fonnesbeck's excellent repository for the DataScience LA tutorial.  Here this material is modified to prepare the ML team @ CEAi for the first Precision Workshop on Bayesian modelling.  We have extended the work with extra topics and exercises.

Material from the PyMC3 introductory page is also added from the [getting started page](https://github.com/pymc-devs/pymc3/blob/master/docs/source/notebooks/getting_started.ipynb).

## TODO list

- [x] Measure initial skill level and knowledge state of group
- [x] Work out speed and method of proceeding at group level
- [x] Add more exercises and/or demonstrations where necessary
- [ ] Come up with a time plan targeting May for completion (deadline Apr 15th)


## Working through the material

### Initial measurement
We polled the ML group in CEAi as to the actual state of knowledge (self-reported) of various topics stated below and the following stacked graph displays the result.

![Initial group level of knowledge](initial_group_level.png)

## Syllabus

The syllabus is modified with the following logic: first come segments which focus on basic usage patterns of PyMC3 and then on model building, using various more or less advanced tools such as custom factor potentials.  This first allows exploration of the expressive capability of Bayesian models and thus making clear the benefits thereof before diving into inference and finally model checking.  We devote a lot of attention to understanding inference methods with diving into sampling and introducing the basics of variational inference.


### Introduction to Bayesian modelling and PyMC3

[x] Variable types
[x] Probability models
[x] Well known distributions refresher
[x] Simple case studies
[x] Comparing analytical solutions to numeric approximations
  [x] Beta-Binomial model
  [x] Normal-Normal model with known precision

### Model Building with PyMC3

[x] Specifying priors and likelihoods
[x] Deterministic variables
[x] Factor potentials
[x] Custom variables
[x] Case study: fitting a 9x9 pixel faces
[x] Case study: tagging two-token names

### Markov Chain Monte Carlo

[x] Monte Carlo: importance sampling and rejection sampling
[ ] Markov Chain Monte Carlo
[ ] Metropolis and Metropolis-Hastings
  [ ] Examples: 2D Gaussian, linear regression with Laplace prior
[ ] Gibbs sampling
  [ ] Examples: 2D Gaussian, Dirichlet Process-based clustering (a taste of nonparametric methods)

### Approximation Methods

[ ] Variational inference
[ ] The ELBO
[ ] Mean field approximation

### Model Checking and Output Processing

[ ] Convergence diagnostics
[ ] Goodness of fit
[ ] Plotting and summarization

## Software Installation

Running PyMC3 requires a working Python interpreter, either version 2.7 (or more recent) or 3.4 (or more recent); we recommend that new users install version 3.5 (but see special note below if you are a Windows user). A complete Python installation for Mac OSX, Linux and Windows can most easily be obtained by downloading and installing the free [`Anaconda Python Distribution`](https://www.continuum.io/downloads) by ContinuumIO. 

`PyMC3` can be installed using `conda`, a package management tool that is bundled with Anaconda. PyMC3 also depends on several third-party Python packages which will be automatically installed when installing via `conda`. The four required dependencies are: `Theano`, `NumPy`, `SciPy`, `Matplotlib`, and `joblib`. To take full advantage of PyMC3, the optional dependencies `seaborn`, `pandas` and `Patsy` should also be installed. You can install PyMC3 and its dependencies by cloning this repository:

```
git clone https://github.com/oapio/PrecisionWorkshop1_Prep
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
