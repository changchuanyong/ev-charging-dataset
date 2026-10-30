# ev-charging-dataset

Backup archives for the robot-ev-charging project (Git LFS).

## Files

| File | Size | SHA256 |
| --- | --- | --- |
| robot-ev-charging-dataset-20261030.zip | 164,371,373 B (156.76 MB) | d2488cc514a4f3a17e4ec2c099117a045802228b3bae5f4e8cb7a85c76987e82 |
| robot-ev-charging-model-20261030.zip | 6,112,574 B (5.83 MB) | f54f7cb2d507ad94476961a144a059905b55c270726708762ca354cb016abe5f |

## Contents

- dataset zip: `dataset/vision` - 841 files, 234 unique RGB training images,
  YOLO labels, per-image records and migrated source annotations.
- model zip: `runs/detect_split_20261030T110042Z_105be6be` - best.pt,
  training_report.json, post_training_audit.json, training_manifest.json,
  epoch/validation coverage, results.csv, args.yaml, preview_config.json.

Source code and evidence: https://github.com/changchuanyong/robot-ev-charging
(code/evidence commit 3d0b6d2; the dataset library was committed locally as
f5dcf19 and is not pushed to the code repository).

## Restore

Extract each zip at the root of a robot-ev-charging checkout:

```powershell
Expand-Archive -Path robot-ev-charging-dataset-20261030.zip -DestinationPath <repo> -Force
Expand-Archive -Path robot-ev-charging-model-20261030.zip -DestinationPath <repo> -Force
```

Each zip contains RESTORE_*.txt and SHA256SUMS_*.txt for verification.

## Clone

```powershell
git lfs install
git clone https://github.com/changchuanyong/ev-charging-dataset.git
```
