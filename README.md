# Line Drawing Guided Progressive Inpainting of Mural Damages
Mural image inpainting, Mural damage repair, Line drawing guided image inpainting


## MuralNet: Line Drawing Guided Progressive Inpainting of Mural Damages
We released the codes of this work, and named this method as MuralNet.

## Prerequisites
- Python 3.7
- PyTorch 1.6
- NVIDIA GPU + CUDA cuDNN


## Dataset
### Images
We built a mural dataset for training and testing MuralNet.

## Getting Started
### Training

MuralNet is trained in two stages: 1) training the coarse network, 2) training the whole model. 

To train the model, modify the training parameters in `checkpoints/config.yml`, you can refer to [edge-connect](https://github.com/knazeri/edge-connect) for specific format.

Run the code for training:
```bash
python train.py
```

### Testing
We provide 10 images in `checkpoints/test` for testing, run the code:
```bash
python test.py
```
Directory of testing images can be modified in `main.py`, the network requires images, corresponding line drawings and mask for inpainting.

## Acknowledgment
Our implementation is mainly based on the code framework of [edge-connect](https://github.com/knazeri/edge-connect). Thanks for the authors of this paper as listed below.

```bash
@inproceedings{nazeri2019edgeconnect,
  title={EdgeConnect: Generative Image Inpainting with Adversarial Edge Learning},
  author={Nazeri, Kamyar and Ng, Eric and Joseph, Tony and Qureshi, Faisal and Ebrahimi, Mehran},
  journal={arXiv preprint},
  year={2019},
}
```
