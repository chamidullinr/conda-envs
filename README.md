# Conda Environments

Repository of Conda Environments that can be used for different use-cases such as 
General Machine Learning, Natural Language Processing, Computer Vision, or Deep Leaning. Environments are using Python version 3.6.

Keeping various conda environments is helpful when working on several machines and on different projects 
as it gets time-consuming to install libraries and maintain correct versions.  

**List of available Environments**
* [*numpy_base*](numpy_base.yml) - General environment with packages for data processing, visualization and machine leaning. It is useful to use this as a starting point and create new environments by cloning *numpy_base*.
    * Python = 3.6
    * Packages: Numpy, Pandas, Matplotlib, Seaborn, Scipy, Scikit-learn


* [*pytorch_cpu*](pytorch_cpu.yml) - Environment with PyTorch for Deep Learning using CPU. 
    * Python = 3.6
    * Cloned from *numpy_base*
    * Packages: PyTorch, torchtext, tensorboard
* [*pytorch_cpu_spyder*](pytorch_cpu_spyder.yml) - *pytorch_cpu* environment with Spyder IDE (version 4) and Jupyter Notebook.


* [*ktrain*](ktrain.yml) - Environment with ktrain and transformers library for Deep Learning with pre-trained models such as BERT. The main models of ktrain library are build on TensorFlow, however there are also some models such as One Shot Learning that are based on PyTorch. 
    * Python = 3.6
    * Cloned from *numpy_base*
    * Packages: ktrain, transformers, TensorFlow, PyTorch
* [*ktrain_spyder*](ktrain_spyder.yml) - *ktrain* environment with Spyder IDE (version 4) and Jupyter Notebook.


## Conda - Managing Environments
This section contains list of useful conda commands for managing environments, i.e. creating, cloning and removing environments. 
For a complete list of conda commands, see [Conda Docs](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html).

### General commands
Activate an environment:
```bash
conda activate myenv
```

Deactive an environment:
```bash
deactivate
```

List all available environments: 
```bash
conda info --envs
```

### Creating, Cloning and Removing
Create an environment:
```bash
conda create -n myenv python=3.6
```

Clone an existing environment into a new one:
```bash
conda create --name myclone --clone myenv
```

Remove an existing environment:
```bash
conda remove --name myenv --all
```

### Managing yml files
Create an environment from a yml file:
```bash
conda env create -f environment.yml
```

Export an active environment to a yml file:
```bash
conda env export > environment.yml
```
