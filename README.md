# ETH3D Camera Model Implementations #

This repository contains implementations of the camera model used in the ETH3D
benchmark.

* The "cpp" folder contains a C++ implementation without any dependencies.
* The "cpp-cuda" folder contains a C++ implementation which is CUDA-compatible,
  i.e., it requires CUDA to compile and can be used within CUDA code (but
  also within CPU code).
* The "matlab-octave" folder contains a small script which can be used to
  compute derivatives with MatLab or octave.

**Please notice**: The C++ implementations assume a different pixel coordinate
convention than the camera calibrations provided by the benchmark. The
calibration format used by the benchmark assumes (0, 0) in pixel coordinates to
be the top-left corner of the top-left pixel, while the camera model
implementations assume (0, 0) to be the center of the top-left pixel. The
calibrations given by the benchmark can be easily converted to the other format
by subtracting 0.5 from cx and cy.

If you use this code for research, please cite our paper:

T. Schöps, J. L. Schönberger, S. Galliani, T. Sattler, K. Schindler, M. Pollefeys, A. Geiger, "A Multi-View Stereo Benchmark with High-Resolution Images and Multi-Camera Videos", Conference on Computer Vision and Pattern Recognition (CVPR), 2017. \[[Bibtex](https://www.eth3d.net/data/schoeps2017cvpr.bib)\]\[[PDF](https://www.eth3d.net/data/schoeps2017cvpr.pdf)\]\[[Supplementary](https://www.eth3d.net/data/schoeps2017cvpr-supp.pdf)\]
