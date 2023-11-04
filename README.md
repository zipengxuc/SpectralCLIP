# SpectralCLIP
Code for WACV 2024 paper [SpectralCLIP: Preventing Artifacts in Text-Guided Style Transfer from a Spectral Perspective](https://arxiv.org/pdf/2303.09270.pdf).

![](images/teaser.png)

## Updates
_24 Oct 2023_: SpectralCLIP is accepted by WACV 2024

_03 Nov 2023_: We release the code of SpectralCLIP


## Usage 

To use SpectralCLIP for style transfer, we implement the method based on [CLIPstyler](https://github.com/cyclomon/CLIPstyler).

### Setup
```
$ conda create -n SpectralCLIP python=3.6
$ conda install --yes -c pytorch pytorch=1.7.1 torchvision cudatoolkit=11.0
$ pip install ftfy regex tqdm
$ pip install git+https://github.com/openai/CLIP.git
$ pip install torch-dct
```

### Style Transfer with SpectralCLIP

```
python train_SpectralCLIP.py --band 2 --text "Giorgio Morandi"
```
To change the filtering band combination, modify the ```--band``` argument.

Here are the filtering band combinations we found effective for different styles:

|Filter | Style |
|---|---|
| c1  |  Lowbrow, Outsider art, Visionary art, Rosy-color oil painting |
| c2  |  Pop art, Cartoon, Giorgio Morandi, Harlem Renaissance, Neon art, Contemporary art|
| c3  |  Fauvism, Digital art|

