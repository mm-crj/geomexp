# geomexp Python2 package

```bash
conda install --name psychopyP2N --yes --file requirements.txt  
pip install -r requirements.txt  
conda env export > environment_droplet.yml  
conda env create -f environment.yml
```
## Installing the package

1. Download the zip or `git clone` the repository.
2. Unzip if you downloaded the zip file.
3. Open a terminal and nagigate to the unzipped folder.
4. Use pip to install

```bash
pip install geomexp  
```
## Installing dependencies
The environment.yml file can be used by conda to create a environment which can run the package. *to be updated*

## Using the package
Once the package is installed then just import it using `import geomexp` and you can then run the Muller-Lyer experiment as follows.

``` Python
geomexp.ml.ml_exp()  
```
The experiment will start by asking some basic details about the subject. The `esc` key will pause the experiment, and `q` will quit the expeiment. The gathered data will be stored in a folder called "data", at the location where you are running the terminal.
