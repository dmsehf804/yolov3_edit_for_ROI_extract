# yolov3_edit_for_ROI_extract
## ROI extractor for human
This project is editing YOLOv3 for ROI extractor for human
<hr>

## Editing file list
- detector.c
- darknet.c
- darknet.h
- image.c
- image.h
<hr>

## darknet.c

**421~432**

Specify required components as relative paths to avoid typing them directly on the command line

## detector.c

**585~746** 

Fixed to use only test_detector function

Apply a process to search the directory listing in a directory and to reference the files in each directory

**625**

**outfile_buffer**: output path

**626** 

**path**: input path

**672**

**jpg_checker**: `pn` is png, `jpg` is jpg

## image.c

**292~402**

ROI extractor - Select maximum area ROI using coordinates of recognized objects.

**317**

`prob`: accuracy.
`names[j]`: detected class name.

**351~366**

drawing box, label.

**367~370**

adding coordinates of objects.

**378~402**

Extracting maximum ROI using all coordinates and crop image.
If there is not human then just save original image








