# Convex Optimization - Assignment Solution


This repository contains my assignment solution for the Convex Optimization course (430.709A_001) offered by Seoul National University (Fall 2018).
Based on [sparse-depth-sensing](https://github.com/sparse-depth-sensing/sparse-depth-sensing), which contains MATLAB codes and data for sparse depth sensing, I used different solver [CVX](http://cvxr.com/cvx/).
Sparse depth sensing is the problem of dense depth image reconstruction from very limited amount of measurements. 
Please refer to the paper [*Sparse Depth Sensing for Resource-Constrained Robots*](https://arxiv.org/abs/1703.01398) and click on the [YouTube video](https://www.youtube.com/watch?v=vE56akCGeJQ) below for more details.

## Requirement
 - Matlab R2015a or later versions, including
   - the Computer Vision System Toolbox
   - the Robotics System Toolbox

## Usage
 - run `demo_single_frame.m` for a demo of the reconstruction algorithm on samples from each individual frame of depth images.
 - run `demo_multi_frame.m` for a demo of the reconstruction algorithm on samples collected across multiple frames, given odometry information.
 - run `demo_middlebury.m` for a demo of the reconstruction algorithm on the Middlebury dataset.

## Code Structure
The code is structured as follows.
 - `lib/algorithm` contains the core code, i.e., the formulation of our optimization problem (in `l1ReconstructionOnImage.m`).
 - `lib/nesta_solver` is the implementation of the NESTA fast solver tailored to our problem.
 - `lib/geometry` handles all geometry related implementations (e.g., rigid body transformation, image projection).
 - `lib/sampling` provides functions for create a small set of measurements from the ground truth depth image.
 - `lib/utility` contains other helper functions.

## Reference


	@article{Ma2017SparseDepthSensing,
	  title={Sparse Depth Sensing for Resource-Constrained Robots},
	  author={Ma, Fangchang and Carlone, Luca and Ayaz, Ulas and Karaman, Sertac},
	  journal={arXiv preprint arXiv:1703.01398},
	  year={2017}
	}

	@inproceedings{ma2016sparse,
	  title={Sparse sensing for resource-constrained depth reconstruction},
	  author={Ma, Fangchang and Carlone, Luca and Ayaz, Ulas and Karaman, Sertac},
	  booktitle={Intelligent Robots and Systems (IROS), 2016 IEEE/RSJ International Conference on},
	  pages={96--103},
	  year={2016},
	  organization={IEEE}
	}

