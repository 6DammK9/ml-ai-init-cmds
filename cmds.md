# DammK ML / AI CMD pack #

## From stratch. Tested for recent course tasks ( CS5489 / CS5491 / CS6493 ) ##

- Must activate environment first!
- Python 3.10 still too new
- May need linux subsystem (WSL2) which may collides with Windows environment
- Do not use install CMDs in jupyter environment! You will crash your computer!
- Only use pip for last resort (e.g. `mujoco-py`)
- Be familiar with **minor** software version difference (should be fine for educational use)

## Primary environment ##

- **Tested** Notebook: ROG GM501GM, Win 10 20H2, WSL2, 6c12t i7-8750, 32GB DDR4 2666, GTX 1060 mobile, 500GB SATA SSD + 16GB M2 Optane
- **Tested** Workstation: X99-F8D, Win 10 20H2, no linux, 24c48t 2678v3 x2, 64GB DDR4 2133 ECC, GTX 1080 Ti, 500GB SATA SSD + 2TB SATA HDD  

## Video / IG links ##

- [mujoco-py on WSL2](https://www.youtube.com/watch?v=6LmCVQ0zov8&ab_channel=6DAMMK9)

## Running the CMDs ##

- For installation, recommended to use elevated command prompt. [How to Open the Command Prompt as Administrator in Windows 8 or 10](https://www.howtogeek.com/194041/how-to-open-the-command-prompt-as-administrator-in-windows-8.1/)

- After installation, VSCode > Terminal > Add > Command Prompt. *Do not use PowerShell*. Verify the console output (no `PS C:\`, and in auto):

```txt
C:\Users\User\Downloads\ml-ai-init-cmds-main>C:/ProgramData/Miniconda3/Scripts/activate

(base) C:\Users\User\Downloads\ml-ai-init-cmds-main>conda activate sklearn-env

(sklearn-env) C:\Users\User\Downloads\ml-ai-init-cmds-main>
```

## Here's the CMDs ##

```bash
#!/bin/bash

# python=3.10 will lead to almost no avaliable packages!
conda create -n sklearn-env -c conda-forge scikit-learn python=3.9
# Activate the new environment first
conda env list
conda activate sklearn-env

# Prefer conda-forge with auto version (older version is not preferred)

# conda-forge failed on 3.9
conda install -c pytorch pytorch
conda install -c pytorch torchvision
conda install -c pytorch torchaudio

# 2.7.0 will have serious issue (cudnn issue)
# 2.6.0 has some weird bug (e.g. keras not found)
conda install -c conda-forge tensorflow-gpu=2.5.0

# Should be fine with almost no risk
conda install -c conda-forge pandas
conda install -c conda-forge matplotlib
conda install -c conda-forge scikit-image
conda install -c conda-forge scipy
conda install -c conda-forge networkx

# Finally the jupyter notebook
conda install -c conda-forge jupyterlab

# Start jupyter (after installation)
jupyter lab
```
