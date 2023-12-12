# Conda Environment
When I tried learning about conda environments, it was a huge mess. Even though I followed instructions everything seems to be out of place. For example, I created a conda environment and installed tensorflow using ```pip install tensorflow```, I surely did activated my conda environment but the tensorflow was installed outside the environment. Maybe I created hundreds of conda environments already only to find out that the pip command I should invoke must be from inside of the virtual environment.

Now, I will walk you through creating a conda environment.


### STEP 1: Use the command below to create a conda environment called "test-env"
```
conda create --name test-env
```
Or you may also install other packages like python using the code below.
```
conda create --name test-env python=3.10
```

### STEP 2: Verify if the "test-env" conda environment is successfully created by either activating it or listing all the available conda environments.

To activate the "test-env":
```
conda activate test-env
```
To list all conda environments:
```
conda env list
```

### STEP 3: Install desired packages. 
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

