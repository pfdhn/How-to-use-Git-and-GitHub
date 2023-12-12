# How to Add Conda Environment to Jupyter

There are two ways on how make your conda environment show up in jupyter notebook. First option is to manually add the conda environment to jupyter and second option is to automatically add the environments to jupyter.

### First Things First
Make sure you have ipykernel installed in the base environment and in your virtual environment. You may use either below.

```conda install -c anaconda ipykernel```
OR
```pip install ipykernel```

And make sure you have jupyter notebook installed in the base environment. You may check the official jupyter website on the installation options of jupyter but usually I install it using pip but you may also try to use conda-forge.

```pip install notebook```

