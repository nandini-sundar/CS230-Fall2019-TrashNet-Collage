
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
│   │   ├── test_labels.csv
│   │   ├── train_labels.csv
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
Annotations has the bounding box annotations for classes for each image in VOC format and YOLO format.

You can create the TF records using the csv files using this python file in cs230-waste-classification-and-detection/data_processing :

```
For Training TF record :
python generate_tfrecord.py --csv_input=annotations/train_labels.csv --output_path=annotations/train.record --img_path=/images/train_set/ --label_map annotations/label_map.pbtxt

For Validation TF record :
python generate_tfrecord.py --csv_input=annotations/val_labels.csv --output_path=annotations/val.record --img_path=/images/val_set/ --label_map annotations/label_map.pbtxt
```
