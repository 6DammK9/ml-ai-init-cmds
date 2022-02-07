# DammK ML / AI CMD pack #

## From stratch. Tested for recent course tasks ( CS5489 / CS5491 / CS6493 ) ##

- Must activate environment first!
- Python 3.10 still too new
- May need linux subsystem (WSL2) which may collides with Windows environment
- Do not use install CMDs in jupyter environment! You will crash your computer!
- Only use pip for last resort (e.g. `mujoco-py`)
- Be familiar with **minor** software version difference (should be fine for educational use)

## Primary environment ##

- Notebook: ROG GM501GM, Win 10 20H2, WSL2, 6c12t i7-8750, 32GB DDR4 2666, GTX 1060 mobile, 500GB SATA SSD + 16GB M2 Optane
- Workstation: X99-F8D, Win 10 20H2, no linux, 24c48t 2678v3 x2, 64GB DDR4 2133 ECC, GTX 1080 Ti, 500GB SATA SSD + 2TB SATA HDD  

## Video / IG links ##

- [mujoco-py on WSL2](https://www.youtube.com/watch?v=6LmCVQ0zov8&ab_channel=6DAMMK9)

## Here's the CMDs ##

```bash
#!/bin/bash

# python=3.10 will lead to almost no avaliable packages!
conda create -n sklearn-env -c conda-forge scikit-learn python=3.9
# Activate before calling jupyter
conda env list
conda activate sklearn-env

# May be fine?
conda install -c conda-forge jupyterlab

# cs6493 tutorial 4
conda install -c conda-forge jupyterlab_widgets
conda install -c conda-forge ipywidgets

# Start jupyter
jupyter lab

# Prefer conda-forge with auto version (older version is not preferred)

# conda-forge failed on 3.9
# supressed by torchtext: https://github.com/pytorch/text
conda install -c pytorch pytorch
conda install -c pytorch torchvision
conda install -c pytorch torchaudio

# cs6493 tutorial 2
conda install -c pytorch torchtext
conda install -c conda-forge ray-tune

# 2.7.0 will have serious issue (cudnn issue)
# 2.6.0 has some weird bug (e.g. keras not found)
conda install -c conda-forge tensorflow-gpu=2.5.0

# Should be fine with almost no risk
conda install -c conda-forge pandas
conda install -c conda-forge matplotlib
conda install -c conda-forge scikit-image
conda install -c conda-forge scipy
conda install -c conda-forge networkx

# Optional: CS6493 asg1 (Testing only)
# transformers includes tokenizers
# conda install -c conda-forge tokenizers

# cs6493 tutorial 3
conda install -c conda-forge datasets

# cs6493 tutorial 4
conda install -c conda-forge transformers
```
