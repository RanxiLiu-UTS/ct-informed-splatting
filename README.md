<div align="center">

# BridgeSplat: Bidirectionally Coupled CT and Non-Rigid Gaussian Splatting for Deformable Intraoperative Surgical Navigation

### MICCAI 2025

Maximilian Fehrentz · Alexander Winkler · Thomas Heiliger · Nazim Haouchine · Christian Heiliger · Nassir Navab

**Computer Aided Medical Procedures, TU Munich**

**Department of General, Visceral, and Transplantation Surgery, Hospital of the LMU Munich**

**Harvard Medical School, Brigham and Women's Hospital**

### [Project Page](https://maxfehrentz.github.io/ct-informed-splatting/) | [Paper](https://papers.miccai.org/miccai-2025/paper/4699_paper.pdf) | [Dataset](https://huggingface.co/datasets/maxfehrentz/BridgeSplat)

</div>

---
Official implementation of **BridgeSplat** (MICCAI 2025).

## Installation

### Setup

1. **Clone the repository recursively:**
```bash
git clone --recursive https://github.com/maxfehrentz/ct-informed-splatting.git
cd ct-informed-splatting
```

2. **Create conda environment:**
```bash
conda env create -f environment.yaml
conda activate bridgesplat
```

3. **Install submodules:**
```bash
# Gaussian Rasterization
cd src/submodules/gaussian-rasterization
python setup.py install

# Simple KNN
cd ../simple-knn
python setup.py install

# ARAP extension
cd ../../cpp_extensions/arap
python setup.py install

# Return to root
cd ../../..
```

> **Note:** Have to navigate to each folder individually as they contain relative references.

## Dataset

Download the dataset from [HuggingFace](https://huggingface.co/datasets/maxfehrentz/BridgeSplat) and place it in a top-level `data/` folder.

## Usage

Run experiments by specifying a configuration file, e.g.:

```bash
python run.py configs/SOFA/sofa_liver_in.yaml --visualize
```

Additional config examples can be found in the `configs/` directory.

## Citation

If you find this work useful, please cite:

```bibtex
@inproceedings{fehrentz2025bridgesplat,
  title={BridgeSplat: Bidirectionally Coupled CT and Non-rigid Gaussian Splatting for Deformable Intraoperative Surgical Navigation},
  author={Fehrentz, Maximilian and Winkler, Alexander and Heiliger, Thomas and Haouchine, Nazim and Heiliger, Christian and Navab, Nassir},
  booktitle={International Conference on Medical Image Computing and Computer-Assisted Intervention},
  pages={44--53},
  year={2025},
  organization={Springer}
}
```

## 📧 Contact

For questions, please open an issue or contact [maximilian.fehrentz@tum.de](mailto:maximilian.fehrentz@tum.de).

## Acknowledgement
We are building on the code of ["Online 3D reconstruction and dense tracking in endoscopic videos"](https://github.com/mhayoz/online_endo_track) (MICCAI 2024).