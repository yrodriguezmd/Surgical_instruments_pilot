### Surgical_instruments

A repository of notebooks for project development of a surgical instrument detection tool

#### A. Pilot

#### 1. Manual_Labelling

#### a. Roboflow

####      i. Instruments curl, parse

Focus:  Using images manually gathered from the net, annotated in roboflow, exported tensorflow OD csv format via curl; parsing done; n_original =10, n_filename = 21, n_class = 13

#### b.  CVAT


#### B.  Datasets For Pseudolabelling

#### 1.  Surg100

Contains:  Downloaded images, comprising of 15 classes, at 5-7 representatives per class, N=100; for inference and pseudolabel generation, refining of annotation.

Classes:

Scalpel:      
Scalpel

Scissors:      
Mayo_metz
Iris
Potts

Forceps:
Forceps
Clamp:
Hemostat
Bulldog
Towel_clip

Needle_Holder:
Castroviejo

Retractor:
Weitlaner
Richardson
Army_navy

Suction:
Frazier
Yankauer

Needle:
Needle

#Finding:# might be possible to upload directly to Roboflow and use COCO-assisted labelling.

Refined annotations downloaded in COCO JSON form and RetinaNet CSV form.

