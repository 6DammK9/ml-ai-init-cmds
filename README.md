# ml-ai-init-cmds #

"Personal use" install commands / notes for attending ML / AI courses.

## Disclaimer ##

I am not taking any responsibility! Do not expect me constantly tracking the compability issues!

## File list ##

- `cmd.md`: Command lines / notes.
- `mujocopy.md`: **deprecated** Topics on installing and running `mujoco-py` on Windows / WSDL. Current version of mujoco (as in 2201) has been fixed the issue.
- `fcnd.md`: Special for FCND environment. `cmd.py` applies here.

## General requirement for ML / AI ##

- Not joking. You must have all hardwares / softwares in **recent generation** and not fall too far behind the mainstream. Otherwise, you won't even able to get the install packages!

### Hardware ###

- **Intel 4th gen or later**. Most libraries needs **FP16 / FP32 instructions**, which is under Intel x86 CPU with AVX2 instructions, i5 2500K would be drastically slow compared with gaming. AMD/ ARM is not tested. Should be better / newer than AMD Bulldozer \*cough and Nvidia Tegra \*cough?

- **Nvidia GPU with Pascal or newer**. GTX 10 series for general publics. This article will use TF 2.5.0 under this [official tested build configurations](https://www.tensorflow.org/install/source#gpu).
Also, for CUDA inside WSDL2, it is a hard requirement also. Maxwell (as extreme as 750 Ti, but not 780 Ti or Titan Z) is "marginal". See [here](https://docs.nvidia.com/deploy/cuda-compatibility/) and [here](https://developer.nvidia.com/cuda-gpus#compute) for corrosponding CUDA / GeForce driver requirement. For other GPUs (AMD, Apple M1), I never tested [this approch for AMD](https://www.amd.com/en/technologies/infinity-hub/tensorflow) or [this approch for Apple M1](https://github.com/apple/tensorflow_macos). 

- **Sturdy RAM, SSD and HDD**. Your dataset will rushing in & out in GBs. "OEM / Stripped server parts" is nice, but "rebuilt SSD / RAM" is too risky. Location / brand is not important, but do get from reliable sources (for my case, extensive testing under 7-day warrenty from 2nd hand sellers).

- **Powerpul cooling. It is worse than 24/7 mining!** Keep monitoring the temperatures with software. If you can't keep it in pace, consider [Disable Intel Turbo Boost](https://www.geeks3d.com/20170213/how-to-disable-intel-turbo-boost-technology-on-a-notebook/), and be patient.

### Software ###

- **Windows 10 1909 or newer**. You may need WSDL2 for Linux subsystem.

- **Linux Ubuntu 18.04 or newer**. as part of WSDL2.
