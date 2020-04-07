# geomexp package :: Python :: 2.7

## To do list
- [ ] Update MANIFEST.in and setup.py to include auxiliary files.
- [ ] create object and classes instead of using bare functions.  
- [ ] Track all the used libraries and update the requirements.   
- [x] create and upload the whole python package to PyPi(test.pypi).   
- [x] Find a suitable freezing package for 1-click excecutable creation. Probably can use  [PyInstaller](https://www.pyinstaller.org/) as suggested [here](https://hackernoon.com/the-one-stop-guide-to-easy-cross-platform-python-freezing-part-1-c53e66556a0a)  
- [ ] Test the v0.1 executable for windows.

## Installing the package

1. The package is up on PyPi, so use pip to install

```bash
pip install geomexp  
```
The installation of dependencis shouldn not be necessery. Use only if you run into trouble with dependencies.

## Using the package
Once the package is installed then just import it using `import geomexp.ml` and you can then run the Muller-Lyer experiment as follows.

``` Python
geomexp.ml.ml_exp()  
```
The experiment will start by asking some basic details about the subject. The `esc` key will pause the experiment, and `q` will quit the expeiment. The gathered data will be stored in a folder called "data", at the location where you are running the terminal.


## Trouble shooting dependencies
The `environment.yml` file can be used by conda to create a environment which can run the package. The first line of the file will be the name of the environment. In this case it is `psychopyP2N`.

If you have conda installed(or  [download here](https://www.anaconda.com/distribution/)) then use the following command to create an environment on top of which the package can run.

```bash
conda env create -f environment.yml python=2.7
```
The command for activating the environment just created is

```bash
conda activate psychopyP2N
```
For further information [read here](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file).  

The method with `pip` and `requirements.txt` is not currently working.
```bash
conda install --name psychopyP2N --yes --file requirements.txt  
pip install -r requirements.txt  
conda env export > environment_droplet.yml  
conda env create -f environment.yml
```
*to be updated*
