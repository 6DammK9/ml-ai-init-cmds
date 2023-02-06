# DammK ML / AI CMD pack V2 #

## From stratch. Tested for recent course tasks ( CS5187 ) ##

- Must activate environment first!
- Python 3.11 still too new
- May need linux subsystem (WSL2) which may collides with Windows environment
- Do not use install CMDs in jupyter environment! You will crash your computer!
- Only use pip for last resort (e.g. `torchvision`)
- Be familiar with **minor** software version difference (should be fine for educational use)

## Computation environment ##

- Development mode: (Notebook) ROG GM501GM, Win 10 21H2, WSL2, 6c12t i7-8750, 32GB DDR4 2666, GTX 1060 mobile, 500GB SATA SSD + 16GB M2 Optane
- Production mode: (Workstation) Huananzhi X99-F8D, Win 10 21H2, no linux subsystem, 24c48t 2678v3 x2, 64GB DDR4 2133 ECC, GTX 1080 Ti x2, 500GB SATA SSD + 2TB SATA HDD

## Video / IG links ##

- Coming soon

## Here's the CMDs ##

```bash
#!/bin/bash

# python=3.11 will crash in application!
conda create -n anifusion2-env -c conda-forge scikit-learn python=3.10
conda activate anifusion2-env

# May be fine?
conda install -c conda-forge jupyterlab

# cs6493 tutorial 4
conda install -c conda-forge jupyterlab_widgets
conda install -c conda-forge ipywidgets

# Start jupyter
jupyter lab

# Prefer conda-forge with auto version (older version is not preferred)

# Win11 DLL fix: https://github.com/conda/conda/issues/11795#issuecomment-1340010125
pip install torch torchvision --extra-index-url https://download.pytorch.org/whl/cu116
# Doesn't work
# conda install -c conda-forge pytorch-gpu
# conda install -c conda-forge torchvision
# Should return true
python -c "import torch; print(torch.cuda.is_available())"

# Should be fine with almost no risk
conda install -c conda-forge pandas
conda install -c conda-forge matplotlib
conda install -c conda-forge scikit-image
conda install -c conda-forge scipy
conda install -c conda-forge networkx
conda install -c conda-forge tqdm
conda install -c conda-forge opencv

# Not related (used for AI art research)
pip install safetensors
```
