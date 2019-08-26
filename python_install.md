# Setup Python Environment

## Intro to Environment

Many systems come with native Python distributions, such as Mac and Linux. 
You can use them for sure but a few things to note: 

1) Many libraries may have versions that are not incompatible with each other.
Some programs may need one version of a package, while some other programs may 
want a different version. In this case, installing one library may crash the other. 
2) Sometimes you may want to try a set of packages (Numpy 1.15.4 and Scipy 1.1.2)
for one program, and use a different setting (Numpy 1.0.2 and Scipy 0.12.0) for another. 
Switching between versions can sometimes be very annoying. 

Therefore we would like to use an environment manager to manage Python libraries. 
I would recommend using [miniconda](https://docs.conda.io/en/latest/miniconda.html)
if you do not have one in hand. Below is a step-by-step instruction for installing 
miniconda, using it to create and configurate an environment (on Mac).

## Configure environment (Mac)
1) Open a terminal. Download the install script to a local folder, 
e.g., `~/Downloads`, and install miniconda with Python3.
```bash
# download
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
# install
bash Miniconda3-latest-MacOSX-x86_64.sh 
```
follow the prompt to complete the installation into a local directory, e.g., 
`$HOME/miniconda3`.
2) Enter conda, create an environment, and install required packages. 
```bash
source $HOME/miniconda3/bin/activate 
conda create --name cse404
conda activate cse404
conda install scipy=1.3.1
conda install numpy=1.16.4
conda install jupyter=1.0.0
```
3) Now you can go to one folder and start Jupyter notebook
```bash
jupyter notebook
```
You should be able to see a browser poping up. Otherwise try [this link](http://localhost:8888/). 
When you are done, you can save changes, close all Jupyter windows, 
and use `ctrl+c` in the console to terminate the Jupyter session. 
4) When you are done, you can exit the environment by:
```bash
conda deactivate  # exit the cse404 environment (and return to base)
exit # exit conda
```

## Other Platforms
Instructions for installing `miniconda` on 
[Windows](https://docs.conda.io/projects/conda/en/latest/user-guide/install/windows.html) 
and
[Linux](https://docs.conda.io/projects/conda/en/latest/user-guide/install/linux.html).
