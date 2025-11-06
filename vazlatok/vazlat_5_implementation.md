# 5 Implementation process

## 5.1 Defining the recipe

 - Goal for app described in 4.1: AR with CV in a cooking environment
 - Need to develop CV system to track things in kitchen relative to cooking
 - No need for costly data creation stage: MS COCO already has suitable data 

*Algorithm 5.1: the recipe*

## 5.2 Collecting the data

 - MS COCO dataset downloaded using fiftyone
 - Only the pictures that match our trackable categories (filtering code)
 
## 5.3 Training the CV module

 - Tensorflow used for training CV module. Specifically MobileNet-SSD v2.
 - Tensorflow needs: Data in .tfrecord format. 
 - Converted coco-json + image to tfrecord with official Tensorflow tutorial
 - More on CV training later:
   - tf config files
   - docker & containerization
   - trained model to tf.js conversion (this might be in 5.4)

## 5.4 Application backend

 - How is the CV module integrated into the mobile app?
 - How does the app track the steps of the recipe?

## 5.5 AR-UI

 - How are augmentations rendered?
