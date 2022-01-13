# mujoco topics #

## Need Linux environment ##

Try install mujoco-py (with conda!) with newest version of mujoco first. If it fails, have a look of following articles.

### Spinningup (OpenAI) ###

```bash
bash
source activate spinningup

python -m spinup.run ppo --hid "[32,32]" --env Walker2d-v2 --exp_name mujocotest
python -m spinup.run plot /home/dammk/spinningup/data/mujocotest/mujocotest_s0
python -m spinup.run test_policy /home/dammk/spinningup/data/mujocotest/mujocotest_s0
```

### Spinningup scripts ###

https://spinningup.openai.com/en/latest/user/running.html#launching-from-scripts
https://spinningup.openai.com/en/latest/spinningup/extra_tf_pg_implementation.html

### Mujoco ###

https://github.com/ethz-asl/reinmav-gym/issues/35
https://blog.csdn.net/Youtian_/article/details/103841453
https://zhuanlan.zhihu.com/p/358447406

### WSL2 ###

https://zhuanlan.zhihu.com/p/355606922

```bash
wsl --set-version  Ubuntu-18.04 2
```

### 21H1 / NVML ###

https://blog.zackzhou.com/win10-docker-wsl2-gpu
https://www.ghacks.net/2021/09/03/how-to-upgrade-windows-10-version-21h1-to-21h2-right-now-kb5003791/

### XMING / GLX SERVER ###

https://github.com/microsoft/WSL/issues/6430
https://theunixtips.com/xming-client-4-rejected-from-ip/
https://stackoverflow.com/questions/66497147/cant-run-opengl-on-wsl2

### GLX CLIENT / OPENGL / MESA ###

https://blog.csdn.net/u011715038/article/details/113733006
https://kheresy.wordpress.com/2021/07/01/setup-opengl-in-wsl2/