# pysumma_camels

#### Workflow 0: Summa team members with access can click on this private resource (until further notice by data owners)
[CAMELS SUMMA Demonstration Resource](https://www.hydroshare.org/resource/b4c7120f38e843c8bdfc137ea1609989/).  View the reources. Edit metadata.    {future option:  Open With blue button. Select MyBinder. }

#### Workflow 1: Run a SUMMA model using CAMELS data.
 
Go to HydroShare.  Groups. Search for a Compute Access Resource Group.

Request access to [CUAHSI JupyterHub](https://www.hydroshare.org/group/156).

Click on the Resources tab or search:
[CAMELS SUMMA Demonstration Resource](https://www.hydroshare.org/resource/b4c7120f38e843c8bdfc137ea1609989/)

#### Workflow 2: Develop Notebooks that run SUMMA using CAMELS data.

If you are already a HydroShare user, you can also start here: 
 - In Github, start from  ashleymedin/pysumma_camels or a branch in Github.  Fork the repository.  
 - In a new browser, go to https://jupyterhub.cuahsi.org/   Read the agreement and authorize your HydroShare user account. 
 - Select the kernel for Python 3.7 - SUMMA Modeling.  This an environment built with the SUMMA model and supporting tools pre-installed. For more information on the SUMMMA model, visit the project webpage.
 - From the Jupyter Lab Launcher. Open a new Terminal.  `git clone <your_repository_fork_or_branch hyperlink>`
 - Run the Notebooks. 
 
 #### Workflow 3: Develop Notebooks that run SUMMA using CAMELS data.
Request access to [CyberGIS-Jupyter for Water](https://www.hydroshare.org/group/157)
 
Click on the Resources tab or search:
[CAMELS SUMMA Demonstration Resource](https://www.hydroshare.org/resource/b4c7120f38e843c8bdfc137ea1609989/)

##  below is a work in progress with version updates 

# Creating a Working Environment

We recommend using Anaconda to create a fresh Python environment with all dependencies installed. After installing Anaconda, simply run the commands below with your desired environment name in place of `MY_ENVIRONMENT_NAME`:

```
conda create -n MY_ENVIRONMENT_NAME --file requirements.txt
```

activate the environment and start a jupyter server

```
source activate MY_ENVIRONMENT_NAME
jupyter notebook
```
### Debugging a Working Environment
Are you getting errors?  Here are some suggested steps. If you still have issues, email help@cuahsi.org or reach out to us (comment on this resource or see emails in HydroShare profiles) and we will invite you to the HydroShare Slack #landlab channel. 

Bug: PackagesNotFound

```
PackagesNotFoundError: The following packages are not available from current channels.
```

Reduce the number of packages that were not available by running the following command

```
conda config --append channels conda-forge
```

Bug: Conda vs.Pip Install

If you get errors for a few packages, remove them from the requirements.txt file until you successfully created the conda environment.

```
conda create -n MY_ENVIRONMENT_NAME --file requirements.txt
```

Any packages that didn't get installed during creation of conda environment can be pip installed separately in the newly created conda environment.
for example: 

```
pip install hs-restclient==1.3.5
```

CAMELS Resources 
