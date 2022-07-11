# Machine learning-accelerated chemistry of protoplanetary disks
### Supplementary materials
##### Grigorii V. Smirnov-Pinchukov, Tamara Molyarova, Dmitry A. Semenov, Vitaly V. Akimkin, Sierk van Terwisga, Riccardo Francheschi, and Thomas Henning

> *Aims*. With large amounts of molecular emission data from (sub)millimeter observatories, it is paramount to have a
fast method to calculate the chemical composition of gas in protoplanetary disks.
> *Methods*. We use thermochemical modeling code to generate a diverse population of protoplanetary disk models. We train the K Near-
est Neighbors regressor to instantly predict the chemistry of other disk models.
> *Results*. We show that due to correlations between the physical parameters in the protoplanetary disk, it is enough to use just a few
most important parameters to describe disk chemistry precisely. We discuss the uncertainties and limitations of this method.
> *Conclusions*. The method we utilize can be used for Bayesian fitting of the line emission data. We present a pipeline to use other
existing chemical disk modeling tools with the same approach.

We provide this Jupyter notebook as a way to reproduce the results from our paper. We encourage colleagues to reproduce our results and use this notebook
as a template for their pipelines to predict disk (or other environment) chemistry based on various physico-chemical models.

<a href="mailto:smirngreg@gmail.com">E-mail us! smirngreg@gmail.com</a>
### Installing

We suggest using the latest release of Anaconda to run this notebook. Anaconda is a conda-based Python distribution with stable versions of libraries.
It can be installed without root privileges, and is available for Windows, Linux, and Mac OS. If you don't have conda yet, install
[Miniconda](https://docs.conda.io/en/latest/miniconda.html) (just conda package manager). After installation, execute `conda init <mysh>`, replacing
`<mysh>` with the shell interpreter (zsh, bash) you prefer. This will add conda initialization to your login procedure.

Once conda is installed, you should have `(base)` at the beginning of your prompt line (bash) or somewhere else (modern zsh themes). Then, create a
separate environment (for example, let's call it mlchem):

```
conda create -y -n mlchem anaconda
conda activate mlchem
```

Additionally, you can install an optional package chemical-names, which converts strings like `HCO+` and `H2O` to `HCO^+` and `H_2O` respectively.

```
pip install git+https://gitlab.com/SmirnGreg/chemical_names.git
```

Now, you are ready to start. Run the Jupyter notebook in your prefered way: from PyCharm Professional, Jupyter Lab, or simply `jupyter notebook diskchef_chemistry.ipynb`
