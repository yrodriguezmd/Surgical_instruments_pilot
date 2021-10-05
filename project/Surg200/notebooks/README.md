#### Surg200 Findings:

Utilizing labelled Surg100 data to finetune a VFnet model, mAP of 0.6 was reached (model Surg100_vfnet.pth).

Using the model to get inferences from the Surg200 dataset, the prediction results are poor.



#### Next step:

Use pretrained VFnet to generate pseudolabels for Surg200, then refine annotations in Roboflow.  --DONE

Merge Surg100 and Surg200 labelled datasets (n= 200), finetune VFnet and generate pseudolabels for Surg300 (n=100)

