## 3D-instance-segmentation-of-Plant-Objects-using-Deep-learning

##### Please use the below-mentioned link to access the source code; (link to my GitLab repository)
https://gitlab.com/Hasal/3d-instance-segmentation

The study and source code presented by Back et al.[1] is modified to perform a three-dimentional instance segmentation task (based on RGB and Depth input data) of plant objects. 
The instance segmentation of plant objects performed here is a multi-class segmentation with the following class labels.

* Class Labels:

    * 'Singularized Cutting'
    * 'Target Cutting'
    * 'Occluded Cutting'
    * 'Double Occluded Cutting'
    * 'Remains'
(Both Occluded Cutting and Double Occluded Cutting classes are merged for segmentation)

This work is designed to be used as part of a vision-based system for object (plant) recognition, robotic separating and sorting of the overlapped cuttings of plants in a robotic unit. This is an implementation of a 3D instance segmentation method with good performance for complex shaped objects such as plants.

#### Execution Procedure

##### 1. Environment Setup
First, install conda and create a new conda environment.
```
$ conda create -n <environment_name> python=3.7
$ conda activate <environment_name>
$ conda install pytorch torchvision torchaudio cudatoolkit=10.2 -c pytorch-lts
$ pip install imgviz tqdm tensorboardX pandas opencv-python imutils pyfastnoisesimd scikit-image pycocotools
```
##### 2. Train
```
$ bash script_trainA.sh
```
Resume training from a checkpoint,
```
$ bash script_train.sh
```
##### 3. Evaluation
```
$ bash script_eval.sh
```
##### 4. Segmentation Visualization
```
$ bash script_visual.sh
```


#### Based on the Original Work,
##### Synthetic RGB-D Fusion (SF) Mask R-CNN for unseen object instance segmentation

> S. Back, J. Kim, R. Kang, S. Choi and K. Lee. **Segmenting unseen industrial components in a heavy clutter using rgb-d fusion and synthetic data.** 2020 IEEE International Conference on Image Processing (ICIP). IEEE, 2020. [[Paper]](https://ieeexplore.ieee.org/abstract/document/9190804) [[Video]](https://youtu.be/eB4LKfYZwYo)

#### Citation
```
[1] @inproceedings{back2020segmenting,
  title={Segmenting unseen industrial components in a heavy clutter using rgb-d fusion and synthetic data},
  author={Back, Seunghyeok and Kim, Jongwon and Kang, Raeyoung and Choi, Seungjun and Lee, Kyoobin},
  booktitle={2020 IEEE International Conference on Image Processing (ICIP)},
  pages={828--832},
  year={2020},
  organization={IEEE}
}