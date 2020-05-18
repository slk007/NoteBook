## conda 


**list of conda environments present on system**
```
conda info --envs 
conda info -e
```

**Creating a conda env with python version x.x**
```
conda create -n yourenvname python=x.x anaconda
```

**Installing Django in env:**
```
pip install django
```


**Activating environment**
```
source activate yourenvname
conda activate yourenvname
```


**Deactivating environments**
```
source deactivate
conda deactivate
```


**Deleting the environment**
```
conda remove --name <myenvname> --all
```