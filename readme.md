# Estimating more camera poses for ego-centric videos is essential for VQ3D

*The implementation of 1st winner for VQ3D challenge in Second International Ego4D Workshop at ECCV 2022.*

## Installation
Please follow [Ego4D VQ3D Benchmark](https://github.com/EGO4D/episodic-memory/blob/main/VQ3D/README.md) to produce the required VQ2D result and baseline VQ3D results (e.g., video clip frames, camera intrinsics, camera poses from the baseline method) at first.

## RUN
After that, check the script `run_colmap.sh` we provide in `vq3d` to get COLMAP estimated poses.
## Registration
Use the following command to collect and register your COLMAP results to Matterport Scan coordinate system.

```
python register_colmap_baseline.py --merge_pose data/poses_json/all_clips_base_colmap.json --debug --align ra

```
The output `all_clips_base_colmap.json` will be your camera poses file.

## Evaluation and Test
Carefully follow the steps in [Ego4D VQ3D Benchmark](https://github.com/EGO4D/episodic-memory/blob/main/VQ3D/README.md) to evaluate and test the results.