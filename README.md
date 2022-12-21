pix2pix denoise in PyTorch

This project is the modification version of Pix2Pix

**Pix2pix:  [Project](https://phillipi.github.io/pix2pix/) |  [Paper](https://arxiv.org/pdf/1611.07004.pdf) |  [Torch](https://github.com/phillipi/pix2pix) **

## Prerequisites
- Linux or macOS
- Python 3
- CPU or NVIDIA GPU + CUDA CuDNN
- Install [PyTorch](http://pytorch.org) and 0.4+ and other dependencies 
  - For pip users, please type the command `pip install -r requirements.txt`.
  - For Conda users, you can create a new Conda environment using `conda env create -f environment.yml`.
  - 
### pix2pix train/test
- To view training results and loss plots, run `python -m visdom.server` and click the URL http://localhost:8097.
- To log training progress and test images to W&B dashboard, set the `--use_wandb` flag with train and test script
- Train a model:
```bash
#!./scripts/train_pix2pix.sh
python train.py --dataroot ./yourdataroot --name createmodelname --model pix2pix --direction AtoB
```
- Test the model (`bash ./scripts/test_pix2pix.sh`):
```bash
#!./scripts/test_pix2pix.sh
python test.py --dataroot ./yourdataroot --name createmodelname --model pix2pix --direction AtoB
```
- The test results will be saved to a html file here: `./results/createmodelname/test_latest/index.html`. You can find more scripts at `scripts` directory.
