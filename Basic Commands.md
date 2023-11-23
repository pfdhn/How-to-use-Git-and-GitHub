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


## Conda environments
When I tried learning conda environments, it was a huge mess. Even though I followed instructions everything seems to be out of place. For example, I created a conda environment to install tensorflow using ```pip install tensorflow```, I surely did activated my conda environment but the tensorflow was installed outside the environment. Maybe I created hundreds of conda environments already before finally realizing what I did wrong. Now, I will walk you through creating a conda environment.


STEP 1: Use the command below to create a conda environment called "test-env"
```
conda create --name test-env
```
Or you may also install other packages like python using the code below.
```
conda create --name test-env python=3.10
```

STEP 2: Verify if the "test-env" conda environment is successfully created by either activating it or listing all the available conda environments.

To activate the "test-env":
```
conda activate test-env
```
To list all conda environments:
```
conda env list
```

STEP 3: Install desired packages. 
One thing I learned was that I have to install the packages using the ```conda``` command first and then use conda-forge for packages that cannot be installed with conda. If the two commands won't install the packages properly, then my last resort is using ```pip``` or ```pip3``` command. You can also use ```pip``` or ```pip3``` all throughout the installation of packages.

Whether you have decided to use ```pip``` or ```pip3``` all throughout the installation process or use pip to install a certain package, make sure you have ```pip``` or ```pip3``` installed inside your conda environment first.

To check if pip is already installed use the command below.
```
conda list pip
```
OR
```
conda list pip3
```

If you have pip already installed, this means you used the ```conda create --name test-env python=3.10``` in Step 1. But if there's no pip installed yet, use either of the command below.
```
conda install pip
```
OR
```
conda install pip3
```













