# MultiPlaneNeRF: Neural Radiance Field with Non-Trainable Representation

<div style="display: flex;">
  <img src="/images/drums_mi_2_spiral_550000_rgb.gif" alt="Image" width="200">
  <img src="/images/ship_mi_spiral_500000_rgb.gif" alt="Image" width="200">
  <img src="/images/lego_mi_final_spiral_500000_rgb.gif" alt="Image" width="200">
</div>

Code based on NeRF pytorch implementation by yenchenlin: https://github.com/yenchenlin/nerf-pytorch, that implements the method of MultiPlaneNeRF paper.

## Requirements
- Dependencies stored in `requirements.txt`.
- Python 3.9.12
- CUDA

## Usage

### Installation
Create new conda environment and install requirements specified in: `pip install -r requirements.txt`

Download official NeRF dataset

### Running - single object
Official NeRF data, can be dowloaded for `lego` model by running:
```
bash download_example_data.sh
```

To run a training for MultiPlaneNeRF, run the Python script:

```
python run_nerf.py --config configs/lego.txt
```

### Running - generalized

We use custom dataset adapted from Shapenet, which contains cars, chairs and planes classes. Each class has 50 images with size 200x200 and corelated pose for each render.

[Download dataset here.](https://ujchmura-my.sharepoint.com/:u:/g/personal/przemyslaw_spurek_uj_edu_pl/ETy5BPpf4ZFLorYEpXxhRRcBY1ASvCqDCgEX_h75Um6MlA?e=MTJdaj)

Put data folders in local path: `./data/multiple` (same path as `datadir` in config files)

To run a training for MultiPlaneNeRF in generalized mode, run the Python script:

```
python run_nerf_many_generalize.py --config configs/generalized_cars.txt
```
