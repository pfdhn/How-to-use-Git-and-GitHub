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

### Get all Conda Environments
```
conda env list
```

### Get all Packages Installed in a Conda Environment
If you invoke the command below in the base environment, all packages installed in the base environment will be listed. But if you activated a conda environment and invoked the command below, all packages listed in the terminal is from the activated conda environment.
```
conda list
```

### Activate a Conda Environment
Before you activate a conda environment, your terminal will show ```(base) username@device_name some/path %```. After invoking the code below, it will show ```({name of environment}) username@device_name some/path %```
```
conda activate {name of environment}
```

### Deactivate a Conda Environment
```
conda deaactivate
```












