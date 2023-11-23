# Conda Basic Commands

#### There's an existing [Conda Cheat Sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf) provided by Anaconda but I am listing here the common commands I typically use.


### Verify Conda installation
```
conda info
```

### Update Conda
```
conda update conda
```

### Install a Conda Package
If the command below wont work, try to check if there is a conda-forge version of the package [here](https://anaconda.org/conda-forge)
```
conda install PACKAGENAME
```

### Update a Conda Package
```
conda update PACKAGENAME
```

## Conda environments
When I tried learning conda environments, it was a huge mess. Even though I followed instructions everything seems to be out of place. For example, I created a conda environment to install tensorflow, I surely did activated my conda environment but the tensorflow was installed outside the environment. Maybe I created hundreds of conda environments before finally realizing what I did wrong.



```
conda update PACKAGENAME
```
