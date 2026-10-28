# Notebook-reported model evaluation

This report transcribes the saved outputs in `notebooks/Omar_Final_Project.ipynb`. No weights or dataset were available in the shared folder, so the numbers have not been reproduced here.

## Separate evaluation output

The evaluation cell reports 825 images, 786 instances, 304 background images, precision 0.7424, recall 0.8351, mAP@0.50 0.8092, mAP@0.50:0.95 0.6472, and calculated F1 0.7860.

| Class | Images | Instances | Precision | Recall | mAP@0.50 | mAP@0.50:0.95 |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Pizza | 21 | 31 | 85.3% | 93.5% | 93.9% | 75.1% |
| Mansaf | 25 | 27 | 72.4% | 87.4% | 78.5% | 60.1% |
| Mjadra | 31 | 32 | 68.7% | 95.8% | 83.9% | 64.7% |
| Maqluba | 32 | 33 | 95.9% | 100.0% | 98.4% | 81.7% |
| Fasolia | 47 | 51 | 71.3% | 94.1% | 88.4% | 80.5% |
| Awameh | 31 | 83 | 56.2% | 55.8% | 59.4% | 41.8% |
| Salad | 31 | 39 | 86.6% | 94.9% | 93.1% | 79.2% |
| Molokhia | 16 | 25 | 83.0% | 78.1% | 91.2% | 72.3% |
| Shawarma | 26 | 51 | 89.1% | 96.1% | 97.8% | 74.1% |
| Macaroni | 35 | 42 | 96.8% | 95.2% | 99.2% | 86.0% |
| Burger | 25 | 26 | 39.5% | 96.2% | 50.9% | 43.7% |
| Kunafa | 31 | 57 | 88.7% | 82.3% | 92.7% | 71.8% |
| Dawali | 35 | 59 | 89.9% | 75.8% | 89.6% | 71.8% |
| Kabsa | 31 | 39 | 70.9% | 53.8% | 61.7% | 40.4% |
| Msakan | 25 | 37 | 72.9% | 79.9% | 84.5% | 66.0% |
| Qatayif | 33 | 93 | 84.6% | 65.1% | 81.4% | 60.8% |
| Cucumber with Yogurt | 32 | 33 | 72.7% | 100.0% | 89.2% | 79.6% |
| Mahashi | 3 | 5 | 14.5% | 60.0% | 13.3% | 12.0% |
| Muhalabia | 11 | 23 | 71.7% | 82.6% | 90.2% | 67.8% |

`Coleslaw Salad` is listed in the class configuration but has no row in this evaluation output, so no per-class score is reported for it here. Mahashi has only 3 evaluation images and 5 instances; its per-class score is especially uncertain.

## Training-cell summary

The training output records 130 epochs completed in 4.901 hours on an NVIDIA A100. Its final summary reports 8,615 images, 9,798 instances, precision 83.7%, recall 83.4%, mAP@0.50 88.8%, and mAP@0.50:0.95 69.7%. The shared YAML currently points both `train` and `val` to the same `food` directory, so this summary should be treated as a training diagnostic, not a held-out result.

## Provenance caveats

- The separate evaluation output scans a `test.cache` file and reports 825 images, but the evaluation cell does not explicitly pass `split="test"`.
- The training cell saves `Model/YOLO_Trained_Model.pt`; a later evaluation cell loads `final_version.pt`. The shared folder does not contain either checkpoint, so the evaluation model cannot be matched to the training run.
- The shared `configs/data1.drive.yaml` has identical `train` and `val` paths. Confirm the split configuration and checkpoint before presenting these values as a verified held-out benchmark.
- The notebook's inference cell output is marked hidden. Separately supplied annotated examples are now included under `assets/prediction-results/`; they are qualitative examples and cannot be independently regenerated here without the checkpoint and source images.
