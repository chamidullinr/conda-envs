# Conda - Managing Environments

This section contains list of useful `conda` commands for managing environments, 
i.e. creating, cloning and removing environments. 
For a complete list of conda commands, see [Conda Docs](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html).

### General commands
Activate an environment:
```bash
conda activate myenv
```

Deactivate an environment:
```bash
deactivate
```

List all available environments: 
```bash
conda env list
```

### Creating, Cloning and Removing
Create an environment with name `myenv`:
```bash
conda create -n myenv python=3.6
```

Clone an existing environment into a new one:
```bash
conda create --name myclone --clone myenv
```

Remove an existing environment `myenv`:
```bash
conda remove -n myenv --all
```

### Managing yml files
Create an environment from a yml file:
```bash
conda env create -f environment.yml
```

Export an active environment to a yml file:
```bash
conda env export --no-builds > environment.yml
```
