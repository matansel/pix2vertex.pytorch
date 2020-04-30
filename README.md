# Unrestricted Facial Geometry Reconstruction Using Image-to-Image Translation - Official Pytorch Implementation
[[Arxiv]](https://arxiv.org/pdf/1703.10131.pdf) [[Video]](https://www.youtube.com/watch?v=6lUdSVcBB-k)

Evaluation code for Unrestricted Facial Geometry Reconstruction Using Image-to-Image Translation. Given a single image, finally ported to pyTorch!

## Recent Updates

**`2020.04.30`**: Initial pyTorch release

# What's in this release?

The [original pix2vertex repo](https://github.com/matansel/pix2vertex) was composed of three parts
 - A `lua` based network to perform the image to depth + correspondence maps trained on synthetic facial data
 - A `Matlab` based non-rigid ICP scheme for converting the output maps to a full 3D Mesh  
 - A `Matlab` based shape-from-shading scheme for adding fine mesoscopic details
 
 This repo currently contains our image-to-image network with weights and model ported from the `lua` version and a simple `python` postprocessing scheme.
 - The released network was trained on a combination of synthetic images and unlabeled real images for some extra robustness :)

## Setup & Usage
The project was tested on `Python 3.6.2` with `pyTorch 1.1.0`, full requirements coming soon :)

### Pretrained Model
Models can be downloaded from these links:
- [pix2vertex model](https://drive.google.com/open?id=1op5_zyH4CWm_JFDdCUPZM4X-A045ETex)
- [dlib landmark predictor](https://drive.google.com/open?id=1ZDISv8GUsReE9hrDt2H_WOOsqd7QlwBF)

or simply by running `download.sh`


## TODOs
- [x] Port Torch model to pyTorch
- [x] Release an inference notebook (using [K3D](https://github.com/K3D-tools/K3D-jupyter))
- [ ] Add requirements
- [ ] Pack as wheel?
- [ ] Port the Shape-from-Shading method used in our matlab paper
- [ ] Write a short blog about the revised training scheme 

## Citation
If you use this code for your research, please cite our paper <a href="https://arxiv.org/pdf/1703.10131.pdf">Unrestricted Facial Geometry Reconstruction Using Image-to-Image Translation</a>:

```
@article{sela2017unrestricted,
  title={Unrestricted Facial Geometry Reconstruction Using Image-to-Image Translation},
  author={Sela, Matan and Richardson, Elad and Kimmel, Ron},
  journal={arxiv},
  year={2017}
}
```