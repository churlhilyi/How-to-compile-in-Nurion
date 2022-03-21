## python_envs_for_postw90_output.md
the python output file of postw90(k-slice of berry curvatrure) depend on matplotlib==2.1.2 version

1. Use  __conda__ command to create the evs: 

        $ conda create -n postw90 matplotlib==2.1.2
        $ conda activate postw90
        $ conda install scipy

2. Use  __python -mpip__ command to install __nagrid__:

        $ python -mpip install git+https://github.com/matplotlib/natgrid.git



Done!

-------------------------
