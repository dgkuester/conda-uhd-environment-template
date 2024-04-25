
## Template for a conda environment
There should be one of these files for every source code project. Copy the environment.yaml into your source code tree.

## Basic Usage

### 1. Adjust dependencies
For this, edit environment.yaml

### 2. Create an environment
```bash
conda env create -p .venv -f environment.yaml
```

### 3. Activate the created environment.

```bash
conda activate ./.venv
```

### 4. Making changes to the environment
To change the environment, adjust environment.yaml. Do this instead of directly calling `conda install`
because this forces all of the dependencies to be resolved at the same time, which from experience
works better than resolving the dependency versions separately.

After making the changes to your environment.yaml, run this:

```bash
conda env update -p .venv -f environment.yaml
```
