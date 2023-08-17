# DiffInfinite

We present DiffInfinite, a hierarchical diffusion model that generates arbitrarily large histological images while preserving long-range correlation structural information. Our approach first generates synthetic segmentation masks, subsequently used as conditions for the high-fidelity generative diffusion process. The proposed sampling method can be scaled up to any desired image size while only requiring small patches for fast training. Moreover, it can be parallelized more efficiently than previous large-content generation methods while avoiding tiling artefacts. The training leverages classifier-free guidance to augment a small, sparsely annotated dataset with unlabelled data. Our method alleviates unique challenges in histopathological imaging practice: large-scale information, costly manual annotation, and protective data handling. The biological plausibility of DiffInfinite data is validated in a survey by ten experienced pathologists as well as a downstream segmentation task. Furthermore, the model scores strongly on anti-copying metrics which is beneficial for the protection of patient data.

![Example Image](images/examples/synth_examples.png)

## Installation

Create a conda environment using the requirements file.

```
conda env create -n env_name -f environment.yaml
conda activate env_name
```

Download and unzip the models (```n_classes``` can be 5 or 10):

```
python download.py --n_classes=5
```

## Usage

Usage example in [Jupyter Notebook](main.ipynb).