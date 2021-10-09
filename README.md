## Object Detection for Surgical Instruments

#### Objective:

Develop an application that can reliably locate and identify surgical instruments in an image.

#### Summary of Methodology:

#### 1.  Develop a teacher model
  
  a.  Create labelled data (n = 500 - 1000)
  
      i.   Generate pseudolabels using a pretrained model (VFnet, RetinaNet in Airctic/IceVision) (n=100)
      
      ii.  Refine annotation using annotation tool in Roboflow
      
      iii. Iteratively generate pseudolabels by passing through fine-tuned models (n= 100 per iteration)
      
  b.  At labelled data n = 500 - 1000, create pseudolabels by running unlabelled images (n= 4000) through:
  
      i.  VFnet with pretrained weights
      
      ii. VFnet with random initialized weights
      
#### 2.  Develop a student model

      i.  Merge the labelled data (from 1.a.) with the pseudolabels (from 1.b)
      
      ii. Run through a VFnet configuration with randomly initialized weights
      
#### 3.  Test on held-out test dataset (n= 500)

#### 4.  Deploy



### Surgical_instruments Repository

A collection of images, annotations and notebooks for project development of a surgical instrument detection tool

#### A. PILOT

#### 1. Manual_Labelling

#### a. Roboflow

####      i. Instruments curl, parse

Focus:  Using images manually gathered from the net, annotated in roboflow, exported tensorflow OD csv format via curl; parsing done; n_original =10, n_filename = 21, n_class = 13

#### b.  CVAT


#### B.  PROJECT

Datasets For Pseudolabelling

#### 1.  Surg100

Contains:  Downloaded images, comprising of 15 classes, at 5-7 representatives per class, N=100; for inference and pseudolabel generation, refining of annotation.

#### Classes (Supercategories/ Name):

#### Scalpel:   
Scalpel

#### Scissors:      
Mayo_metz

Iris

Potts

#### Forceps:
Forceps

#### Clamp:
Hemostat

Bulldog

Towel_clip

#### Needle_holder:
Castroviejo

#### Retractor:
Weitlaner

Richardson

Army_navy

#### Suction:
Frazier

Yankauer

#### Needle:
Needle

Refined annotations downloaded in COCO JSON form and RetinaNet CSV form.

#### Surg200

Mixed surgical instruments, N=100, n_classes = 15, n_supercategories = 8.

--> Merge Surg100 and Surg200, fine tune Vfnet


#### Annotation Tool insights

- initial label assist not good, but as progress through the process, suggestions become better

- train/ val/ test split representatives are preserved when projects are merged
