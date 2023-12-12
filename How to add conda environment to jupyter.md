# How to Add Conda Environment to Jupyter

There are two ways on how make your conda environment show up in jupyter notebook. First option is to manually add the conda environment to jupyter and second option is to automatically add the environments to jupyter.

### First Things First
To prevent confusion with the terms, instead of using "conda environment", I will use the following terms.

Base Environment: refers to the base conda environment
Virtual Environment: refers to the conda environment you created using the ```conda create --name NAME_OF_ENV``` command

Make sure you have ipykernel installed in the base environment and in your virtual environment. You may use either below.

```
conda install -c anaconda ipykernel
```

OR

```
pip install ipykernel
```

And make sure you have jupyter notebook installed in the base environment. You may check the official [jupyter website](https://jupyter.org/install) on the installation options of jupyter but usually I install it using pip but you may also try to use conda-forge.

```
pip install notebook
```

### Manually Add Conda Env to Jupyter Notebook
In the base environment, install the virtual environment. Make sure to change NAME_OF_ENV to the actual virtual environment name.

```
python -m ipykernel install --user --name=NAME_OF_ENV
```

Then open jupyter notebook to check if your virtual environment was successfully added to your jupyter notebook.
```
jupyter notebook
```

A new tab opens where you can see the folders where the jupyter command was invoked. Click the new button to see if your conda environment shows there. If not, double check if you have correctly followed the instructions above. 

Whenever I encounter a problem in manually adding the virtual environment to jupyter, I start fresh by uninstalling the virtual environment.
```
jupyter kernelspec uninstall NAME_OF_ENV
```

OR I resort to the easiest way of adding virtual environments which will be discussed in the next section.

### Automatically Add Conda Env to Jupyter Notebook
I am not sure if automatic is the right term of saying this but this is far most the easiest way I know.

Assuming you have already followed [this section](https://github.com/pfdhn/Personal-Documentation/blob/main/How%20to%20add%20conda%20environment%20to%20jupyter.md#first-things-first) and you have created your virtual environment, then all you have to do is the following.

Activate your virstual environment.
```
conda activate NAME_OF_ENV
```

And copy and paste the following commands:
```
conda install -c conda-forge notebook nb_conda_kernels jupyter_contrib_nbextensions
```

That's it!


