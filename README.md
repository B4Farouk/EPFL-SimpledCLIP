# SimpledCLIP

## Section I: Datasets
We do not use any internal nor external datasets, so as long as the person willing to reproduce our work respects the same repository architecture as ours, all the code should run correctly provided you have the needed dependencies (see the section III).

## Section II: Files

### prompts.md
Presents the prompts we used in this project.

### models_and_parameters.md
Presents the model versions and hyperparameters and optimization parameters that we used most often and/or that worked best empirically.

### basicModel_f_lbs_10_207_0_v1.0.0.pkl
A pickled SMPL model for a female mesh.

### basicModel_neutral_lbs_10_207_0_v1.0.0.pkl
A pickled SMPL model for a neutral mesh.

### f_02_alb.002.png
The 2D texture map we use in our project when we mention a human-textured mesh.

### SMPL_female_with_colors.obj
3D texture to apply to the mesh.

## Section III: Codebase

### smpl.py
Contains our implementation of an SMPLwrapper, a class that uses SMPL underneath and exposes only what we need.

### textures.py
Contains our implementations of textures and texture mappings used in this project.

### optimization.py
Contains our optimization environment class together with its configuration class (optimization parameters and algorithms, loss aggregations, learning rate scheduling...etc) and tracking class (tracking losses, poses and shapes)

### rendering.py
Contains our Renderer class, together with the rasterization, shader and cameras settings we used in this project.

### model.py
Contains the functions to compose SMPL, the differentiable renderer and CLIP into an instance of SimpledCLIP.

### clipwrapper.py
Contains our implementation of an SMPLwrapper, a class that uses CLIP underneath and exposes only what we need.

### aux_functions.py
Contains a few helper functions. Those are not really relevant for the project, but rather for convenience.

## Section IV: How to reproduce our setup ?
All of our results detailed in the report and more are available on our SimpledCLIP_demo.ipynb. **We strongly recommend that you run this notebook on google colab, as that was the environment we used.** Please refer to the section "X. Reproducibility" of our report for further details about parameter values.

Note: If you run the notebook on your own environment, please know that we assume that it has all the core python libraries. Please refer to the requirements.txt for further details about the dependencies you may need in that case.
