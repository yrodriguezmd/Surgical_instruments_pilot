#### Surg100_400 

finetuning of vfnet with poor mAPs at 0.35 at >50epoch run.

Poor inference with Surg500 dataset.



#### Surg100_400_infSurg500

With lower lr (0.0005) compared to the first (0.0025), now with good mAP 67.

When Surg500 was used for inference, generated reasonable bboxes, poor classification apart from Weitlaner.

Refine pseudolabels.  Json annotation now using 8 supercategories.
