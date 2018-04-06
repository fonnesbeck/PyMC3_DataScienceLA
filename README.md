# Introduction to Probabilistic programming (with PyMC3)

This repository was forked from the excellent tutorial by Chris Fonnesbeck: [PyMC3 DataScienceLA](https://github.com/fonnesbeck/PyMC3_DataScienceLA).

CEAi has modified some material and added new material - especially exercises with the aim of using this series of notebooks to prepare for our first Precision workshop - on Bayesian modelling.

## Why this material?
At CEAi we are always looking to push our ML skills to the next level and this is an experiment in how to implement this in the fast paced environment of a startup studio.  Instead of just doing a workshop on Bayesian modelling, we believe that we can get much more out of a workshop if we invest significant effort into preparation.  We are working through this material in the course of approximately 3 months to prepare for a workshop that will take approximately 3 days. We expect at least the following effects: everyone will enter the workshop with a given minimal level of knowledge, the three month period will allow lots of time to get into the topics and think through more difficult issues, we will have basic coding experience with PyMC3 as a vehicle for learning about Bayesian modelling and since these materials are being created just before use, we can adjust the difficulty level online.

We welcome all feedback to the notebooks and please send us pull requests with ideas for improvement.

We also note that we have found lots of inspiration elsewhere for arranging this material, including the PyMC3 documentation, examples, various talks and papers.  Relevant sources should be appended to each notebook.

## TODO list

- [x] Measure initial skill level and knowledge state of group
- [x] Work out speed and method of proceeding at group level
- [ ] Come up with a time plan targeting May for completion (deadline Apr 15th)

## Working through the material

### Initial measurement
We polled the ML group in CEAi as to the actual state of knowledge (self-reported) of various topics stated below and the following stacked graph displays the result.

![Initial group level of knowledge](initial_group_level.png)

### Interim measurement 
We aim for another measurement on 22.3.2018.


## Syllabus
We order the topics as follows: building models (using PyMC3 for inference), inference based on sampling, inference based on variational methods and finally model checking.  We aim for different levels of depth depending on the topic based on estimating what can be best handled in-house and what is best left for the workshop itself.


### Introduction to Bayesian modelling and PyMC3

- [x] Variable types
- [x] Probability models
- [x] Well known distributions refresher
- [x] Simple case studies
- [x] Comparing analytical solutions to numeric approximations
  - [x] Beta-Binomial model
  - [x] Normal-Normal model with known precision

### Model Building with PyMC3

- [x] Specifying priors and likelihoods
- [x] Deterministic variables
- [x] Factor potentials
- [x] Custom variables
- [x] Case study: fitting a 9x9 pixel faces
- [x] Case study: tagging two-token names

### Markov Chain Monte Carlo

- [x] Monte Carlo: importance sampling and rejection sampling
- [x] Markov Chain Monte Carlo
- [x] Metropolis and Metropolis-Hastings
  - [x] Examples: 2D Gaussian, linear regression with Laplace prior
- [x] Exercise: write your own sampler
- [ ] Gibbs sampling
  - [ ] Examples: 2D Gaussian, Dirichlet Process-based clustering (a taste of nonparametric methods)

### Approximation Methods

- [ ] Variational inference
- [ ] The ELBO
- [ ] Mean field approximation

### Model Checking and Output Processing

- [ ] Convergence diagnostics
- [ ] Goodness of fit
- [ ] Plotting and summarization

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
