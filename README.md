# Cross-species alignment

- Ref: [Xu, Nenning et al., (2020). Cross-species functional alignment reveals evolutionary hierarchy within the connectome. NeuroImage, 223,117346](https://www.sciencedirect.com/science/article/pii/S1053811920308326)
- Download [https://github.com/TingsterX/alignment_macaque-human](https://github.com/TingsterX/alignment_macaque-human)
---
## Joint-embedding alignment between human and macaque

### Cross-species alignment in Joint-embedding space
![Cross-species alignment](https://github.com/TingsterX/alignment_macaque-human/blob/main/animations/cross-species_alignment_28s.gif)

---
### Functional phylogenetic map  (functional connectivity homology index)

<img src=https://github.com/TingsterX/alignment_macaque-human/blob/main/functional_homology/figure_functional_homology_map.png alt="homology map" height=300> 

---
### Cross-species parcellation
<img src=https://github.com/TingsterX/alignment_macaque-human/blob/main/cross-species_parcellation/figure_cross-species_parcellation.png alt="human">

---
### Landmark (Relative Surface Area Human/Macaque)
<img src=https://github.com/TingsterX/alignment_macaque-human/blob/main/landmarks/figure_landmarks.png alt="human" height=400>

---
### Evolutional Areal Expansion (Relative Surface Area Human/Macaque)
<img src=https://github.com/TingsterX/alignment_macaque-human/blob/main/area_expansion/figure_area_expansion_relative_0_36_human.png alt="human" height=150>
<img src=https://github.com/TingsterX/alignment_macaque-human/blob/main/area_expansion/figure_area_expansion_relative_0_36_monkey.png alt="macaque" height=150>

---
### Usage - align your own maps across species 
The folder `deformation_macaque-human` contains spherical deformation files necessary for align your data [Connectome Workbench is required](https://www.humanconnectome.org/software/connectome-workbench).

Note: This is topological contrained surface alignment. The original spherical alignment was created using [MSM](https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/MSM) on 10k resolution surfaces. 

- `surfaces` folder contains the surface files for human and macaque. The human surface data need to be on the [standard surface spaces](https://osf.io/k89fh/wiki/Surface/) - 32k_fs_LR or 10k_fs_LR resolution. The macaque surface data need to be on [MacaqueYerkes19 surface space](https://balsa.wustl.edu/reference/976nz) - 32k_fs_LR or 10k_fs_LR resolution.
- workbench command: `-metric-resample`, `-cifti-resample`, `-label-resample` 
- Macaque (32k_fs_LR) to human: 

    current-sphere: `deformation_macaque-human/L.macaque-to-human.sphere.reg.32k_fs_LR.surf.gii` 

    new-sphere: `surfaces/Human/*k_fs_LR/S1200.L.sphere.*k_fs_LR.surf.gii` 

- Macaque (10k_fs_LR) to human: 

    current-sphere: `deformation_macaque-human/L.macaque-to-human.sphere.reg.10k_fs_LR.surf.gii` 

    new-sphere: `surfaces/Human/*k_fs_LR/S1200.L.sphere.*k_fs_LR.surf.gii`

- Human (32k_fs_LR) to macaque

    current-sphere: `deformation_macaque-human/L.human-to-macaque.sphere.reg.32k_fs_LR.surf.gii` 

    new-sphere: `surfaces/Macaque/*k_fs_LR/MacaqueYerkes19.L.sphere.*k_fs_LR.surf.gii` 

- Human (10k_fs_LR) to macaque

    current-sphere: `deformation_macaque-human/L.human-to-macaque.sphere.reg.10k_fs_LR.surf.gii` 

    new-sphere: `surfaces/Macaque/*k_fs_LR/MacaqueYerkes19.L.sphere.*k_fs_LR.surf.gii` 
---
### More resource
See [https://github.com/TingsterX/PRIME-DE]
