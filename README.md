For now no license so not free to use! 

Notebooks use DeepLabCut body pose estimation data.
I used the labels nose, ear right and left, shoulder right and left and tailbase.

Protocols:
- downsample video framerates from 25 and 22 to 20 as these were not the same in my dataset.
- Slices video beginning/end based on 20 continues frames were all body points are above 0.90 likelihood. 
- Removes body parts points that have a likelihood under 0.5 and performes linear interpolation.
- extracts features (triangle angles, areas and pairwise distances between DeepLabCut labels), same features used in https://github.com/mlfpm/deepof.
- Random forest/ PCA random forest to predict genetic condition 
