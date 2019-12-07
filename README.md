
## Directory structure
```
├── TrashNet-Collage
│   ├── Split
│   │   ├── test_set
│   │   ├── train_set
│   │   └── val_set
│   ├── annotations
│   │   ├── voc_xmls
│   │   ├── yolo_labels
│   │   ├── label_map.pbtxt
│   │   ├── test.record
│   │   ├── test_labels.csv
│   │   ├── train.record
│   │   ├── train_labels.csv
│   │   ├── val.record
│   │   ├── val_labels.csv        
|   ├── classes.txt
│   └── images

```

# Description

This folder has images after the following preprocessing :
a) 100 images from each category was taken from the original TrashNet dataset (https://github.com/garythung/trashnet), 
b) frontmost object was cropped, 
c) collages of 4 uniformly distributed random images to a 1200x800 canvas was created.

Split has the Train-Val-Test split of 80-10-10
Annotations has the bounding box annotations for classes for each image in VOC format, YOLO format and TF Records format